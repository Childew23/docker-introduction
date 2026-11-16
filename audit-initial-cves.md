<h2>:mag: Vulnerabilities of <code>quiz-docker:initial</code></h2>

<details open="true"><summary>:package: Image Reference</strong> <code>quiz-docker:initial</code></summary>
<table>
<tr><td>digest</td><td><code>sha256:0626f6547f25e4a8663a4e75207e88c424aab34c28b73668164c23e42637199c</code></td><tr><tr><td>vulnerabilities</td><td><img alt="critical: 1" src="https://img.shields.io/badge/critical-1-8b1924"/> <img alt="high: 11" src="https://img.shields.io/badge/high-11-e25d68"/> <img alt="medium: 12" src="https://img.shields.io/badge/medium-12-fbb552"/> <img alt="low: 1" src="https://img.shields.io/badge/low-1-fce1a9"/> <img alt="unspecified: 5" src="https://img.shields.io/badge/unspecified-5-lightgrey"/></td></tr>
<tr><td>platform</td><td>linux/amd64</td></tr>
<tr><td>size</td><td>72 MB</td></tr>
<tr><td>packages</td><td>266</td></tr>
</table>
</details></table>
</details>

<table>
<tr><td valign="top">
<details><summary><img alt="critical: 1" src="https://img.shields.io/badge/C-1-8b1924"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>zlib</strong> <code>1.3.2-r1</code> (apk)</summary>

<small><code>pkg:apk/alpine/zlib@1.3.2-r1?os_name=alpine&os_version=3.24</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-4738?s=alpine&n=zlib&ns=alpine&t=apk&osn=alpine&osv=3.24&vr=%3C1.4-r0"><img alt="critical : CVE--2026--4738" src="https://img.shields.io/badge/CVE--2026--4738-lightgrey?label=critical%20&labelColor=8b1924"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.4-r0</code></td></tr>
<tr><td>Fixed version</td><td><code>1.4-r0</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.269%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>19th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>



</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 5" src="https://img.shields.io/badge/H-5-e25d68"/> <img alt="medium: 2" src="https://img.shields.io/badge/M-2-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>brace-expansion</strong> <code>2.0.2</code> (npm)</summary>

<small><code>pkg:npm/brace-expansion@2.0.2</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-13149?s=github&n=brace-expansion&t=npm&vr=%3E%3D2.0.0%2C%3C2.1.2"><img alt="high 7.7: CVE--2026--13149" src="https://img.shields.io/badge/CVE--2026--13149-lightgrey?label=high%207.7&labelColor=e25d68"/></a> <i>Uncontrolled Resource Consumption</i>

<table>
<tr><td>Affected range</td><td><code>>=2.0.0<br/><2.1.2</code></td></tr>
<tr><td>Fixed version</td><td><code>2.1.2</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.7</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:N/PR:N/UI:N/VC:N/VI:N/VA:H/SC:N/SI:N/SA:N/E:P/S:N/AU:Y/R:U/V:D/RE:M/U:Amber</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.364%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>31st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary
brace-expansion's expand() exhibits exponential-time - O(2ⁿ) - behavior in the number of consecutive non-expanding {} groups. A short, all-ASCII input (~90 bytes/30 groups) blocks the calling thread for minutes; a slightly longer input hangs it effectively indefinitely. Because the dominant consumers run on Node's single-threaded event loop, one small input can fully stall a worker/process.

In `expand_`, `post` is computed unconditionally at the top of the function, before the early-return branches that don't use it:
```js
const post = m.post.length ? expand_(m.post, max, false) : [''];   // always recurses
  ...
if (!isSequence && !isOptions) {
  if (m.post.match(/,(?!,).*\}/)) {
    str = m.pre + '{' + m.body + escClose + m.post;
    return expand_(str, max, true); // restart — `post` discarded
  }
  return [str];
}
```

For input like a{},{},…, the first {} is non-expanding, so control reaches the {a},b} rewrite branch - but `expand_` has already recursed into post over the entire remaining tail, only to throw the result away.
Each level therefore spawns two recursive expansions over essentially the same remaining work: `T(n) = 2·T(n−1) ⇒ O(2ⁿ)`.

The max option does not mitigate this: max only bounds the output-building loops; neither the post recursion nor the rewrite recursion consults it.
  
Measured on 5.0.6:

| groups (n) | input bytes | time |
|---|---|---|
| 20 | 60 | 130 ms |
| 24 | 72 | 1.9 s |
| 26 | 78 | 7.8 s |
| 30 (PoC) | 90 | ~2 min |

### Proof of concept
```js
const { expand } = require('brace-expansion');
// 30 non-expanding groups, ~90 bytes — blocks for minutes:
expand('a{},{},{},{},{},{},{},{},{},{},{},{},{},{},{},{},{},{},{},{},{},{},{},{},{},{},{},{},{},{}');
```

### Impact

Any application that passes attacker-influenced strings to brace-expansion.expand() - directly or transitively via minimatch/glob brace patterns - can be driven into a multi-minute-to-indefinite CPU hang by a tiny request, denying service on that thread/process.

### Remediation

Upgrade to a patched release. The fix:
1. Defers computing post until after the early-return branches (and computes it locally in the $-suffix branch), so post is only expanded when a brace set actually expands and the value is used. This alone removes the exponential.
1. Converts the {a},b} rewrite from recursion to an in-function loop, so a long run of rewrites cannot grow the call stack.

Verified: the PoC drops from ~2 min to 0.55 ms, 5,000 groups complete in ~344 ms, and output is identical to 5.0.6 across a behavioral-equivalence suite (sequences, padding, $-prefix, a{},b}c, {},a}b, x{{a,b}}y, etc.). Post-fix complexity is ~O(n²) on this input class - acceptable for the security fix; a linear rewrite can be a non-urgent follow-up.

If immediate upgrade isn't possible, avoid passing untrusted input to expand() / glob brace patterns, or run such expansion under a timeout/worker.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-69152?s=github&n=brace-expansion&t=npm&vr=%3E%3D2.0.0%2C%3C2.1.4"><img alt="high 7.5: CVE--2026--69152" src="https://img.shields.io/badge/CVE--2026--69152-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Uncontrolled Resource Consumption</i>

<table>
<tr><td>Affected range</td><td><code>>=2.0.0<br/><2.1.4</code></td></tr>
<tr><td>Fixed version</td><td><code>2.1.4</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N/A:H</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.647%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>52nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

The `maxLength` mitigation added in `5.0.8` for GHSA-mh99-v99m-4gvg / CVE-2026-14257 is incomplete. It bounds the accumulator where results are *combined*, but not the intermediate arrays that feed it. A ~25 KB input still crashes the Node process with an **uncatchable** out-of-memory error, so `try/catch` around `expand()` does not help.

A second, related path in the same function lets a ~400 KB input block the event loop for over two minutes without ever exceeding the memory bound.

### Details

`maxLength` was enforced in `combine()`, the single place output grows. Two arrays are built *before* `combine()` runs, and neither was bounded.

**1. Comma alternatives accumulate without a running total (memory exhaustion)**

Each alternative in `{a,b,c,...}` is expanded by its own recursive `expand_()` call, so each receives a full, independent `maxLength` allowance. The results were then concatenated into a single `values` array with no cumulative limit:

```js
values = []
for (let j = 0; j < n.length; j++) {
  values.push.apply(values, expand_(n[j], max, maxLength, false))
}

acc = combine(acc, pre, values, max, maxLength, ...)
```

With `A` alternatives, `values` can reach `A * maxLength` characters before `combine()` gets a chance to truncate it. At the default `maxLength` of 4,000,000 and 400 alternatives, that is well past any default heap.

**2. Padded sequences ignore `maxLength` while generating (CPU exhaustion)**

`expandSequence()` was bounded by `max` (the result *count*) but never consulted `maxLength`. A padded sequence's element width follows the input, so `{0...01..100000}` with a wide pad generates `max` elements, each as wide as the input, only for `combine()` to discard all but a handful.

Memory stays flat here, because V8 represents the padded strings as cons-strings, which is likely why this path was not caught alongside the original issue. The cost is time: work proportional to `max * width`.

| pad width | input bytes | results kept | time (5.0.8) | time (patched) |
|---|---|---|---|---|
| 20,000 | 20 KB | 199 | ~7.3 s | ~20 ms |
| 100,000 | 100 KB | 39 | ~32 s | ~20 ms |
| 400,000 | 400 KB | 9 | ~124 s | ~18 ms |

Output is byte-identical before and after the fix; only the wasted work is removed.

### Proof of concept

Memory exhaustion, against `5.0.8`:

```js
import { expand } from 'brace-expansion'

const part = '{' + '0'.repeat(50) + '1..100000}'
const input = '{' + Array(400).fill(part).join(',') + '}'  // ~25 KB

try {
  expand(input)
} catch (e) {
  // never reached - the process is already dead
}
```

```
FATAL ERROR: Ineffective mark-compacts near heap limit Allocation failed - JavaScript heap out of memory
Aborted
```

Event-loop stall, against `5.0.8`:

```js
import { expand } from 'brace-expansion'

// ~400 KB input, returns 9 results after roughly two minutes of blocking CPU
expand('{' + '0'.repeat(400_000) + '1..100000}')
```

### Impact

Denial of service. Any application that passes attacker-controlled input to `expand()`, directly or transitively through a glob or pattern-matching library, can be remotely crashed or stalled. The out-of-memory variant terminates the process and cannot be handled with `try/catch`.

Applications already on `5.0.8` are affected: the `5.0.8` mitigation does not cover these paths.

### Patches

Both intermediate arrays are now bounded as they are built, using the same `max` and `maxLength` limits already applied in `combine()`:

- `values` tracks a running result count and character length while alternatives are appended, and stops once either bound is reached.
- `expandSequence()` accepts `maxLength` and stops generating once the sequence's own characters reach it.

As with the existing limits, output is truncated rather than allowed to grow without bound, which matches how `max` already behaves. The defaults sit well above any realistic expansion, so legitimate input is unaffected.

### Workarounds

If upgrading is not immediately possible, avoid passing untrusted input to `expand()` or to glob brace patterns, or pass an explicitly small `max` **and** `maxLength`.

Note that a small `maxLength` alone was not sufficient on affected versions: it was applied per alternative rather than cumulatively, which is the root of the first issue above.

### Credits

The memory-exhaustion bypass was reported by Alessio Della Libera, CEO & Co-founder at [Numyra](https://numyra.ai/).

The sequence-generation issue was found while verifying that report.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-14257?s=github&n=brace-expansion&t=npm&vr=%3E%3D2.0.0%2C%3C2.1.3"><img alt="high 7.5: CVE--2026--14257" src="https://img.shields.io/badge/CVE--2026--14257-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Uncontrolled Resource Consumption</i>

<table>
<tr><td>Affected range</td><td><code>>=2.0.0<br/><2.1.3</code></td></tr>
<tr><td>Fixed version</td><td><code>5.0.8</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N/A:H</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.643%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>51st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

`expand()` bounds the *number* of results it produces (the `max` option,
`100_000` by default) but not their *length*. By chaining many brace groups,
an attacker keeps the result count under `max` while making every result grow
with the number of groups. Building `max` long results — plus the intermediate
arrays combined at each brace group — exhausts memory and crashes the Node
process with an **uncatchable** out-of-memory error. `try/catch` around
`expand()` does not help: the fatal error terminates the process.

A ~7.5 KB input (`'{a,b}'.repeat(1500)`) is enough to crash a default Node
process.

### Details

For `N` chained brace groups such as `'{a,b}'.repeat(N)`:

- the result count is `2^N`, immediately capped at `max` (`100_000`), so the
  `max` protection appears to hold, but
- each result is `N` characters long, so the total output size is
  `max × N` characters, which grows without bound in `N`.

`expand_` combines each brace set with the fully-expanded tail:

```js
const post = m.post.length ? expand_(m.post, max, false) : ['']
...
for (let j = 0; j < N.length; j++) {
  for (let k = 0; k < post.length && expansions.length < max; k++) {
    const expansion = pre + N[j] + post[k]   // grows one group longer per level
    ...
    expansions.push(expansion)
  }
}
```

The loop guard `expansions.length < max` limits how many strings are built, but
nothing limits how long they get. Each recursion level materializes another
array of up to `max` strings, one character longer than the level below, and —
because V8 represents `pre + N[j] + post[k]` as a cons-string (rope) that
references `post[k]` — those intermediate strings stay reachable through the
whole chain. Memory therefore scales with `max × N`.

Measured on `5.0.7` (`'{a,b}'.repeat(N)`, default `max`):

| groups (N) | input bytes | result count | peak RSS |
|---|---|---|---|
| 20 | 100 | 100,000 | ~80 MB |
| 50 | 250 | 100,000 | ~214 MB |
| 100 | 500 | 100,000 | ~409 MB |
| 300 | 1,500 | 100,000 | ~1,148 MB |
| 1500 | 7,500 | — | **OOM crash** |

### Proof of concept

```js
const { expand } = require('brace-expansion')

// ~7.5 KB input — crashes the process with a fatal, uncatchable OOM:
//   FATAL ERROR: ... JavaScript heap out of memory
try {
  expand('{a,b}'.repeat(1500))
} catch (e) {
  // never reached — the process is already dead
}
```

### Impact

Any application that passes attacker-influenced strings to
`brace-expansion.expand()` — directly, or transitively via `minimatch` / `glob`
brace patterns — can be crashed by a small request. Because the failure is a
fatal V8 out-of-memory error rather than a thrown exception, it cannot be caught
and it takes down the whole worker/process, denying service.

### Remediation

Upgrade to a patched release. The fix bounds the total number of characters a
single `expand()` call may accumulate (`EXPANSION_MAX_LENGTH`, default
`4_000_000`, configurable via a new `maxLength` option), applied inside the
output-building loops so intermediate arrays are bounded too. Once the limit is
reached, output is truncated — consistent with how `max` already truncates —
instead of growing without bound. The limit sits well above any realistic
expansion (100,000 results hitting `max` measure ~1M characters), so legitimate
input is unaffected.

After the fix, `'{a,b}'.repeat(1500)` returns a bounded, truncated result in
~0.7 s using ~340 MB and never crashes, including under a constrained 512 MB
heap.

The fix bounds memory but the algorithm still rebuilds intermediate arrays at
each level (roughly `O(N × maxLength)` work on this input class). A streaming
rewrite that produces output in `O(total output size)` can be a non-urgent
follow-up.

If immediate upgrade isn't possible, avoid passing untrusted input to
`expand()` / glob brace patterns, or pass a small explicit `max` **and**
`maxLength`.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-102278?s=github&n=brace-expansion&t=npm&vr=%3E%3D2.0.0%2C%3C2.1.6"><img alt="high 7.5: CVE--2026--102278" src="https://img.shields.io/badge/CVE--2026--102278-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Uncontrolled Resource Consumption</i>

<table>
<tr><td>Affected range</td><td><code>>=2.0.0<br/><2.1.6</code></td></tr>
<tr><td>Fixed version</td><td><code>2.1.6</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N/A:H</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.491%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>43rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

`expand_()` recurses once per level of brace *nesting*. Deeply nested input exhausts the native stack and crashes the process.

This is distinct from CVE-2026-14257 / GHSA-mh99-v99m-4gvg, which made the *tail* iterative (recursion on `m.post`, driven by how many groups are chained). Nesting depth drives a different recursion that the tail fix never touched, so the documented constant-stack-depth guarantee only ever covered chained input, not nested input.

It is also distinct from GHSA-6j4f-fj2g-mc7p, which fixed recursion in `parseCommaParts()`. Both payloads below still crash with that fix applied.

### Two recursion sites

**Comma members.** Each alternative of a brace set is expanded by a recursive call, so nesting a set inside every alternative recurses once per level:

```js
expand('{a,'.repeat(4000) + 'z' + '}'.repeat(4000))
// RangeError: Maximum call stack size exceeded
```

Crashes at depth 3,907 - about **15.6 KB** of input.

**Single set.** A brace set whose body parses to a single part is expanded by a recursive call before being re-wrapped (`x{{a,b}}y` -> `x{a}y x{b}y`), which recurses once per nesting level:

```js
expand('{'.repeat(3200) + 'a,b' + '}'.repeat(3200))
// RangeError: Maximum call stack size exceeded
```

Crashes at depth 3,125 - about **6.25 KB** of input. This is the cheapest stack-exhaustion payload known against this package: roughly a quarter the input of GHSA-6j4f-fj2g-mc7p (29 KB), and about a tenth of minimatch's `MAX_PATTERN_LENGTH` (65,536).

### Why `max` and `maxLength` do not help

Both crashes happen while recursing into sub-expansions, before the result set grows. The payloads produce almost no output - the single-set case yields 2 results - so neither bound is ever the limiter. `expand(payload, { max: 1, maxLength: 1 })` still overflows.

### Impact

Any application passing an untrusted string to `expand()`, directly or through `minimatch` / `glob` as a user-supplied glob pattern, can be crashed. In Node a `RangeError` the application does not catch terminates the process, so a server globbing user input is exposed to remote unauthenticated denial of service.

Availability only. No code execution, no data exposure.

### Affected versions

Verified affected on 1.1.18, 2.1.4, 3.0.6 and 5.0.9, at near-identical depths on every line (single set: 3,125 on all four; comma members: 3,907-4,102). Not a regression from any recent fix - the gap predates them.

### Patch

A `maxDepth` bound (default `EXPANSION_MAX_DEPTH`) is threaded through `expand_()`. Past the cap a group is treated as non-expanding and returned literally, which is how the parser already handles a group that cannot expand. This matches the existing `max` / `maxLength` caps, which truncate rather than throw, so `expand()` continues never to throw on any input.

The default sits far above any realistic nesting depth and well below the crash threshold.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-102276?s=github&n=brace-expansion&t=npm&vr=%3E%3D2.0.0%2C%3C2.1.5"><img alt="high 7.5: CVE--2026--102276" src="https://img.shields.io/badge/CVE--2026--102276-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Uncontrolled Resource Consumption</i>

<table>
<tr><td>Affected range</td><td><code>>=2.0.0<br/><2.1.5</code></td></tr>
<tr><td>Fixed version</td><td><code>2.1.5</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N/A:H</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.455%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>40th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

`parseCommaParts()` can exhaust the native stack and crash the process. There are two distinct ways to trigger it, both reachable from a single untrusted pattern string.

This is the parsing-side counterpart to CVE-2026-14257 / GHSA-mh99-v99m-4gvg. That fix made `expand_()` iterative and documented a constant-stack-depth guarantee, but `parseCommaParts()` was left recursive, so the guarantee only held for one of the two parsing paths.

### Vector 1 - unbounded recursion on `post`

`parseCommaParts()` recursed on the remainder of the string once per brace group:

```js
const postParts = parseCommaParts(post)   // unbounded
```

A brace group containing many comma-separated groups drives one recursion level per group:

```js
expand('{' + '{a},'.repeat(7000) + 'b}')
// RangeError: Maximum call stack size exceeded
```

About 7,300 repetitions - roughly 29 KB of input - is enough on Node 24; roughly 6,300 (25 KB) on Node 18. The threshold is identical on every affected release line.

### Vector 2 - `push.apply` with an unbounded array

Even with the recursion removed, `parseCommaParts()` spread whole arrays into an argument list:

```js
p.push.apply(p, postParts)
parts.push.apply(parts, p)
```

`Function.prototype.apply` places one argument per element on the stack, so a single large array overflows it. This needs **no recursion depth at all** - the following reaches a recursion depth of exactly 1:

```js
expand('{{x},' + 'a,'.repeat(125000) + 'b}')
// RangeError: Maximum call stack size exceeded
```

Threshold is about 124,300 repetitions (~249 KB). This vector was not part of the original report; it was found while verifying the fix. A patch that only de-recurses but keeps `push.apply` leaves a working denial of service behind.

### Why `max` and `maxLength` do not help

Both crashes happen during **parsing**, before any expansion. The payloads produce one result per group, so output size grows linearly with input and is never the limiter. `expand(payload, { max: 1, maxLength: 1 })` still overflows.

### Impact

Any application that passes an untrusted string to `expand()` - directly, or through `minimatch` / `glob` where it is a user-supplied glob pattern - can be crashed. In Node, a `RangeError` that the application does not catch terminates the process, so a server that globs user input is exposed to remote unauthenticated denial of service.

`minimatch`'s own `MAX_PATTERN_LENGTH` cap (65,536) does not help against vector 1: the overflow threshold sits well below it. Confirmed on minimatch 10.2.6 - a 64,003-byte pattern passes the length check and overflows both `minimatch.braceExpand()` and `new minimatch.Minimatch()`.

This is an availability-only issue. No code execution and no data exposure.

### Not a regression

5.0.8 and 5.0.9 overflow at the same repetition count, so the gap predates the recent advisories; those fixes simply did not reach it. Verified affected on 1.1.18, 2.1.4, 3.0.6, 5.0.8 and 5.0.9, all at an identical threshold.

### Patch

`parseCommaParts()` is rewritten as a loop that carries the partial part across chunks, and every array append uses an element-by-element loop rather than `push.apply`. The redundant `if (!str) return ['']` guard is dropped - the loop returns `['']` for the empty string on its own.

Equivalence of the old and new implementations was checked by differential testing: exhaustive over every string of `{`, `}`, `,`, `a` up to length 7 plus 300,000 random inputs - 322,000 cases, zero mismatches.

### Severity note

Scored 7.5 High under CVSS 3.1 for consistency with the other availability advisories on this package (GHSA-mh99-v99m-4gvg, GHSA-rgw5-rvv9-x895), which use the same vector. The reporter self-assessed 6.9 Medium under CVSS 4.0 (`CVSS:4.0/AV:N/AC:L/AT:N/PR:N/UI:N/VC:N/VI:N/VA:L/SC:N/SI:N/SA:N`).

### Credit

Reported by baeseungwon1010, with a working proof of concept and a proposed patch. Vector 2 was identified during maintainer verification.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-33750?s=github&n=brace-expansion&t=npm&vr=%3E%3D2.0.0%2C%3C2.0.3"><img alt="medium 6.5: CVE--2026--33750" src="https://img.shields.io/badge/CVE--2026--33750-lightgrey?label=medium%206.5&labelColor=fbb552"/></a> <i>Uncontrolled Resource Consumption</i>

<table>
<tr><td>Affected range</td><td><code>>=2.0.0<br/><2.0.3</code></td></tr>
<tr><td>Fixed version</td><td><code>5.0.5</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:N/I:N/A:H</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.457%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>40th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Impact

A brace pattern with a zero step value (e.g., `{1..2..0}`) causes the sequence generation loop to run indefinitely, making the process hang for seconds and allocate heaps of memory.

The loop in question:

https://github.com/juliangruber/brace-expansion/blob/daa71bcb4a30a2df9bcb7f7b8daaf2ab30e5794a/src/index.ts#L184

`test()` is one of

https://github.com/juliangruber/brace-expansion/blob/daa71bcb4a30a2df9bcb7f7b8daaf2ab30e5794a/src/index.ts#L107-L113

The increment is computed as `Math.abs(0) = 0`, so the loop variable never advances. On a test machine, the process hangs for about 3.5 seconds and allocates roughly 1.9 GB of memory before throwing a `RangeError`. Setting max to any value has no effect because the limit is only checked at the output combination step, not during sequence generation.

This affects any application that passes untrusted strings to expand(), or by error sets a step value of `0`. That includes tools built on minimatch/glob that resolve patterns from CLI arguments or config files. The input needed is just 10 bytes.

### Patches


Upgrade to versions
- 5.0.5+

A step increment of 0 is now sanitized to 1, which matches bash behavior.

### Workarounds

Sanitize strings passed to `expand()` to ensure a step value of `0` is not used.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-102277?s=github&n=brace-expansion&t=npm&vr=%3E%3D2.0.0%2C%3C2.1.7"><img alt="medium 5.3: CVE--2026--102277" src="https://img.shields.io/badge/CVE--2026--102277-lightgrey?label=medium%205.3&labelColor=fbb552"/></a> <i>Uncontrolled Resource Consumption</i>

<table>
<tr><td>Affected range</td><td><code>>=2.0.0<br/><2.1.7</code></td></tr>
<tr><td>Fixed version</td><td><code>2.1.7</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N/A:L</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.428%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>38th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

Expanding `{a},b}`-shaped input takes time quadratic in the number of literal `}` characters, blocking the event loop.

Bash preserves a quirk where a brace group followed by a comma set still expands (`{a},b}`). The parser implements this by rewriting the string and restarting the scan. Each pass absorbs exactly one `}` and re-scans from the beginning, so `n` trailing braces cost `n` full passes.

### Reproduction

```js
const build = n => '{a}' + '}'.repeat(n) + ',z}'

for (const n of [8000, 16000, 32000, 64000, 128000]) {
  const t = Date.now()
  expand(build(n))
  console.log(n, Date.now() - t + 'ms')
}
```

| n | input | time | results |
|---|---|---|---|
| 8,000 | 8 KB | 110 ms | 2 |
| 16,000 | 16 KB | 446 ms | 2 |
| 32,000 | 32 KB | 1.7 s | 2 |
| 64,000 | 64 KB | 6.9 s | 2 |
| 128,000 | 128 KB | **27.7 s** | 2 |

`ms/n^2` is flat at ~1.7 and each doubling of `n` costs exactly 4.0x - quadratic. 128 KB of input blocks the event loop for nearly half a minute to produce two results.

### Mechanism

Instrumenting the rewrite branch confirms it runs exactly `n + 1` times, once per literal `}`, each re-scanning the whole string.

There is a second multiplier. The rewrite replaces the group's closing `}` with the internal `escClose` sentinel, which is `'\0CLOSE' + Math.random() + '\0'` - about 25 characters. The working string therefore *grows* by ~25 characters on every pass:

| n | input length | final string length |
|---|---|---|
| 1,000 | 1,006 | 26,006 |
| 8,000 | 8,006 | 208,006 |

So the input is inflated roughly 26x, and that factor multiplies both the quadratic constant and peak memory. This makes it partly a memory-pressure issue as well as a CPU one.

### Why `max` and `maxLength` do not help

The cost is in parsing, before the result set exists. The payload yields 2 results regardless of size, so neither bound is ever reached.

### Impact

An application passing an untrusted pattern to `expand()`, directly or through `minimatch` / `glob`, can have its event loop blocked for tens of seconds by a payload well under minimatch's 65,536-character cap. For a single-threaded Node server that is a full stall, not just a slow request.

Degraded availability rather than a crash - the process recovers once the expansion completes.

### Affected versions

Verified affected on 1.1.18, 2.1.4, 3.0.6 and 5.0.9, all within a few percent of each other (~460-490 ms at n=16,000).

### Patch

The rewrite loop gets an iteration bound. Past the cap the remaining string is treated as non-expanding and returned literally, consistent with the existing `max` / `maxLength` caps, which truncate rather than throw.

Note this bounds the number of passes, not the cost of each: worst-case work remains proportional to `cap x input length`. The cap is set low enough that the residual is bounded in practice, and far above what any realistic `{a},b}` input needs.

### Severity note

Scored 5.3 Medium (`A:L`) for consistency with GHSA-3jxr-9vmj-r5cp, the other algorithmic-complexity advisory on this package (CWE-407), which uses the same vector. The stack-exhaustion advisories on this package score `A:H` because they crash the process outright; this one stalls it.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 5" src="https://img.shields.io/badge/M-5-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>ip-address</strong> <code>10.1.0</code> (npm)</summary>

<small><code>pkg:npm/ip-address@10.1.0</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-69192?s=github&n=ip-address&t=npm&vr=%3C%3D10.3.0"><img alt="high 7.7: CVE--2026--69192" src="https://img.shields.io/badge/CVE--2026--69192-lightgrey?label=high%207.7&labelColor=e25d68"/></a> <i>Improper Input Validation</i>

<table>
<tr><td>Affected range</td><td><code><=10.3.0</code></td></tr>
<tr><td>Fixed version</td><td><code>10.3.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.7</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:N/PR:N/UI:N/VC:L/VI:N/VA:N/SC:H/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.465%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>41st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

`Address4` accepts an octet written with a leading zero and decodes it as decimal, while the WHATWG URL host parser, `inet_aton`, and `getaddrinfo` all decode a leading zero as octal. The library and the network stack therefore disagree about which host a string names. `new Address4('012.0.0.1')` reports `correctForm()` of `12.0.0.1` and `isPrivate()` of `false`, but `fetch('http://012.0.0.1/')` connects to `10.0.0.1`.

An application that builds a network trust-boundary decision on these checks (for example a filter intended to block Server-Side Request Forgery, or SSRF) will classify an internal target as external and allow the request. SSRF is an attack in which a user-supplied address coaxes the server into making a request to an internal destination the user could not otherwise reach, such as a loopback service or a cloud metadata endpoint.

### Details

`Address4.parse` gates untrusted input on `RE_ADDRESS` (`src/v4/constants.ts:5`), whose per-octet alternative is:

```
(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)
```

The `[01]?[0-9][0-9]?` branch matches a leading zero, so `012` passes validation. Every downstream decode then reads the octet with `parseInt(part, 10)` (`src/common.ts:87`), yielding 12. A resolver reading the same string treats the leading `0` as base 8 and yields 10.

The defect is in the parse gate rather than in any one classifier, so every consumer of `Address4` inherits it: `isPrivate()`, `isLoopback()`, `isLinkLocal()`, `isCGNAT()`, `isInSubnet()`, `isHostInSubnet()`, and `correctForm()` are all computed from the mis-decoded octets.

`Address6` already rejects this notation on its IPv4-in-IPv6 path, throwing "IPv4 addresses can't have leading zeroes." (`src/ipv6.ts:751-762`), so `Address4` is the outlier within the library.

### Affected versions

`<= 10.3.0`. Unlike GHSA-22jq-vg5j-6vgg and GHSA-4xrf-jv44-h6hh, which were bounded below by the `is*` classification API introduced in 10.1.1, this defect is in `parse` and reaches every release: a guard built on `isInSubnet()` against the RFC 1918 ranges is affected in versions predating that API.

### Impact

The disagreement runs in both directions. Under-blocking is the security-relevant case; over-blocking is a correctness and availability problem.

| Input | `correctForm()` | Classified as | Resolver reaches | Effect |
|---|---|---|---|---|
| `012.0.0.1` | `12.0.0.1` | public | `10.0.0.1` | internal target allowed |
| `012.012.012.012` | `12.12.12.12` | public | `10.10.10.10` | internal target allowed |
| `010.0.0.1` | `10.0.0.1` | private | `8.0.0.1` | public target blocked |

Reachable targets are those whose leading octet is expressible as a three-character octal literal, which covers the whole of `10.0.0.0/8` and `0.0.0.0/8`. A four-character octet such as `0177` for 127 is rejected by the regex, so loopback is not reachable through this path; see the note on rejection below for why rejection is not the same as safety.

### Reachability

A leading-zero address is a legal URL host, so this is reachable through the ordinary URL path with no unusual application shape required:

```js
new URL('http://012.0.0.1/').hostname   // '10.0.0.1'
```

This distinguishes it from GHSA-4xrf-jv44-h6hh, where the `/0` CIDR suffix could not survive URL parsing and exploitation therefore required an application that accepted a bare suffix-bearing string. Here the attack rides the same code path a normal user-supplied URL takes.

### Proof of concept

`npm i ip-address@<!-- -->10.3.0`, then:

```js
const { Address4 } = require('ip-address');

// A guard of the shape the library documents.
function isBlocked(host) {
  return Address4.isValid(host) && new Address4(host).isPrivate();
}

for (const h of ['10.0.0.1', '012.0.0.1', '012.012.012.012']) {
  console.log(isBlocked(h) ? 'BLOCK' : 'ALLOW', h,
              '-> resolver reaches', new URL('http://' + h + '/').hostname);
}
```

On affected versions:

```
BLOCK 10.0.0.1 -> resolver reaches 10.0.0.1
ALLOW 012.0.0.1 -> resolver reaches 10.0.0.1
ALLOW 012.012.012.012 -> resolver reaches 10.10.10.10
```

The literal RFC 1918 address is blocked as expected; the octal-ambiguous spellings of the same destinations are allowed through.

### Remediation

Upgrade to the patched release. In the fix, `Address4.parse` rejects any octet with a leading zero followed by further digits, mirroring the check `Address6` already applies at `src/ipv6.ts:751`, and `RE_ADDRESS` is tightened so those forms no longer appear in the valid corpus. After upgrading, `Address4.isValid('012.0.0.1')` returns `false` and the constructor throws `AddressError`.

This rejects input that previous releases accepted. An application that deliberately feeds zero-padded addresses such as `010.010.010.010` from a legacy system must strip the padding before parsing.

If you cannot upgrade immediately, reject any host whose octets carry a leading zero before you parse it:

```js
if (host.split('.').some((octet) => /^0\d/.test(octet))) throw new Error('ambiguous address');
```

### A note on SSRF defense

These methods are address classifiers, not a complete SSRF defense. Regardless of this fix, a robust SSRF guard must resolve the hostname and validate the *resolved* IP against the socket it connects to, and account for DNS rebinding and redirects. Treat these checks as one layer, not the only one.

One specific pitfall is worth naming, because the fix above does not remove it. `Address4.isValid()` returning `false` means "this is not a dotted-quad IPv4 literal"; it does not mean "this is not an address that will reach an internal host". Every one of the following is rejected by `isValid()` and still resolves to loopback:

```
0177.0.0.1    0x7f.0.0.1    0x7f000001    2130706433
127.1         127.0.1       127.0.0.1.    １２７.0.0.1
```

A guard shaped `if (Address4.isValid(h)) { check() } else { treatAsHostname() }` therefore routes all of them past the IP check. Rejecting these is correct behavior for an IPv4 parser and is not changed by this advisory, but a guard must treat "not a valid literal" as a case to resolve and re-check, never as a case to allow.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-111997?s=github&n=ip-address&t=npm&vr=%3C%3D10.7.3"><img alt="medium 6.3: CVE--2026--111997" src="https://img.shields.io/badge/CVE--2026--111997-lightgrey?label=medium%206.3&labelColor=fbb552"/></a> <i>Inefficient Regular Expression Complexity</i>

<table>
<tr><td>Affected range</td><td><code><=10.7.3</code></td></tr>
<tr><td>Fixed version</td><td><code>10.7.4</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:N/VC:N/VI:N/VA:L/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.315%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>25th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

`new Address6()` and `Address6.isValid()` strip a zone identifier with the pattern `/%.*$/` before they apply the 45-character length limit. When the string holds many `%` characters followed by a line terminator, the pattern is retried from every `%` and each attempt scans to the line terminator before failing, so rejecting the string takes time proportional to the square of its length. 10,000 `%` characters and a newline take 41 ms, 40,000 take 632 ms and 100,000 take 3.9 s of synchronous work. The same strings without the newline are rejected in under a millisecond.

An application that validates an attacker-supplied string with these methods can be stalled by a single long request. The input is rejected with the correct `AddressError`; the cost of reaching that rejection is the defect.

### Details

The constructor in `src/ipv6.ts` removes the CIDR suffix, then the zone, then checks the length of what is left:

```ts
const zone = constants6.RE_ZONE_STRING.exec(address);

if (zone) {
  this.zone = zone[0];

  address = address.replace(constants6.RE_ZONE_STRING, '');
}

const longest = this.groups * 5 + 5;

if (address.length > longest) {
  throw new AddressError(`IPv6 addresses are at most ${longest} characters.`);
}
```

`RE_ZONE_STRING` is `/%.*$/`. It has no anchor at its start, `.` does not match a line terminator (`\n`, `\r`, U+2028 or U+2029), and without the `m` flag `$` matches only at the end of the input. For `%` repeated N times and then `\n`, the engine starts a match at the first `%`, `.*` consumes the remaining `%` characters up to the newline, `$` fails there, and backtracking through every shorter `.*` fails too. The engine then starts again at the second `%`, and so on: N starts, each proportional to N. The length limit that follows rejects the string in constant time, after the scan has already run.

The line terminator need not be last. Any string in which many `%` characters precede a line terminator behaves the same way.

Every entry point that passes a caller's string to the `Address6` constructor is affected: `new Address6()`, `isValid()`, both arguments of `fromAddressAndMask()` and `fromAddressAndWildcardMask()`, and the prefix argument of `fromAddress4Nat64()` and `toAddress4Nat64()`. `fromWildcard()` rejects a `%` before it constructs anything, `fromURL()` admits only hex digits, colons and dots in a host, and `fromArpa()` checks the nibble grammar first, so those three are unaffected. `Address4` has no zone and is unaffected.

### Affected versions

`<= 10.7.3`. The zone pattern has been in the constructor since 1.0.0; 5.9.4, 9.0.5 and 10.7.0 show the same timings as 10.7.3.

### Impact

`Address6.isValid()` on N `%` characters and a newline, measured on ip-address 10.7.3 and node 24.21.0:

| Input | Wall time | Same length of `!` |
|---|---|---|
| 5,461 characters | 13 ms | 0.1 ms |
| 16 KiB | 108 ms | 0.1 ms |
| 100 KB | 3.9 s | 0.1 ms |
| 256 KiB | 27 s | 0.2 ms |

The parse is synchronous, so the event loop is blocked for the whole of the wall time and nothing else on that process is served. No memory is retained and the process resumes when the call returns.

### Reachability

The input needs a line terminator after the `%` characters, which decides where it can arrive. An HTTP header value cannot carry a carriage return or a line feed, so a host or address taken from a header does not reach this. A URL can carry both characters percent-encoded at three bytes each, and Node's default 16 KB limit on the request line and headers admits about 5,461 of them: 13 ms. A request body is where the larger sizes come from. Common body parsers default to between 100 KB and 1 MB, and at 100 KB one field passed to the parser unchecked blocks the process for 3.9 s.

### Proof of concept

`npm i ip-address@<!-- -->10.7.3`, then:

```js
const { Address6 } = require('ip-address');

function time(input) {
  const start = process.hrtime.bigint();

  Address6.isValid(input);

  return `${(Number(process.hrtime.bigint() - start) / 1e6).toFixed(1)} ms`;
}

for (const n of [10000, 20000, 40000, 100000]) {
  console.log(`${n}: ${time(`${'%'.repeat(n)}\n`)}, without the newline ${time('%'.repeat(n))}`);
}
```

On affected versions (node 24.21.0):

```
10000: 41.0 ms, without the newline 0.0 ms
20000: 161.1 ms, without the newline 0.0 ms
40000: 632.4 ms, without the newline 0.1 ms
100000: 3899.8 ms, without the newline 0.1 ms
```

Each doubling of the input multiplies the time by four.

### Remediation

Upgrade to the patched release. In the fix, the constructor finds the zone by the index of the first `%` and accepts the remainder as a zone only when it holds no line terminator, which reads the input once. 1 MiB of the input above is rejected in about a millisecond. Every address that parsed before parses to the same result, and a string with a line terminator after a `%` is rejected as it was.

`RE_ZONE_STRING` stays exported from `v6/constants` for code that imports it directly and is marked `@<!-- -->deprecated`; the library itself does not call it.

If you cannot upgrade immediately, reject a candidate longer than an address with a zone identifier can be before you parse it:

```js
if (host.length > 64) throw new Error('not an IP address');
```

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-101913?s=github&n=ip-address&t=npm&vr=%3C%3D10.5.0"><img alt="medium 6.3: CVE--2026--101913" src="https://img.shields.io/badge/CVE--2026--101913-lightgrey?label=medium%206.3&labelColor=fbb552"/></a> <i>Incorrect Comparison</i>

<table>
<tr><td>Affected range</td><td><code><=10.5.0</code></td></tr>
<tr><td>Fixed version</td><td><code>10.5.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:N/VC:L/VI:N/VA:N/SC:L/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.386%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>33rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

`Address6.isLinkLocal()` recognizes `fe80::/64` rather than `fe80::/10`. Link-local unicast is the whole `/10` under RFC 4291 §2.4 and the IANA IPv6 Special-Purpose Address Registry, so the method returns `false` for every link-local address outside the one `/64` that stateless address autoconfiguration happens to use. `new Address6('fe81::1').isLinkLocal()` is `false`.

The library contradicts itself on the same object: for `fe81::1`, `getType()` returns `'Link-local unicast'`, `getScope()` returns `'Link local'`, and `isHostInSubnet(new Address6('fe80::/10'))` returns `true`, while `isLinkLocal()` returns `false`.

An application that builds a network trust-boundary decision on these checks (for example a filter intended to block Server-Side Request Forgery, or SSRF) will classify a link-local target as unremarkable and allow the request. SSRF is an attack in which a user-supplied address coaxes the server into making a request to an internal destination the user could not otherwise reach.

### Details

`isLinkLocal()` in `src/ipv6.ts` compares the first 64 bits of the address against a literal string:

```ts
// Zeroes are required, i.e. we can't check isHostInSubnet with 'fe80::/10'
if (
  this.getBitsBase2(0, 64) ===
  '1111111010000000000000000000000000000000000000000000000000000000'
) {
  return true;
}
```

The comparison requires the first 64 bits to be exactly `fe80:0000:0000:0000`, so it accepts 2⁶⁴ of the 2¹¹⁸ addresses in `fe80::/10`. The comment states a premise the library disproves: `getType()` classifies the same range with `isHostInSubnet` against the `'fe80::/10': 'Link-local unicast'` entry in `src/v6/constants.ts`, and `Address4.isLinkLocal()` is a plain `isHostInSubnet` test against `169.254.0.0/16`. RFC 4291 §2.5.6 constrains the format of an autoconfigured link-local address; it does not define the range, and reading it as the definition is the likeliest origin of the `/64` comparison.

The IPv4-mapped and NAT64 well-known paths of `isLinkLocal()` are unaffected: `::ffff:169.254.169.254` and `64:ff9b::a9fe:a9fe` are classified by their embedded IPv4 address and report `true`.

### Affected versions

`<= 10.5.0`. The comparison has had this shape since `Address6.isLinkLocal()` was introduced, so every release exposing the method is affected.

### Impact

Every well-formed address in `fe80::/10` outside `fe80::/64` is parsed successfully, `isValid()` is `true`, and the classifier reports something untrue about it. No other classifier catches these addresses: `isPrivate()` covers ULA (`fc00::/7`), not link-local.

| Address | `isLinkLocal()` | `getType()` | `getScope()` |
|---|---|---|---|
| `fe80::1` | `true` | Link-local unicast | Link local |
| `fe81::1` | `false` | Link-local unicast | Link local |
| `fe8f::1` | `false` | Link-local unicast | Link local |
| `febf::1` | `false` | Link-local unicast | Link local |
| `fe80:0:0:1::1` | `false` | Link-local unicast | Link local |
| `fe80::1:0:0:0:1` | `false` | Link-local unicast | Link local |

Python's `ipaddress` module, the `IN6_IS_ADDR_LINKLOCAL` macro in `netinet6/in6.h`, and Linux's `ipv6_addr_type()` all apply a ten-bit prefix test and classify every row above as link-local.

A request admitted through a guard built on `isLinkLocal()` reaches a link-local host on the server's own segment: a neighboring machine or the on-link router. An IPv6 link-local destination generally needs a zone index and a neighbor on the same link, so the reach is the server's own segment rather than the internet or a universal metadata endpoint, and the severity reflects that.

### Proof of concept

`npm i ip-address@<!-- -->10.5.0`, then:

```js
const { Address6 } = require('ip-address');

// A guard of the shape the library documents.
function isBlocked(host) {
  const a = new Address6(host);
  return a.isLoopback() || a.isLinkLocal() || a.isPrivate() || a.isMulticast() || a.isUnspecified();
}

for (const h of ['fe80::1', 'fe81::1', 'febf::1', 'fe80:0:0:1::1']) {
  const a = new Address6(h);
  console.log(isBlocked(h) ? 'BLOCK' : 'ALLOW', h, '-> getType()', a.getType());
}
```

On affected versions:

```
BLOCK fe80::1 -> getType() Link-local unicast
ALLOW fe81::1 -> getType() Link-local unicast
ALLOW febf::1 -> getType() Link-local unicast
ALLOW fe80:0:0:1::1 -> getType() Link-local unicast
```

### Remediation

Upgrade to the patched release. In the fix, `isLinkLocal()` tests the address against `fe80::/10` with the same `isHostInSubnet` predicate `getType()` and `Address4.isLinkLocal()` use. The same release adds `2001::/32` to the type table so `getType()` reports `'Teredo'` for the addresses `isTeredo()` returns `true` for; that is a consistency correction with no security effect.

If you cannot upgrade immediately, test the range directly:

```js
const LINK_LOCAL = new Address6('fe80::/10');
const linkLocal = new Address6(host).isHostInSubnet(LINK_LOCAL);
```

### A note on SSRF defense

These methods are address classifiers, not a complete SSRF defense. Regardless of this fix, a robust SSRF guard must resolve the hostname and validate the *resolved* IP against the socket it connects to, and account for DNS rebinding and redirects. Treat these checks as one layer, not the only one.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-101912?s=github&n=ip-address&t=npm&vr=%3C%3D10.7.0"><img alt="medium 6.3: CVE--2026--101912" src="https://img.shields.io/badge/CVE--2026--101912-lightgrey?label=medium%206.3&labelColor=fbb552"/></a> <i>Incorrect Comparison</i>

<table>
<tr><td>Affected range</td><td><code><=10.7.0</code></td></tr>
<tr><td>Fixed version</td><td><code>10.7.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:N/VC:N/VI:L/VA:N/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.370%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>31st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

`isInSubnet()` and `isHostInSubnet()` accept an address of either family and compare masked binary strings without checking that both operands are the same family. `Address4` pads to 32 bits and `Address6` to 128, so whenever the leading bits agree the strings are equal: `new Address6('a00::1').isInSubnet(new Address4('10.0.0.0/8'))` is `true`, and `new Address4('32.0.0.1').isInSubnet(new Address6('2000::/3'))` is `true`. No IPv4 address is inside an IPv6 network, so both answers are untrue.

An application that parses untrusted input as whichever family accepts it and then tests the result against a fixed-family allowlist can admit an address outside the list.

### Details

Both methods are in `src/common.ts`:

```ts
export function isInSubnet(this: Address4 | Address6, address: Address4 | Address6) {
  if (this.subnetMask < address.subnetMask) {
    return false;
  }

  return isHostInSubnet.call(this, address);
}

export function isHostInSubnet(this: Address4 | Address6, address: Address4 | Address6) {
  return this.mask(address.subnetMask) === address.mask();
}
```

`mask(n)` returns the first `n` bits of the address as a string of `0` and `1`, taken from a representation padded to the family's width. `new Address6('a00::1').mask(8)` is `'00001010'`, and so is `new Address4('10.0.0.0/8').mask()`, so string equality reports containment. The signature admits either family on either side, so TypeScript raises nothing, and the `v4` property on `Address6` marks IPv4 notation (`::ffff:10.0.0.1`) rather than family, so it does not discriminate either.

Which cross-family pairs coincide depends on the network's prefix length. `mask(n)` on an `Address4` returns at most 32 bits, so an IPv6 network longer than `/32` never matches an IPv4 address, and an IPv6 network of `/32` or shorter matches exactly the IPv4 addresses whose leading bits equal its prefix. An IPv4 network is at most 32 bits and matches every IPv6 address whose leading bits equal its prefix.

### Affected versions

`<= 10.7.0`. The comparison has had this shape since the methods were written, so every release is affected.

### Impact

| Expression | Result | Reason |
|---|---|---|
| `new Address6('a00::1').isInSubnet(new Address4('10.0.0.0/8'))` | `true` | both mask to `00001010` |
| `new Address4('10.0.0.1').isInSubnet(new Address6('a00::/8'))` | `true` | the same bits, reversed |
| `new Address4('32.0.0.1').isInSubnet(new Address6('2000::/3'))` | `true` | both begin `001` |
| `new Address4('32.1.13.184').isInSubnet(new Address6('2001:db8::/32'))` | `true` | the `/32` spells an IPv4 address |
| `new Address6('cb00:7100::1').isInSubnet(new Address4('203.0.113.0/24'))` | `true` | the `/24` spells an IPv6 prefix |
| `new Address4('10.0.0.1').isInSubnet(new Address6('::ffff:10.0.0.0/104'))` | `false` | `/104` is longer than 32 bits |
| `new Address4('8.8.8.8').isInSubnet(new Address4('10.0.0.0/8'))` | `false` | same-family control |

In the allowlist direction the check admits an address outside the list; in the denylist direction it blocks an address outside the list. What the coincidence can admit is narrow. An IPv6 allowlist of `/32` or shorter admits the IPv4 addresses its prefix spells: `2001:db8::/32` admits exactly `32.1.13.184`, and `2000::/3` admits `32.0.0.0/3`. Those are public IPv4 addresses; the private, loopback, and link-local ranges begin with bit patterns no allocated IPv6 prefix shares. An IPv4 allowlist admits the IPv6 addresses its prefix spells, and those all sit in blocks IANA has not allocated. So a request admitted through this defect reaches an address outside the intended list, not an internal host, and the severity reflects that.

### Proof of concept

`npm i ip-address@<!-- -->10.7.0`, then:

```js
const { Address4, Address6 } = require('ip-address');

// An allowlist of the application's own IPv6 range, tested against whichever
// family the input parses as.
const allowed = new Address6('2001:db8::/32');

function parse(host) {
  return Address4.isValid(host) ? new Address4(host) : new Address6(host);
}

for (const h of ['2001:db8::1', '2001:db9::1', '32.1.13.184', '32.1.13.185']) {
  console.log(parse(h).isInSubnet(allowed) ? 'ALLOW' : 'BLOCK', h);
}
```

On affected versions:

```
ALLOW 2001:db8::1
BLOCK 2001:db9::1
ALLOW 32.1.13.184
BLOCK 32.1.13.185
```

The IPv6 rows are right. The IPv4 address whose 32 bits equal the allowlist's prefix is admitted; the one next to it is not.

### Remediation

Upgrade to the patched release. In the fix, `isHostInSubnet()` returns `false` when the two addresses are of different families, and `isInSubnet()` inherits the answer. The methods keep accepting either family so existing call sites compile. A caller that means to compare across families converts first, with `Address6.fromAddress4()`, `to4()`, or `toAddress4Nat64()`: `new Address6('::ffff:10.0.0.1').to4().isInSubnet(new Address4('10.0.0.0/8'))` is `true`, as before.

If you cannot upgrade immediately, compare the classes before you compare the addresses:

```js
const contained = host.constructor === network.constructor && host.isInSubnet(network);
```

### A note on SSRF defense

These methods are address classifiers, not a complete SSRF defense. Regardless of this fix, a robust SSRF guard must resolve the hostname and validate the *resolved* IP against the socket it connects to, and account for DNS rebinding and redirects. Treat these checks as one layer, not the only one.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-101911?s=github&n=ip-address&t=npm&vr=%3C%3D10.7.0"><img alt="medium 6.3: CVE--2026--101911" src="https://img.shields.io/badge/CVE--2026--101911-lightgrey?label=medium%206.3&labelColor=fbb552"/></a> <i>Uncontrolled Resource Consumption</i>

<table>
<tr><td>Affected range</td><td><code><=10.7.0</code></td></tr>
<tr><td>Fixed version</td><td><code>10.7.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:N/VC:N/VI:N/VA:L/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.383%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>33rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

`new Address6()` and `Address6.isValid()` place no bound on the length of the string they parse. When the string contains a character that cannot appear in an IPv6 address, the parser builds a diagnostic that wraps every such character in a 34-byte `<span class="parse-error">`, so the work and the memory scale with the input rather than with an address. A 1 MiB string of `!` costs about 110 MB and 70 ms of synchronous work, 8 MiB costs about 800 MB and half a second, 16 MiB throws a `RangeError` in place of the documented `AddressError`, and 32 MiB aborts the Node process. `isValid()` builds the diagnostic and discards it, so a caller that only asks whether a string is valid pays the full price.

An application that validates an attacker-supplied string with these methods can be stalled or crashed by a single oversized request. This is a crash on input that should have been rejected cleanly, which SECURITY.md lists as in scope.

### Details

`parse()` in `src/ipv6.ts` checks for characters outside `[0-9a-f:/%]` and, on finding any, throws an `AddressError` whose `parseMessage` is the whole input with each offending character wrapped:

```ts
const badCharacters = address.match(constants6.RE_BAD_CHARACTERS);

if (badCharacters) {
  throw new AddressError(
    `Bad character${badCharacters.length > 1 ? 's' : ''} detected in address: ${badCharacters.join('')}`,
    address.replace(constants6.RE_BAD_CHARACTERS, '<span class="parse-error">$1</span>'),
  );
}
```

`RE_BAD_CHARACTERS` is `/([^0-9a-f:/%])/gi`. For an input made entirely of punctuation the `match` allocates one string per character, the `join` copies them all into the message, and the `replace` produces a string 34 times the input. Nothing before this point looks at the length: the constructor strips a CIDR suffix and a zone identifier and hands the rest to `parse()`. The `RE_BAD_ADDRESS` branch below it builds its diagnostic the same way at about a third of the ratio, for input in the hex-and-colon alphabet such as `fffff:` repeated.

`parse()` is reached only through the constructor, so every entry point that constructs an `Address6` from a string it has not already bounded is affected: `new Address6()`, `isValid()`, both arguments of `fromAddressAndMask()` and `fromAddressAndWildcardMask()`, `fromWildcard()`, and the prefix argument of `fromAddress4Nat64()` and `toAddress4Nat64()`. `fromURL()` admits only hex, colons, and dots in a host, so it reaches the `RE_BAD_ADDRESS` branch and not the other. `fromArpa()` caps its input at 32 nibbles before constructing anything, and `fromBigInt()`, `fromByteArray()`, and `fromAddress4()` build the string themselves, so those are unaffected.

The `replace` is where size becomes fatal. V8 caps a string at 2^29 - 24 characters, so past 16 MiB of input the `replace` throws `RangeError: Invalid string length` rather than the `AddressError` callers catch; `isValid()` swallows it, but a constructor call guarded by `instanceof AddressError` does not. Past 32 MiB the replacement builder's internal array exceeds its maximum size and V8 aborts the process with `Fatal JavaScript invalid size error`, which no `try`/`catch` intercepts.

### Affected versions

`<= 10.7.0`. The diagnostic has had this shape since the parser was written, so every release is affected.

### Impact

`Address6.isValid()` on N bytes of `!`, measured on node 24.19.0:

| Input | Wall time | Transient heap | Outcome |
|---|---|---|---|
| 16 KiB | 1 ms | 1 MB | `false` |
| 1 MiB | 73 ms | 112 MB | `false` |
| 8 MiB | 464 ms | 784 MB | `false` |
| 16 MiB | | | `RangeError: Invalid string length` from the constructor; `isValid()` returns `false` |
| 32 MiB | | | the process aborts |

The parse is synchronous, so the event loop is blocked for the whole of the wall time and nothing else on that process is served. The heap is transient and is reclaimed after the call returns, so memory does not accumulate across requests; the abort at 32 MiB is a single request. `Address4` has no diagnostic of this shape and parses the same 8 MiB in a few milliseconds.

### Reachability

Reaching the sizes above requires that the application hand the parser a string it has not already bounded. A host taken from a URL or an HTTP header is bounded by the server's header limit (Node's default is 16 KB), and at that size the cost is a millisecond. The megabyte sizes need a request body the application accepts at that scale and passes through unchecked. Common body parsers default to between 100 KB and 1 MB, which caps the effect at a stall of under 100 ms per request, and the abort needs 32 MiB in a single field, which no default admits. The severity is scored for the stall, not the abort: an application that accepts 32 MiB bodies into an address parser is the exception, and the reader running one should treat this as a crash.

### Proof of concept

`npm i ip-address@<!-- -->10.7.0`, then:

```js
const { Address6 } = require('ip-address');

for (const mib of [1, 8]) {
  const input = '!'.repeat(mib * 1024 * 1024);
  const before = process.memoryUsage().heapUsed;
  const start = process.hrtime.bigint();

  Address6.isValid(input);

  const ms = Number(process.hrtime.bigint() - start) / 1e6;
  const mb = (process.memoryUsage().heapUsed - before) / 1048576;

  console.log(`${mib} MiB: ${ms.toFixed(0)} ms, ${mb.toFixed(0)} MB`);
}

try {
  new Address6('!'.repeat(16 * 1024 * 1024));
} catch (e) {
  console.log(`16 MiB: ${e.name}: ${e.message}`);
}

new Address6('!'.repeat(32 * 1024 * 1024));
```

On affected versions (node 24.19.0):

```
1 MiB: 73 ms, 112 MB
8 MiB: 464 ms, 784 MB
16 MiB: RangeError: Invalid string length


#
# Fatal error in , line 0
# Fatal JavaScript invalid size error 142606336
#
```

The last line is V8 terminating the process; the script does not reach its end.

### Remediation

Upgrade to the patched release. In the fix, the constructor rejects an address longer than the family allows before `parse()` runs: 45 characters for IPv6 once the CIDR suffix and zone identifier are stripped (six four-digit groups, six colons, and a dotted quad, the same line CPython's `ipaddress` module draws), and 15 characters for IPv4. The rejection is an `AddressError` with no `parseMessage`, so `isValid()` returns `false` for the cost of a length comparison and the 32 MiB input above is rejected in the same time as a 46-character one. A zone identifier is not counted, since it never reaches the diagnostic.

This rejects nothing a previous release accepted: every string longer than the limit already failed to parse.

If you cannot upgrade immediately, reject a candidate longer than an address with a zone identifier can be before you parse it:

```js
if (host.length > 64) throw new Error('not an IP address');
```

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-42338?s=github&n=ip-address&t=npm&vr=%3C%3D10.1.0"><img alt="medium 5.3: CVE--2026--42338" src="https://img.shields.io/badge/CVE--2026--42338-lightgrey?label=medium%205.3&labelColor=fbb552"/></a> <i>Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')</i>

<table>
<tr><td>Affected range</td><td><code><=10.1.0</code></td></tr>
<tr><td>Fixed version</td><td><code>10.1.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:N/PR:N/UI:P/VC:L/VI:L/VA:N/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.471%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>41st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

`Address6.group()` and `Address6.link()` do not HTML-escape attacker-controlled content before embedding it in the HTML strings they return, and `AddressError.parseMessage` (emitted by the `Address6` constructor for invalid input) can contain unescaped attacker-controlled content in one branch. An application that (1) passes untrusted input to `Address6` and (2) renders the output of these methods, or the thrown error's `parseMessage`, as HTML (e.g. via `innerHTML`) is vulnerable to cross-site scripting. A related issue in `v6.helpers.spanAll()` produced malformed markup but was not exploitable; it is hardened in the same release for consistency.

### Details

Four related issues were identified and fixed together:

1. **`Address6.group()`: zone ID injection.** The `Address6` constructor stores the raw input (including any IPv6 zone ID) in `this.address` before zone stripping. `group()` then passed `this.address` to `helpers.simpleGroup()`, which wrapped each `:`-separated segment in a `<span>` element without HTML-escaping the content. A zone ID containing HTML markup was embedded verbatim.
2. **`Address6.link({ prefix, className })`: attribute-value injection.** `link()` concatenated user-supplied `prefix` and `className` into the `href="…"` and `class="…"` attributes without escaping. A caller passing untrusted content through these options could inject event handlers (e.g. `onmouseover`) and achieve XSS.
3. **`Address6` constructor: leading-zero IPv4 error path.** The leading-zero branch in `parse4in6()` built `AddressError.parseMessage` by concatenating the raw address through `String.replace()`. Because `parse4in6()` runs before the bad-character check, any characters in the groups preceding the IPv4 suffix flowed into the error's HTML unescaped. Consumers who render `parseMessage` as HTML (its documented purpose — it already contains `<span class="parse-error">` markup) could be XSS'd by a crafted input such as `<img src=x onerror=alert(1)>:10.0.01.1`.
4. **`v6.helpers.spanAll()`: attribute-value injection (defense in depth).** `spanAll()` embedded each character of its input into a `class="digit value-${n} …"` attribute without escaping. Because `split('')` limits `n` to a single character this was not exploitable in practice, but it produced malformed markup and is fixed for consistency.

### Affected Versions

All versions up to and including `10.1.0`.

### Patched Version

`10.1.1`.

### Impact

Real-world exposure is believed to be extremely limited. Analysis of all 425 dependent npm packages as well as GitHub code search found zero consumers of `group()`, `link()`, or `spanAll()`: these HTML-emitting surfaces appear to be unused across published npm packages and public repositories. Applications using only the address-parsing and comparison APIs (`isValid`, `correctForm`, `isInSubnet`, `bigInt`, etc.) are not affected.

Consumers who **do** render the output of `group()`, `link()`, `spanAll()`, or `AddressError.parseMessage` as HTML against untrusted input should upgrade.

### PoC

```javascript
const { Address6 } = require('ip-address');
const addr = new Address6('fe80::1%<img src=x onerror=alert(1)>');
document.body.innerHTML = addr.group();  // fires the onerror handler in 10.1.0
```

### Workarounds

If users cannot upgrade immediately:

- Do not pass untrusted input to the `Address6` constructor, or
- Never render the output of `group()`, `link()`, or `spanAll()`, nor the `parseMessage` field of any thrown `AddressError`, as HTML; treat these values as text only, or run them through [DOMPurify](https://github.com/cure53/DOMPurify) before inserting into the DOM (DOMPurify's default configuration preserves the library's intended `<span>` wrapping while stripping any injected event handlers), or
- Validate input with `Address6.isValid()` and reject anything that contains a zone identifier (a `%` character) or characters outside `[0-9a-fA-F:/]` before passing it to the constructor.

### Lack of separate CVEs

Given the evidence that these methods are not used, and given that they are all of the same construction, maintainers do not think it's relevant or useful to create a separate CVE for each library method.

### Credit

ip-address thanks @<!-- -->scovetta for reporting this issue.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>picomatch</strong> <code>4.0.3</code> (npm)</summary>

<small><code>pkg:npm/picomatch@4.0.3</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-33671?s=github&n=picomatch&t=npm&vr=%3E%3D4.0.0%2C%3C4.0.4"><img alt="high 7.5: CVE--2026--33671" src="https://img.shields.io/badge/CVE--2026--33671-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Inefficient Regular Expression Complexity</i>

<table>
<tr><td>Affected range</td><td><code>>=4.0.0<br/><4.0.4</code></td></tr>
<tr><td>Fixed version</td><td><code>4.0.4</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N/A:H</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.429%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>38th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Impact
`picomatch` is vulnerable to Regular Expression Denial of Service (ReDoS) when processing crafted extglob patterns. Certain patterns using extglob quantifiers such as `+()` and `*()`, especially when combined with overlapping alternatives or nested extglobs, are compiled into regular expressions that can exhibit catastrophic backtracking on non-matching input.

Examples of problematic patterns include `+(a|aa)`, `+(*|?)`, `+(+(a))`, `*(+(a))`, and `+(+(+(a)))`. In local reproduction, these patterns caused multi-second event-loop blocking with relatively short inputs. For example, `+(a|aa)` compiled to `^(?:(?=.)(?:a|aa)+)$` and took about 2 seconds to reject a 41-character non-matching input, while nested patterns such as `+(+(a))` and `*(+(a))` took around 29 seconds to reject a 33-character input on a modern M1 MacBook.

Applications are impacted when they allow untrusted users to supply glob patterns that are passed to `picomatch` for compilation or matching. In those cases, an attacker can cause excessive CPU consumption and block the Node.js event loop, resulting in a denial of service. Applications that only use trusted, developer-controlled glob patterns are much less likely to be exposed in a security-relevant way.

### Patches
This issue is fixed in picomatch 4.0.4, 3.0.2 and 2.3.2.

Users should upgrade to one of these versions or later, depending on their supported release line.

### Workarounds
If upgrading is not immediately possible, avoid passing untrusted glob patterns to `picomatch`.

Possible mitigations include:
- disable extglob support for untrusted patterns by using `noextglob: true`
- reject or sanitize patterns containing nested extglobs or extglob quantifiers such as `+()` and `*()`
- enforce strict allowlists for accepted pattern syntax
- run matching in an isolated worker or separate process with time and resource limits
- apply application-level request throttling and input validation for any endpoint that accepts glob patterns

### Resources
- Picomatch repository: https://github.com/micromatch/picomatch
- `lib/parse.js` and `lib/constants.js` are involved in generating the vulnerable regex forms
- Comparable ReDoS precedent: CVE-2024-4067 (`micromatch`)
- Comparable generated-regex precedent: CVE-2024-45296 (`path-to-regexp`)

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-33672?s=github&n=picomatch&t=npm&vr=%3E%3D4.0.0%2C%3C4.0.4"><img alt="medium 5.3: CVE--2026--33672" src="https://img.shields.io/badge/CVE--2026--33672-lightgrey?label=medium%205.3&labelColor=fbb552"/></a> <i>Improperly Controlled Modification of Object Prototype Attributes ('Prototype Pollution')</i>

<table>
<tr><td>Affected range</td><td><code>>=4.0.0<br/><4.0.4</code></td></tr>
<tr><td>Fixed version</td><td><code>4.0.4</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.435%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>38th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Impact
picomatch is vulnerable to a **method injection vulnerability (CWE-1321)** affecting the `POSIX_REGEX_SOURCE` object. Because the object inherits from `Object.prototype`, specially crafted POSIX bracket expressions (e.g., `[[:constructor:]]`) can reference inherited method names. These methods are implicitly converted to strings and injected into the generated regular expression.

This leads to **incorrect glob matching behavior (integrity impact)**, where patterns may match unintended filenames. The issue does **not enable remote code execution**, but it can cause security-relevant logic errors in applications that rely on glob matching for filtering, validation, or access control.

All users of affected `picomatch` versions that process untrusted or user-controlled glob patterns are potentially impacted.

### Patches

This issue is fixed in picomatch 4.0.4, 3.0.2 and 2.3.2.

Users should upgrade to one of these versions or later, depending on their supported release line.

### Workarounds

If upgrading is not immediately possible, avoid passing untrusted glob patterns to picomatch.

Possible mitigations include:
- Sanitizing or rejecting untrusted glob patterns, especially those containing POSIX character classes like `[[:...:]]`.
- Avoiding the use of POSIX bracket expressions if user input is involved.
- Manually patching the library by modifying `POSIX_REGEX_SOURCE` to use a null prototype:

  ```js
  const POSIX_REGEX_SOURCE = {
    __proto__: null,
    alnum: 'a-zA-Z0-9',
    alpha: 'a-zA-Z',
    // ... rest unchanged
  };
  
### Resources

- fix for similar issue: https://github.com/micromatch/picomatch/pull/144
- picomatch repository https://github.com/micromatch/picomatch

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>musl</strong> <code>1.2.6-r3</code> (apk)</summary>

<small><code>pkg:apk/alpine/musl@1.2.6-r3?os_name=alpine&os_version=3.24</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-107891?s=alpine&n=musl&ns=alpine&t=apk&osn=alpine&osv=3.24&vr=%3C1.2.6-r6"><img alt="high : CVE--2026--107891" src="https://img.shields.io/badge/CVE--2026--107891-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.2.6-r6</code></td></tr>
<tr><td>Fixed version</td><td><code>1.2.6-r6</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.549%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>47th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>



</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>sigstore</strong> <code>3.1.0</code> (npm)</summary>

<small><code>pkg:npm/sigstore@3.1.0</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-48815?s=github&n=sigstore&t=npm&vr=%3C%3D4.1.0"><img alt="high 7.5: CVE--2026--48815" src="https://img.shields.io/badge/CVE--2026--48815-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Improper Verification of Cryptographic Signature</i>

<table>
<tr><td>Affected range</td><td><code><=4.1.0</code></td></tr>
<tr><td>Fixed version</td><td><code>4.1.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:H/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.173%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>7th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

The documented `certificateOIDs` option in `sigstore.verify()` is accepted by the public API but discarded before verification, so required certificate extension OIDs are never checked.

### Details

The public verify options include `certificateOIDs` and the documentation says those OID/value pairs “must be present in the certificate’s extension list.” The policy-construction path used by `sigstore.verify()` and `createVerifier()` only copies the SAN and issuer settings into the verification policy and completely ignores `certificateOIDs`.

As a result, callers can believe they are constraining verification to certificates carrying specific Fulcio or workload-identifying OIDs, while the actual verifier never receives those constraints. Any bundle that satisfies the remaining checks is accepted even if the required OID extensions are absent or mismatched.

This is reachable from supported usage through the documented `certificateOIDs` verify option.

### PoC

```javascript
const { createVerificationPolicy } = require("sigstore/dist/config");

const policy = createVerificationPolicy({
  certificateIssuer: "https://issuer.example",
  certificateIdentityEmail: "victim@<!-- -->example.com",
  certificateOIDs: {
    "1.2.3.4": "required-value",
  },
});

console.log("certificateOIDs" in policy, JSON.stringify(policy));
// false {"subjectAlternativeName":"victim@<!-- -->example.com","extensions":{"issuer":"https://issuer.example"}}
```

### Impact

Applications that rely on `certificateOIDs` to restrict which certificates may sign artifacts receive no such protection. Unauthorized certificates that should be rejected on extension policy can be accepted as long as they satisfy the remaining verification checks.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>pacote</strong> <code>20.0.1</code> (npm)</summary>

<small><code>pkg:npm/pacote@20.0.1</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-9496?s=github&n=pacote&t=npm&vr=%3E%3D11.2.7%2C%3C21.5.1"><img alt="high 7.7: CVE--2026--9496" src="https://img.shields.io/badge/CVE--2026--9496-lightgrey?label=high%207.7&labelColor=e25d68"/></a> <i>Inefficient Regular Expression Complexity</i>

<table>
<tr><td>Affected range</td><td><code>>=11.2.7<br/><21.5.1</code></td></tr>
<tr><td>Fixed version</td><td><code>21.5.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.7</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:N/PR:N/UI:N/VC:N/VI:N/VA:H/SC:N/SI:N/SA:N/E:P</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.346%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>29th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Versions of the package pacote from 11.2.7 are vulnerable to Denial of Service (DoS) via the addGitSha function. An attacker can exploit this vulnerability by supplying a specially crafted spec.rawSpec value that triggers the function’s regex replacement and string-manipulation logic, causing excessive CPU consumption and potentially stalling or crashing the process.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>pacote</strong> <code>19.0.2</code> (npm)</summary>

<small><code>pkg:npm/pacote@19.0.2</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-9496?s=github&n=pacote&t=npm&vr=%3E%3D11.2.7%2C%3C21.5.1"><img alt="high 7.7: CVE--2026--9496" src="https://img.shields.io/badge/CVE--2026--9496-lightgrey?label=high%207.7&labelColor=e25d68"/></a> <i>Inefficient Regular Expression Complexity</i>

<table>
<tr><td>Affected range</td><td><code>>=11.2.7<br/><21.5.1</code></td></tr>
<tr><td>Fixed version</td><td><code>21.5.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.7</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:N/PR:N/UI:N/VC:N/VI:N/VA:H/SC:N/SI:N/SA:N/E:P</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.346%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>29th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Versions of the package pacote from 11.2.7 are vulnerable to Denial of Service (DoS) via the addGitSha function. An attacker can exploit this vulnerability by supplying a specially crafted spec.rawSpec value that triggers the function’s regex replacement and string-manipulation logic, causing excessive CPU consumption and potentially stalling or crashing the process.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --><strong>postcss-selector-parser</strong> <code>7.1.1</code> (npm)</summary>

<small><code>pkg:npm/postcss-selector-parser@7.1.1</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-104844?s=github&n=postcss-selector-parser&t=npm&vr=%3E%3D7.0.0%2C%3C7.1.6"><img alt="medium 5.9: CVE--2026--104844" src="https://img.shields.io/badge/CVE--2026--104844-lightgrey?label=medium%205.9&labelColor=fbb552"/></a> <i>Uncontrolled Resource Consumption</i>

<table>
<tr><td>Affected range</td><td><code>>=7.0.0<br/><7.1.6</code></td></tr>
<tr><td>Fixed version</td><td><code>7.1.6</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.9</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:N/A:H</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.389%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>34th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Impact

`.` and `#` are not word delimiters in the tokenizer, so a flat selector such as
`.a.a.a...` reaches `splitWord()` as a single word token carrying n class or id
indexes. Three passes scanned those index arrays linearly for every index,
making the parse O(n^2) in the number of indexes rather than in input length:
`uniqs()`, the `indices.forEach` loop, and the Sass-interpolation filter.
Parsing a 400 KB flat selector took ~34 s on a modern laptop, fully occupying a
single thread. A benign selector of identical byte size parses in tens of
milliseconds, so the cost is driven by the index count, not the input size.
The nesting depth of such a selector is 0, so the `maxNestingDepth` guard added
in 7.1.3 offers no protection.

Reachability is deployment dependent. Only consumers that parse untrusted,
attacker-supplied selectors synchronously in a request path are exposed, for
example CSS sanitizers, CSS-in-JS services and online playgrounds. Ordinary
build-time use on trusted sources is not affected.

### Patches

Fixed in 7.1.6. The three passes now use Set membership tests, making parsing
linear in the number of indexes. There is no behaviour change: parsing is
byte-identical on a differential corpus of 8413 selectors.

### Workarounds

Cap the size of selectors accepted from untrusted sources before parsing.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-9358?s=github&n=postcss-selector-parser&t=npm&vr=%3E%3D7.1.0%2C%3C7.1.3"><img alt="low 2.1: CVE--2026--9358" src="https://img.shields.io/badge/CVE--2026--9358-lightgrey?label=low%202.1&labelColor=fce1a9"/></a> <i>Improper Resource Shutdown or Release</i>

<table>
<tr><td>Affected range</td><td><code>>=7.1.0<br/><7.1.3</code></td></tr>
<tr><td>Fixed version</td><td><code>7.1.3</code></td></tr>
<tr><td>CVSS Score</td><td><code>2.1</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:N/PR:N/UI:P/VC:N/VI:N/VA:L/SC:N/SI:N/SA:N/E:P</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.325%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>26th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A vulnerability was determined in postcss-selector-parser before 6.1.3 and 7.1.1. Affected is the function toString of the file src/selectors/container.js of the component AST Serialization. Executing a manipulation can lead to uncontrolled recursion. It is possible to launch the attack remotely. The exploit has been publicly disclosed and may be utilized. The vendor explains, that according to his definition "DoS on server-side on user-generated CSS is low risk for us (since most users compile own CSS with PostCSS)."

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>minimatch</strong> <code>9.0.9</code> (npm)</summary>

<small><code>pkg:npm/minimatch@9.0.9</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-118764?s=github&n=minimatch&t=npm&vr=%3E%3D7.0.0%2C%3C11.0.1"><img alt="medium 6.9: CVE--2026--118764" src="https://img.shields.io/badge/CVE--2026--118764-lightgrey?label=medium%206.9&labelColor=fbb552"/></a> <i>Asymmetric Resource Consumption (Amplification)</i>

<table>
<tr><td>Affected range</td><td><code>>=7.0.0<br/><11.0.1</code></td></tr>
<tr><td>Fixed version</td><td><code>11.0.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.9</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:N/PR:N/UI:N/VC:N/VI:N/VA:L/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.301%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>23rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

minimatch 10.2.6 contains an attacker-controlled pattern amplification in firstPhasePreProcess() when optimizationLevel >= 2.

researcher: Reid Downing (b1nv0id)
files: 

- src/index.ts: 690-770
- src/index.ts: 780-796

issue:
input-controlled growth of globParts during first-phase preprocessing, followed by quadratic second-phase processing.

the **/../ transformation clones a globparts entry and appends the clone to the same globparts array:
```
parts.splice(gs, 1)
const other = parts.slice(0)
other[gs] = '**'
globParts.push(other)
```
this occurs inside a do...while (didSomething) fixpoint loop, allowing generated entries to be processed again.

the expanded globparts array is subsequently processed by secondPhasePreProcess(), which performs pairwise comparisons:
```
for (let i = 0; i < globParts.length - 1; i++) {
  for (let j = i + 1; j < globParts.length; j++) {
    this.partsMatch(...)
  }
}
```
an attacker who can supply a glob pattern can therefore cause additional pattern entries to be generated during preprocessing, followed by quadratic pairwise processing, resulting in excessive cpu and memory consumption.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>glob</strong> <code>10.5.0</code> (npm)</summary>

<small><code>pkg:npm/glob@10.5.0</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-118773?s=github&n=glob&t=npm&vr=%3E%3D9.0.0%2C%3C%3D14.0.1"><img alt="medium 6.3: CVE--2026--118773" src="https://img.shields.io/badge/CVE--2026--118773-lightgrey?label=medium%206.3&labelColor=fbb552"/></a> <i>Uncontrolled Resource Consumption</i>

<table>
<tr><td>Affected range</td><td><code>>=9.0.0<br/><=14.0.1</code></td></tr>
<tr><td>Fixed version</td><td><code>14.0.2</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:N/VC:N/VI:N/VA:L/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.350%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>29th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

In glob 13.0.6, an aborted async walk rejects or emits an error but continues recursively reading directories in the background.

The root cause is that abort branches in src/walker.ts call cb() without returning. As a result, callers that rely on signal or AbortSignal.timeout() to bound glob traversal cost can still incur filesystem I/O and CPU work after the request has already been rejected.

### Details

This was reproduced on glob v13.0.6 (commit e80cb38ae60d6cbff9e75f39032a994858994d35).

The README documents that the signal option cancels the glob walk. However, in src/walker.ts, the following methods call cb() when this.signal?.aborted is true but do not return:

- GlobUtil.walkCB()
- GlobUtil.walkCB2()
- GlobUtil.walkCBSync()
- GlobUtil.walkCB2Sync()

Example vulnerable pattern:

if (this.signal?.aborted) cb()

Because execution continues after cb(), the walker still reaches processor.processPatterns(), readdirCB(), and recursive walkCB2() calls.

The issue was directly demonstrated against v13.0.6. A source-history review shows the same missing-return pattern is present in tagged releases from v9.0.0 through v13.0.6.

The issue affects both glob() and globStream().

Recommended fix:
Change each abort branch to return immediately:

if (this.signal?.aborted) return cb()

### Proof of concept

Environment:
- Linux x86_64
- Node.js v22.23.3
- npm 10.9.9
- glob 13.0.6

Reproduction steps:

1. Install the affected package:
   npm init -y
   npm install glob@<!-- -->13.0.6

2. Run the attached PoC:
   node poc/abort-continues-work.mjs

The PoC aborts after the first readdir() call, waits briefly, and counts how many more directory reads happen after the promise has already rejected.

Observed output on the vulnerable version:

{
  "rejection": "Error: probe-abort",
  "readdirCalls": 1365,
  "readdirCallsAtReject": 5,
  "readdirCallsAfterReject": 1360
}

Expected behavior:
readdirCallsAfterReject should be 0.

A second PoC using AbortSignal.timeout() also reproduces the issue:

{
  "rejection": "TimeoutError: The operation was aborted due to timeout",
  "readdirCalls": 133,
  "readdirCallsAtReject": 1,
  "readdirCallsAfterReject": 132
}

The same test against a patched build with return cb() in the four abort branches stops immediately:

{
  "readdirCalls": 1,
  "readdirCallsAtReject": 1,
  "readdirCallsAfterReject": 0
}

### Impact

This is an availability issue.

Applications that expose globbing over attacker-influenced patterns or attacker-controlled directory trees and use AbortSignal / AbortSignal.timeout() as a traversal budget can still perform significant filesystem I/O and CPU work after a request has already timed out or been canceled.

Repeated timed-out requests can stack background glob walks and degrade worker throughput or service availability.

No confidentiality or integrity impact was observed.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>@sigstore/core</strong> <code>2.0.0</code> (npm)</summary>

<small><code>pkg:npm/%40sigstore/core@2.0.0</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-48758?s=github&n=core&ns=%40sigstore&t=npm&vr=%3C%3D3.2.0"><img alt="medium 5.4: CVE--2026--48758" src="https://img.shields.io/badge/CVE--2026--48758-lightgrey?label=medium%205.4&labelColor=fbb552"/></a> <i>Improper Verification of Cryptographic Signature</i>

<table>
<tr><td>Affected range</td><td><code><=3.2.0</code></td></tr>
<tr><td>Fixed version</td><td><code>3.2.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.4</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:L/UI:N/S:U/C:N/I:L/A:L</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.239%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>15th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Impact
The `preAuthEncoding` function in `@<!-- -->sigstore/core` uses Node.js `'ascii'` encoding when converting the PAE (Pre-Authentication Encoding) string to bytes. This allows `payloadType` to be mutated after signing without invalidating the signature, breaking the type-binding guarantee that DSSE is designed to provide.

In `packages/core/src/dsse.ts`, the PAE function builds a string containing `payloadType` and then encodes it with `Buffer.from(prefix, 'ascii')`.

In Node.js, `'ascii'` encoding for string-to-Buffer is equivalent to `'latin1'`, which **truncates characters above U+00FF to their low byte**. This means for any ASCII character, there exist Unicode characters (at U+01xx, U+02xx, etc.) that produce the identical encoded byte:

| Original | Codepoint | Mutant | Codepoint | Encoded byte |
|----------|-----------|--------|-----------|--------------|
| `t`      | U+0074    | `Ŵ`    | U+0174    | `0x74`       |
| `e`      | U+0065    | `ť`    | U+0165    | `0x65`       |

An attacker can substitute every character in `payloadType` with a Unicode variant whose low byte matches, producing **identical PAE bytes** and a passing signature verification.

Additionally, `payloadType.length` returns the JavaScript string length (UTF-16 code units) rather than the UTF-8 byte length required by the DSSE spec, though this is only a contributing factor for non-ASCII types.

#### Reproduction

```javascript
const { preAuthEncoding } = require('@<!-- -->sigstore/core/dist/dsse.js');
const payload = Buffer.from('hello world');

const original = preAuthEncoding('text/plain', payload);
// U+01xx chars whose low bytes match the original ASCII chars
const mutant = preAuthEncoding('\u0174\u0165\u0178\u0174/\u0170\u016c\u0161\u0169\u016e', payload);

console.log('PAE bytes equal:', original.equals(mutant)); // true — should be false
```

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <img alt="unspecified: 5" src="https://img.shields.io/badge/U-5-lightgrey"/><strong>openssl</strong> <code>3.5.9-r0</code> (apk)</summary>

<small><code>pkg:apk/alpine/openssl@3.5.9-r0?os_name=alpine&os_version=3.24</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-95692?s=alpine&n=openssl&ns=alpine&t=apk&osn=alpine&osv=3.24&vr=%3C3.5.9-r1"><img alt="unspecified : CVE--2026--95692" src="https://img.shields.io/badge/CVE--2026--95692-lightgrey?label=unspecified%20&labelColor=lightgrey"/></a> 

<table>
<tr><td>Affected range</td><td><code><3.5.9-r1</code></td></tr>
<tr><td>Fixed version</td><td><code>3.5.9-r1</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.211%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>11th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>



</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-95691?s=alpine&n=openssl&ns=alpine&t=apk&osn=alpine&osv=3.24&vr=%3C3.5.9-r1"><img alt="unspecified : CVE--2026--95691" src="https://img.shields.io/badge/CVE--2026--95691-lightgrey?label=unspecified%20&labelColor=lightgrey"/></a> 

<table>
<tr><td>Affected range</td><td><code><3.5.9-r1</code></td></tr>
<tr><td>Fixed version</td><td><code>3.5.9-r1</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.190%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>9th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>



</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-88823?s=alpine&n=openssl&ns=alpine&t=apk&osn=alpine&osv=3.24&vr=%3C3.5.9-r1"><img alt="unspecified : CVE--2026--88823" src="https://img.shields.io/badge/CVE--2026--88823-lightgrey?label=unspecified%20&labelColor=lightgrey"/></a> 

<table>
<tr><td>Affected range</td><td><code><3.5.9-r1</code></td></tr>
<tr><td>Fixed version</td><td><code>3.5.9-r1</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.142%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>4th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>



</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-88822?s=alpine&n=openssl&ns=alpine&t=apk&osn=alpine&osv=3.24&vr=%3C3.5.9-r1"><img alt="unspecified : CVE--2026--88822" src="https://img.shields.io/badge/CVE--2026--88822-lightgrey?label=unspecified%20&labelColor=lightgrey"/></a> 

<table>
<tr><td>Affected range</td><td><code><3.5.9-r1</code></td></tr>
<tr><td>Fixed version</td><td><code>3.5.9-r1</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.190%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>9th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>



</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-107496?s=alpine&n=openssl&ns=alpine&t=apk&osn=alpine&osv=3.24&vr=%3C3.5.9-r1"><img alt="unspecified : CVE--2026--107496" src="https://img.shields.io/badge/CVE--2026--107496-lightgrey?label=unspecified%20&labelColor=lightgrey"/></a> 

<table>
<tr><td>Affected range</td><td><code><3.5.9-r1</code></td></tr>
<tr><td>Fixed version</td><td><code>3.5.9-r1</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.127%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>2nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>



</blockquote>
</details>
</details></td></tr>
</table>

