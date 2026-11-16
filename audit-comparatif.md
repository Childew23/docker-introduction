
## Overview

| Image reference | `quiz-docker:initial`        | `quiz-docker:secure`        |
|-----------------|---------------------------|---------------------------|
| - digest        | `0626f6547f25` | `17bd0ca35790` |
| - tag           | `initial` | `secure` |
| - vulnerabilities | <img alt="critical: 1" src="https://img.shields.io/badge/critical-1-8b1924"/> <img alt="high: 11" src="https://img.shields.io/badge/high-11-e25d68"/> <img alt="medium: 12" src="https://img.shields.io/badge/medium-12-fbb552"/> <img alt="low: 1" src="https://img.shields.io/badge/low-1-fce1a9"/> <img alt="unspecified: 5" src="https://img.shields.io/badge/unspecified-5-lightgrey"/> | <img alt="critical: 6" src="https://img.shields.io/badge/critical-6-8b1924"/> <img alt="high: 63" src="https://img.shields.io/badge/high-63-e25d68"/> <img alt="medium: 80" src="https://img.shields.io/badge/medium-80-fbb552"/> <img alt="low: 47" src="https://img.shields.io/badge/low-47-fce1a9"/> <img alt="unspecified: 2" src="https://img.shields.io/badge/unspecified-2-lightgrey"/> |
| - platform | linux/amd64 | linux/amd64 |
| - size | 72 MB | 88 MB (+16 MB) |
| - packages | 266 | 356 (+90) |
| **Base Image** | `node:22-alpine`<br/>also known as:<br/>• <code>22-alpine3.24</code><br/>• <code>22.23-alpine</code><br/>• <code>22.23-alpine3.24</code><br/>• <code>22.23.5-alpine</code><br/>• <code>22.23.5-alpine3.24</code><br/>• <code>jod-alpine</code><br/>• <code>jod-alpine3.24</code> | `node:24-bookworm-slim`<br/>also known as:<br/>• <code>24-slim</code><br/>• <code>24.22-bookworm-slim</code><br/>• <code>24.22-slim</code><br/>• <code>24.22.3-bookworm-slim</code><br/>• <code>24.22.3-slim</code><br/>• <code>krypton-bookworm-slim</code><br/>• <code>krypton-slim</code> |
| - vulnerabilities | <img alt="critical: 1" src="https://img.shields.io/badge/critical-1-8b1924"/> <img alt="high: 10" src="https://img.shields.io/badge/high-10-e25d68"/> <img alt="medium: 12" src="https://img.shields.io/badge/medium-12-fbb552"/> <img alt="low: 1" src="https://img.shields.io/badge/low-1-fce1a9"/> <img alt="unspecified: 5" src="https://img.shields.io/badge/unspecified-5-lightgrey"/> | <img alt="critical: 0" src="https://img.shields.io/badge/critical-0-lightgrey"/> <img alt="high: 13" src="https://img.shields.io/badge/high-13-e25d68"/> <img alt="medium: 17" src="https://img.shields.io/badge/medium-17-fbb552"/> <img alt="low: 41" src="https://img.shields.io/badge/low-41-fce1a9"/> <!-- unspecified: 0 --> |

<details><summary><strong>Environment Variables</strong> (2 changes)</summary>

> * `+` 1 added
> * `±` 1 changed
> * _2 unchanged_


```diff
+NODE_ENV=production
-NODE_VERSION=22.23.5
+NODE_VERSION=24.22.3
 PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
 YARN_VERSION=1.22.22
```


</details>



<details><summary><strong>Config</strong> (2 changes)</summary>

> * `±` 2 changed
> * _3 unchanged_


```diff
 3000/tcp=
-cmd=serve -s dist
+cmd=serve -s dist -l 3000
 entrypoint=docker-entrypoint.sh
-user=
+user=node
 workdir=/app
```


</details>

<details ><summary><strong>Policies</strong> (1 improved, 3 worsened)</summary>

**Health score:** `quiz-docker:initial` D (50%) → `quiz-docker:secure` D (33%)

| Policy Name | `quiz-docker:initial` | `quiz-docker:secure` | Change | Standing |
|-------------|---------------|--------------------|--------|---|
|Default non-root user | :warning: | :white_check_mark: | -1 | Improved |
|No copyleft licenses | :warning: 20 | :warning: 335 | +315 | Worsened |
|No fixable critical or high vulnerabilities | :warning: 12 | :warning: 62 | +50 | Worsened |
|No high-profile vulnerabilities | :white_check_mark: | :warning: 2 | +2 | Worsened |
|No outdated base images | :white_check_mark: | :white_check_mark: |  | No Change |
|No unapproved base images | :white_check_mark: | :white_check_mark: |  | No Change |
|Supply chain attestations | :warning: 2 | :warning: 2 |  | No Change |

</details>


<details><summary><strong>Packages and Vulnerabilities</strong> (283 package changes and 208 vulnerability changes)</summary>

> * :heavy_plus_sign: 141 packages added
> * :heavy_minus_sign: 47 packages removed
> * :infinity: 95 packages changed
> * 100 packages unchanged


> * :heavy_exclamation_mark: 188 vulnerabilities added
> * :heavy_check_mark: 20 vulnerabilities removed
<details><summary>Changes for packages of type <code>apk</code> (24 changes)</summary>
<table>
	<tr>
		<th></th>
		<th valign="top">Package</th>
		<th valign="top">Version<br/><code>quiz-docker:initial</code></th>
		<th valign="top">Version<br/><code>quiz-docker:secure</code></th>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>alpine-base</strong></td>
		<td valign="top"><code>3.24.4-r0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>alpine-baselayout</strong></td>
		<td valign="top"><code>3.7.2-r1</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>alpine-baselayout-data</strong></td>
		<td valign="top"><code>3.7.2-r1</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>alpine-keys</strong></td>
		<td valign="top"><code>2.6-r0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>alpine-release</strong></td>
		<td valign="top"><code>3.24.4-r0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>apk-tools</strong></td>
		<td valign="top"><code>3.0.9-r0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>busybox</strong></td>
		<td valign="top"><code>1.37.0-r31</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>busybox-binsh</strong></td>
		<td valign="top"><code>1.37.0-r31</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>ca-certificates</strong></td>
		<td valign="top"><code>20261020-r0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>ca-certificates-bundle</strong></td>
		<td valign="top"><code>20261020-r0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>gcc</strong></td>
		<td valign="top"><code>15.2.0-r5</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>libapk</strong></td>
		<td valign="top"><code>3.0.9-r0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>libatomic</strong></td>
		<td valign="top"><code>15.2.0-r5</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>libcrypto3</strong></td>
		<td valign="top"><code>3.5.9-r0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>libgcc</strong></td>
		<td valign="top"><code>15.2.0-r5</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>libssl3</strong></td>
		<td valign="top"><code>3.5.9-r0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>libstdc++</strong></td>
		<td valign="top"><code>15.2.0-r5</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>musl</strong></td>
		<td valign="top"><code>1.2.6-r3</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
		<td valign="top"></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"><strong>Removed vulnerabilities (1):</strong><br/><ul><li><img alt="high : CVE--2026--107891" src="https://img.shields.io/badge/CVE--2026--107891-lightgrey?label=high%20&labelColor=e25d68"/></li></ul></td>
		<td valign="top"></td>
	</tr><tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>musl-utils</strong></td>
		<td valign="top"><code>1.2.6-r3</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>openssl</strong></td>
		<td valign="top"><code>3.5.9-r0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <img alt="unspecified: 5" src="https://img.shields.io/badge/U-5-lightgrey"/></td>
		<td valign="top"></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"><strong>Removed vulnerabilities (5):</strong><br/><ul><li><img alt="unspecified : CVE--2026--95692" src="https://img.shields.io/badge/CVE--2026--95692-lightgrey?label=unspecified%20&labelColor=lightgrey"/></li><li><img alt="unspecified : CVE--2026--95691" src="https://img.shields.io/badge/CVE--2026--95691-lightgrey?label=unspecified%20&labelColor=lightgrey"/></li><li><img alt="unspecified : CVE--2026--88823" src="https://img.shields.io/badge/CVE--2026--88823-lightgrey?label=unspecified%20&labelColor=lightgrey"/></li><li><img alt="unspecified : CVE--2026--88822" src="https://img.shields.io/badge/CVE--2026--88822-lightgrey?label=unspecified%20&labelColor=lightgrey"/></li><li><img alt="unspecified : CVE--2026--107496" src="https://img.shields.io/badge/CVE--2026--107496-lightgrey?label=unspecified%20&labelColor=lightgrey"/></li></ul></td>
		<td valign="top"></td>
	</tr><tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>pax-utils</strong></td>
		<td valign="top"><code>1.3.9-r1</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>scanelf</strong></td>
		<td valign="top"><code>1.3.9-r1</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>ssl_client</strong></td>
		<td valign="top"><code>1.37.0-r31</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>zlib</strong></td>
		<td valign="top"><code>1.3.2-r1</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"><img alt="critical: 1" src="https://img.shields.io/badge/C-1-8b1924"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
		<td valign="top"></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"><strong>Removed vulnerabilities (1):</strong><br/><ul><li><img alt="critical : CVE--2026--4738" src="https://img.shields.io/badge/CVE--2026--4738-lightgrey?label=critical%20&labelColor=8b1924"/></li></ul></td>
		<td valign="top"></td>
	</tr>
</table>
</details>
<details><summary>Changes for packages of type <code>deb</code> (125 changes)</summary>
<table>
	<tr>
		<th></th>
		<th valign="top">Package</th>
		<th valign="top">Version<br/><code>quiz-docker:initial</code></th>
		<th valign="top">Version<br/><code>quiz-docker:secure</code></th>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>acl</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.3.1-3</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>adduser</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.134</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>apt</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.6.2</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (1):</strong><br/><ul><li><img alt="low : CVE--2011--3374" src="https://img.shields.io/badge/CVE--2011--3374-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>attr</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1:2.5.1-4</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>audit</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1:3.0.9-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>base-files</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>12.4+deb12u15</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>base-passwd</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.6.1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>bash</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>5.2.15-2+b13</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>bsdutils</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1:2.38.1-5+deb12u3</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>bzip2</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.0.8-5</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>cdebconf</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>0.270</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>coreutils</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>9.1-1</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 4" src="https://img.shields.io/badge/L-4-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (4):</strong><br/><ul><li><img alt="low : CVE--2026--56392" src="https://img.shields.io/badge/CVE--2026--56392-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2026--56391" src="https://img.shields.io/badge/CVE--2026--56391-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2025--5278" src="https://img.shields.io/badge/CVE--2025--5278-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2017--18018" src="https://img.shields.io/badge/CVE--2017--18018-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>dash</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>0.5.12-2</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 2" src="https://img.shields.io/badge/L-2-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (2):</strong><br/><ul><li><img alt="low : CVE--2026--102474" src="https://img.shields.io/badge/CVE--2026--102474-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2026--102473" src="https://img.shields.io/badge/CVE--2026--102473-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>db5.3</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>5.3.28+dfsg2-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>debconf</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.5.82</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>debian-archive-keyring</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2023.3+deb12u2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>debianutils</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>5.7-0.5~deb12u1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>diffutils</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1:3.8-4</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (1):</strong><br/><ul><li><img alt="low : CVE--2026--53910" src="https://img.shields.io/badge/CVE--2026--53910-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>dpkg</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.21.23</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>e2fsprogs</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.47.0-2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>findutils</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>4.9.0-4</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>gcc-12</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>12.2.0-14+deb12u1</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 2" src="https://img.shields.io/badge/L-2-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (2):</strong><br/><ul><li><img alt="low : CVE--2026--115456" src="https://img.shields.io/badge/CVE--2026--115456-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2022--27943" src="https://img.shields.io/badge/CVE--2022--27943-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>gcc-12-base</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>12.2.0-14+deb12u1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>glibc</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.36-9+deb12u14</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 2" src="https://img.shields.io/badge/M-2-fbb552"/> <img alt="low: 10" src="https://img.shields.io/badge/L-10-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (13):</strong><br/><ul><li><img alt="high : CVE--2026--84243" src="https://img.shields.io/badge/CVE--2026--84243-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="medium : CVE--2026--86805" src="https://img.shields.io/badge/CVE--2026--86805-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--115819" src="https://img.shields.io/badge/CVE--2026--115819-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="low : CVE--2026--97399" src="https://img.shields.io/badge/CVE--2026--97399-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2026--100290" src="https://img.shields.io/badge/CVE--2026--100290-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2026--95818" src="https://img.shields.io/badge/CVE--2026--95818-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2019--9192" src="https://img.shields.io/badge/CVE--2019--9192-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2019--1010025" src="https://img.shields.io/badge/CVE--2019--1010025-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2019--1010024" src="https://img.shields.io/badge/CVE--2019--1010024-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2019--1010023" src="https://img.shields.io/badge/CVE--2019--1010023-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2019--1010022" src="https://img.shields.io/badge/CVE--2019--1010022-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2018--20796" src="https://img.shields.io/badge/CVE--2018--20796-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2010--4756" src="https://img.shields.io/badge/CVE--2010--4756-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>gmp</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2:6.2.1+dfsg1-1.1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>gnupg2</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.2.40-1.1+deb12u2</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (1):</strong><br/><ul><li><img alt="low : CVE--2022--3219" src="https://img.shields.io/badge/CVE--2022--3219-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>gnutls28</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.7.9-2+deb12u7</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 7" src="https://img.shields.io/badge/L-7-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (7):</strong><br/><ul><li><img alt="low : CVE--2026--95210" src="https://img.shields.io/badge/CVE--2026--95210-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2026--95209" src="https://img.shields.io/badge/CVE--2026--95209-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2026--95184" src="https://img.shields.io/badge/CVE--2026--95184-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2026--88648" src="https://img.shields.io/badge/CVE--2026--88648-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2026--88647" src="https://img.shields.io/badge/CVE--2026--88647-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2026--67693" src="https://img.shields.io/badge/CVE--2026--67693-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2011--3389" src="https://img.shields.io/badge/CVE--2011--3389-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>gpgv</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.2.40-1.1+deb12u2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>grep</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.8-5</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>gzip</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.12-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>hostname</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.23+nmu1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>init-system-helpers</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.65.2+deb12u1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libacl1</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.3.1-3</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libapt-pkg6.0</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.6.2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libattr1</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1:2.5.1-4</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libaudit-common</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1:3.0.9-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libaudit1</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1:3.0.9-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libblkid1</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.38.1-5+deb12u3</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libbz2-1.0</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.0.8-5+b1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libc-bin</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.36-9+deb12u14</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libc6</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.36-9+deb12u14</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libcap-ng</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>0.8.3-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libcap-ng0</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>0.8.3-1+b3</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libcap2</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1:2.66-4+deb12u3+b1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libcom-err2</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.47.0-2+b2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libcrypt1</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1:4.4.33-2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libdb5.3</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>5.3.28+dfsg2-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libdebconfclient0</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>0.270</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libext2fs2</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.47.0-2+b2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libffi</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.4.4-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libffi8</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.4.4-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libgcc-s1</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>12.2.0-14+deb12u1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libgcrypt20</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.10.1-3+deb12u1</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 2" src="https://img.shields.io/badge/L-2-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (2):</strong><br/><ul><li><img alt="low : CVE--2024--2236" src="https://img.shields.io/badge/CVE--2024--2236-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2018--6829" src="https://img.shields.io/badge/CVE--2018--6829-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libgmp10</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2:6.2.1+dfsg1-1.1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libgnutls30</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.7.9-2+deb12u7</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libgpg-error</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.46-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libgpg-error0</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.46-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libhogweed6</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.8.1-2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libidn2</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.3.3-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libidn2-0</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.3.3-1+b1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>liblz4-1</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.9.4-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>liblzma5</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>5.4.1-1+deb12u2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libmd</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.0.4-2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libmd0</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.0.4-2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libmount1</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.38.1-5+deb12u3</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libnettle8</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.8.1-2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libp11-kit0</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>0.24.1-2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libpam-modules</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.5.2-6+deb12u2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libpam-modules-bin</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.5.2-6+deb12u2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libpam-runtime</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.5.2-6+deb12u2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libpam0g</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.5.2-6+deb12u2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libpcre2-8-0</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>10.42-1+deb12u2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libseccomp</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.5.4-1+deb12u1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libseccomp2</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.5.4-1+deb12u1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libselinux</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.4-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libselinux1</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.4-1+b6</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libsemanage</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.4-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libsemanage-common</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.4-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libsemanage2</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.4-1+b5</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libsepol</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.4-2.1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libsepol2</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.4-2.1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libsmartcols1</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.38.1-5+deb12u3</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libss2</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.47.0-2+b2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libstdc++6</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>12.2.0-14+deb12u1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libsystemd0</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>252.39-1~deb12u2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libtasn1-6</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>4.19.0-2+deb12u1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libtinfo6</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>6.4-4</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libudev1</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>252.39-1~deb12u2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libunistring</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.0-2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libunistring2</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.0-2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libuuid1</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.38.1-5+deb12u3</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libxcrypt</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1:4.4.33-2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libxxhash0</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>0.8.1-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libzstd</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.5.4+dfsg2-5</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>libzstd1</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.5.4+dfsg2-5</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>login</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1:4.13+dfsg1-1+deb12u2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>logsave</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.47.0-2+b2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>lz4</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.9.4-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>mawk</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.3.4.20200120-3.1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>mount</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.38.1-5+deb12u3</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>ncurses</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>6.4-4</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>ncurses-base</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>6.4-4</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>ncurses-bin</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>6.4-4</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>nettle</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.8.1-2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>p11-kit</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>0.24.1-2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>pam</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.5.2-6+deb12u2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>passwd</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1:4.13+dfsg1-1+deb12u2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>pcre2</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>10.42-1+deb12u2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>perl</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>5.36.0-7+deb12u4</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 2" src="https://img.shields.io/badge/L-2-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (4):</strong><br/><ul><li><img alt="high : CVE--2026--82560" src="https://img.shields.io/badge/CVE--2026--82560-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="medium : CVE--2026--15534" src="https://img.shields.io/badge/CVE--2026--15534-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="low : CVE--2023--31486" src="https://img.shields.io/badge/CVE--2023--31486-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2011--4116" src="https://img.shields.io/badge/CVE--2011--4116-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>perl-base</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>5.36.0-7+deb12u4</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>sed</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>4.9-1+deb12u1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>shadow</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1:4.13+dfsg1-1+deb12u2</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (1):</strong><br/><ul><li><img alt="low : CVE--2007--5686" src="https://img.shields.io/badge/CVE--2007--5686-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>systemd</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>252.39-1~deb12u2</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 4" src="https://img.shields.io/badge/L-4-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (4):</strong><br/><ul><li><img alt="low : CVE--2023--31439" src="https://img.shields.io/badge/CVE--2023--31439-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2023--31438" src="https://img.shields.io/badge/CVE--2023--31438-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2023--31437" src="https://img.shields.io/badge/CVE--2023--31437-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2013--4392" src="https://img.shields.io/badge/CVE--2013--4392-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>sysvinit</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.06-4</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>sysvinit-utils</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.06-4</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>tar</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.34+dfsg-1.2+deb12u1</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (2):</strong><br/><ul><li><img alt="medium : CVE--2025--45582" src="https://img.shields.io/badge/CVE--2025--45582-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="low : CVE--2005--2541" src="https://img.shields.io/badge/CVE--2005--2541-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>tzdata</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2026f-0+deb12u1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>usr-is-merged</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>37~deb12u1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>usrmerge</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>37~deb12u1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>util-linux</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.38.1-5+deb12u3</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 3" src="https://img.shields.io/badge/H-3-e25d68"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 2" src="https://img.shields.io/badge/L-2-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (6):</strong><br/><ul><li><img alt="high : CVE--2026--53615" src="https://img.shields.io/badge/CVE--2026--53615-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--78410" src="https://img.shields.io/badge/CVE--2026--78410-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--53613" src="https://img.shields.io/badge/CVE--2026--53613-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="medium : CVE--2026--13595" src="https://img.shields.io/badge/CVE--2026--13595-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="low : CVE--2025--14104" src="https://img.shields.io/badge/CVE--2025--14104-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2022--0563" src="https://img.shields.io/badge/CVE--2022--0563-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>util-linux-extra</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.38.1-5+deb12u3</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>xxhash</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>0.8.1-1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>xz-utils</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>5.4.1-1+deb12u2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>zlib</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1:1.2.13.dfsg-1</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 2" src="https://img.shields.io/badge/H-2-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (2):</strong><br/><ul><li><img alt="high : CVE--2026--85091" src="https://img.shields.io/badge/CVE--2026--85091-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--76844" src="https://img.shields.io/badge/CVE--2026--76844-lightgrey?label=high%20&labelColor=e25d68"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>zlib1g</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1:1.2.13.dfsg-1</code></td>
	</tr>
	
</table>
</details>
<details><summary>Changes for packages of type <code>generic</code> (3 changes)</summary>
<table>
	<tr>
		<th></th>
		<th valign="top">Package</th>
		<th valign="top">Version<br/><code>quiz-docker:initial</code></th>
		<th valign="top">Version<br/><code>quiz-docker:secure</code></th>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>bash</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>5.2.15</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>gzip</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.12</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>util-linux</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>2.38.1</code></td>
	</tr>
	
</table>
</details>
<details><summary>Changes for packages of type <code>github</code> (1 changes)</summary>
<table>
	<tr>
		<th></th>
		<th valign="top">Package</th>
		<th valign="top">Version<br/><code>quiz-docker:initial</code></th>
		<th valign="top">Version<br/><code>quiz-docker:secure</code></th>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>node</strong></td>
		<td valign="top"><code>22.23.5</code></td>
		<td valign="top"><code>24.22.3</code></td>
	</tr>
	
</table>
</details>
<details><summary>Changes for packages of type <code>golang</code> (3 changes)</summary>
<table>
	<tr>
		<th></th>
		<th valign="top">Package</th>
		<th valign="top">Version<br/><code>quiz-docker:initial</code></th>
		<th valign="top">Version<br/><code>quiz-docker:secure</code></th>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>github.com/evanw/esbuild</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>UNKNOWN</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>golang.org/x/sys</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>0.0.0-20220715151400-c0bba94af5f8</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (1):</strong><br/><ul><li><img alt="low : CVE--2026--39824" src="https://img.shields.io/badge/CVE--2026--39824-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>stdlib</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.20.7</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 6" src="https://img.shields.io/badge/C-6-8b1924"/> <img alt="high: 39" src="https://img.shields.io/badge/H-39-e25d68"/> <img alt="medium: 41" src="https://img.shields.io/badge/M-41-fbb552"/> <img alt="low: 2" src="https://img.shields.io/badge/L-2-fce1a9"/> <img alt="unspecified: 1" src="https://img.shields.io/badge/U-1-lightgrey"/></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (89):</strong><br/><ul><li><img alt="critical : CVE--2025--68121" src="https://img.shields.io/badge/CVE--2025--68121-lightgrey?label=critical%20&labelColor=8b1924"/></li><li><img alt="critical : CVE--2026--56857" src="https://img.shields.io/badge/CVE--2026--56857-lightgrey?label=critical%20&labelColor=8b1924"/></li><li><img alt="critical : CVE--2024--24790" src="https://img.shields.io/badge/CVE--2024--24790-lightgrey?label=critical%20&labelColor=8b1924"/></li><li><img alt="critical : CVE--2026--39821" src="https://img.shields.io/badge/CVE--2026--39821-lightgrey?label=critical%20&labelColor=8b1924"/></li><li><img alt="critical : CVE--2026--78663" src="https://img.shields.io/badge/CVE--2026--78663-lightgrey?label=critical%20&labelColor=8b1924"/></li><li><img alt="critical : CVE--2025--22871" src="https://img.shields.io/badge/CVE--2025--22871-lightgrey?label=critical%20&labelColor=8b1924"/></li><li><img alt="high : CVE--2026--39822" src="https://img.shields.io/badge/CVE--2026--39822-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--97032" src="https://img.shields.io/badge/CVE--2026--97032-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--97031" src="https://img.shields.io/badge/CVE--2026--97031-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--94440" src="https://img.shields.io/badge/CVE--2026--94440-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--94439" src="https://img.shields.io/badge/CVE--2026--94439-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--78669" src="https://img.shields.io/badge/CVE--2026--78669-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--78667" src="https://img.shields.io/badge/CVE--2026--78667-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--78660" src="https://img.shields.io/badge/CVE--2026--78660-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--78659" src="https://img.shields.io/badge/CVE--2026--78659-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--56866" src="https://img.shields.io/badge/CVE--2026--56866-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--56862" src="https://img.shields.io/badge/CVE--2026--56862-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--56859" src="https://img.shields.io/badge/CVE--2026--56859-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--56853" src="https://img.shields.io/badge/CVE--2026--56853-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--42504" src="https://img.shields.io/badge/CVE--2026--42504-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--42499" src="https://img.shields.io/badge/CVE--2026--42499-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--39836" src="https://img.shields.io/badge/CVE--2026--39836-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--39820" src="https://img.shields.io/badge/CVE--2026--39820-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--33818" src="https://img.shields.io/badge/CVE--2026--33818-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--33814" src="https://img.shields.io/badge/CVE--2026--33814-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--33811" src="https://img.shields.io/badge/CVE--2026--33811-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--32283" src="https://img.shields.io/badge/CVE--2026--32283-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--32281" src="https://img.shields.io/badge/CVE--2026--32281-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--32280" src="https://img.shields.io/badge/CVE--2026--32280-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--25679" src="https://img.shields.io/badge/CVE--2026--25679-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2025--61729" src="https://img.shields.io/badge/CVE--2025--61729-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2025--61726" src="https://img.shields.io/badge/CVE--2025--61726-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2025--61725" src="https://img.shields.io/badge/CVE--2025--61725-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2025--61723" src="https://img.shields.io/badge/CVE--2025--61723-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2025--58188" src="https://img.shields.io/badge/CVE--2025--58188-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2025--58187" src="https://img.shields.io/badge/CVE--2025--58187-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2024--34158" src="https://img.shields.io/badge/CVE--2024--34158-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2024--34156" src="https://img.shields.io/badge/CVE--2024--34156-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2024--24791" src="https://img.shields.io/badge/CVE--2024--24791-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2024--24784" src="https://img.shields.io/badge/CVE--2024--24784-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2023--45288" src="https://img.shields.io/badge/CVE--2023--45288-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2023--45283" src="https://img.shields.io/badge/CVE--2023--45283-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2023--44487" src="https://img.shields.io/badge/CVE--2023--44487-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2023--39325" src="https://img.shields.io/badge/CVE--2023--39325-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2022--30635" src="https://img.shields.io/badge/CVE--2022--30635-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="medium : CVE--2026--111943" src="https://img.shields.io/badge/CVE--2026--111943-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--4673" src="https://img.shields.io/badge/CVE--2025--4673-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--27145" src="https://img.shields.io/badge/CVE--2026--27145-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--61728" src="https://img.shields.io/badge/CVE--2025--61728-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--61727" src="https://img.shields.io/badge/CVE--2025--61727-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--47906" src="https://img.shields.io/badge/CVE--2025--47906-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2023--45290" src="https://img.shields.io/badge/CVE--2023--45290-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--32282" src="https://img.shields.io/badge/CVE--2026--32282-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--97030" src="https://img.shields.io/badge/CVE--2026--97030-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--94448" src="https://img.shields.io/badge/CVE--2026--94448-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--56858" src="https://img.shields.io/badge/CVE--2026--56858-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--39826" src="https://img.shields.io/badge/CVE--2026--39826-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--39823" src="https://img.shields.io/badge/CVE--2026--39823-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--32289" src="https://img.shields.io/badge/CVE--2026--32289-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--27142" src="https://img.shields.io/badge/CVE--2026--27142-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2024--45341" src="https://img.shields.io/badge/CVE--2024--45341-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2024--45336" src="https://img.shields.io/badge/CVE--2024--45336-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2023--39319" src="https://img.shields.io/badge/CVE--2023--39319-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2023--39318" src="https://img.shields.io/badge/CVE--2023--39318-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--56860" src="https://img.shields.io/badge/CVE--2026--56860-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2024--24783" src="https://img.shields.io/badge/CVE--2024--24783-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--32288" src="https://img.shields.io/badge/CVE--2026--32288-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--0913" src="https://img.shields.io/badge/CVE--2025--0913-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2024--24789" src="https://img.shields.io/badge/CVE--2024--24789-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2024--24785" src="https://img.shields.io/badge/CVE--2024--24785-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--42507" src="https://img.shields.io/badge/CVE--2026--42507-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--42505" src="https://img.shields.io/badge/CVE--2026--42505-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--39825" src="https://img.shields.io/badge/CVE--2026--39825-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--61730" src="https://img.shields.io/badge/CVE--2025--61730-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--61724" src="https://img.shields.io/badge/CVE--2025--61724-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--58189" src="https://img.shields.io/badge/CVE--2025--58189-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--58186" src="https://img.shields.io/badge/CVE--2025--58186-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--58185" src="https://img.shields.io/badge/CVE--2025--58185-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--47912" src="https://img.shields.io/badge/CVE--2025--47912-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2023--45284" src="https://img.shields.io/badge/CVE--2023--45284-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2023--39326" src="https://img.shields.io/badge/CVE--2023--39326-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--22870" src="https://img.shields.io/badge/CVE--2025--22870-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--58183" src="https://img.shields.io/badge/CVE--2025--58183-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2024--34155" src="https://img.shields.io/badge/CVE--2024--34155-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2023--45289" src="https://img.shields.io/badge/CVE--2023--45289-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--22866" src="https://img.shields.io/badge/CVE--2025--22866-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="low : CVE--2025--22873" src="https://img.shields.io/badge/CVE--2025--22873-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2026--27139" src="https://img.shields.io/badge/CVE--2026--27139-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="unspecified : CVE--2026--97054" src="https://img.shields.io/badge/CVE--2026--97054-lightgrey?label=unspecified%20&labelColor=lightgrey"/></li></ul></td>
	</tr>
</table>
</details>
<details><summary>Changes for packages of type <code>npm</code> (127 changes)</summary>
<table>
	<tr>
		<th></th>
		<th valign="top">Package</th>
		<th valign="top">Version<br/><code>quiz-docker:initial</code></th>
		<th valign="top">Version<br/><code>quiz-docker:secure</code></th>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>@esbuild/linux-x64</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>0.18.20</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>@gar/promise-retry</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.0.3</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>@isaacs/cliui</strong></td>
		<td valign="top"><code>8.0.2</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@npmcli/agent</strong></td>
		<td valign="top"><code>3.0.0</code></td>
		<td valign="top"><code>4.0.2</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@npmcli/arborist</strong></td>
		<td valign="top"><code>8.0.5</code></td>
		<td valign="top"><code>9.9.1</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@npmcli/config</strong></td>
		<td valign="top"><code>9.0.0</code></td>
		<td valign="top"><code>10.12.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@npmcli/fs</strong></td>
		<td valign="top"><code>4.0.0</code></td>
		<td valign="top"><code>5.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@npmcli/git</strong></td>
		<td valign="top"><code>6.0.3</code></td>
		<td valign="top"><code>7.0.2</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@npmcli/installed-package-contents</strong></td>
		<td valign="top"><code>3.0.0</code></td>
		<td valign="top"><code>4.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@npmcli/map-workspaces</strong></td>
		<td valign="top"><code>4.0.2</code></td>
		<td valign="top"><code>5.0.3</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@npmcli/metavuln-calculator</strong></td>
		<td valign="top"><code>8.0.1</code></td>
		<td valign="top"><code>9.0.3</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@npmcli/name-from-folder</strong></td>
		<td valign="top"><code>3.0.0</code></td>
		<td valign="top"><code>4.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@npmcli/node-gyp</strong></td>
		<td valign="top"><code>4.0.0</code></td>
		<td valign="top"><code>5.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@npmcli/package-json</strong></td>
		<td valign="top"><code>6.2.0</code></td>
		<td valign="top"><code>7.0.5</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@npmcli/promise-spawn</strong></td>
		<td valign="top"><code>8.0.3</code></td>
		<td valign="top"><code>9.0.1</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@npmcli/query</strong></td>
		<td valign="top"><code>4.0.1</code></td>
		<td valign="top"><code>5.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@npmcli/redact</strong></td>
		<td valign="top"><code>3.2.2</code></td>
		<td valign="top"><code>4.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@npmcli/run-script</strong></td>
		<td valign="top"><code>9.1.0</code></td>
		<td valign="top"><code>10.0.4</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>@pkgjs/parseargs</strong></td>
		<td valign="top"><code>0.11.0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@sigstore/bundle</strong></td>
		<td valign="top"><code>3.1.0</code></td>
		<td valign="top"><code>4.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@sigstore/core</strong></td>
		<td valign="top"><code>2.0.0</code></td>
		<td valign="top"><code>3.2.1</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
		<td valign="top"></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"><strong>Removed vulnerabilities (1):</strong><br/><ul><li><img alt="medium : CVE--2026--48758" src="https://img.shields.io/badge/CVE--2026--48758-lightgrey?label=medium%20&labelColor=fbb552"/></li></ul></td>
		<td valign="top"></td>
	</tr><tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@sigstore/protobuf-specs</strong></td>
		<td valign="top"><code>0.4.3</code></td>
		<td valign="top"><code>0.5.1</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@sigstore/sign</strong></td>
		<td valign="top"><code>3.1.0</code></td>
		<td valign="top"><code>4.1.1</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@sigstore/tuf</strong></td>
		<td valign="top"><code>3.1.1</code></td>
		<td valign="top"><code>4.0.2</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@sigstore/verify</strong></td>
		<td valign="top"><code>2.1.1</code></td>
		<td valign="top"><code>3.1.1</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>@tufjs/models</strong></td>
		<td valign="top"><code>3.0.1</code></td>
		<td valign="top"><code>4.1.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>abbrev</strong></td>
		<td valign="top"><code>3.0.1</code></td>
		<td valign="top"><code>4.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>balanced-match</strong></td>
		<td valign="top"><code>1.0.2</code></td>
		<td valign="top"><code>4.0.4</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>bin-links</strong></td>
		<td valign="top"><code>5.0.0</code></td>
		<td valign="top"><code>6.0.2</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>binary-extensions</strong></td>
		<td valign="top"><code>2.3.0</code></td>
		<td valign="top"><code>3.1.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>brace-expansion</strong></td>
		<td valign="top"><code>2.0.2</code></td>
		<td valign="top"><code>5.0.9</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 5" src="https://img.shields.io/badge/H-5-e25d68"/> <img alt="medium: 2" src="https://img.shields.io/badge/M-2-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 2" src="https://img.shields.io/badge/H-2-e25d68"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><br/><img atl="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey?labelColor=lightgrey"/><img atl="high: -3" src="https://img.shields.io/badge/H---3-2e7f74?labelColor=lightgrey"/><img atl="medium: -1" src="https://img.shields.io/badge/M---1-2e7f74?labelColor=lightgrey"/><img atl="low: 0" src="https://img.shields.io/badge/L-0-lightgrey?labelColor=lightgrey"/><!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"><strong>Removed vulnerabilities (4):</strong><br/><ul><li><img alt="high : CVE--2026--13149" src="https://img.shields.io/badge/CVE--2026--13149-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--69152" src="https://img.shields.io/badge/CVE--2026--69152-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--14257" src="https://img.shields.io/badge/CVE--2026--14257-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="medium : CVE--2026--33750" src="https://img.shields.io/badge/CVE--2026--33750-lightgrey?label=medium%20&labelColor=fbb552"/></li></ul></td>
		<td valign="top"></td>
	</tr><tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>cacache</strong></td>
		<td valign="top"><code>19.0.1</code></td>
		<td valign="top"><code>20.0.4</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>cidr-regex</strong></td>
		<td valign="top"><code>4.1.3</code></td>
		<td valign="top"><code>5.0.5</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>cli-columns</strong></td>
		<td valign="top"><code>4.0.0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>cmd-shim</strong></td>
		<td valign="top"><code>7.0.0</code></td>
		<td valign="top"><code>8.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>common-ancestor-path</strong></td>
		<td valign="top"><code>1.0.1</code></td>
		<td valign="top"><code>2.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>cross-spawn</strong></td>
		<td valign="top"><code>7.0.6</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>diff</strong></td>
		<td valign="top"><code>5.2.2</code></td>
		<td valign="top"><code>8.0.4</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>encoding</strong></td>
		<td valign="top"><code>0.1.13</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>err-code</strong></td>
		<td valign="top"><code>2.0.3</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>esbuild</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>0.18.20</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (1):</strong><br/><ul><li><img alt="medium : GHSA--67mh--4wv8--2f99" src="https://img.shields.io/badge/GHSA--67mh--4wv8--2f99-lightgrey?label=medium%20&labelColor=fbb552"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>foreground-child</strong></td>
		<td valign="top"><code>3.3.1</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>glob</strong></td>
		<td valign="top"><code>10.5.0</code></td>
		<td valign="top"><code>13.0.6</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><br/><img atl="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey?labelColor=lightgrey"/><img atl="high: 0" src="https://img.shields.io/badge/H-0-lightgrey?labelColor=lightgrey"/><img atl="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey?labelColor=lightgrey"/><img atl="low: 0" src="https://img.shields.io/badge/L-0-lightgrey?labelColor=lightgrey"/><!-- unspecified: 0 --></td>
	</tr><tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>hosted-git-info</strong></td>
		<td valign="top"><code>8.1.0</code></td>
		<td valign="top"><code>9.0.3</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>iconv-lite</strong></td>
		<td valign="top"><code>0.6.3</code></td>
		<td valign="top"><code>0.7.2</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>ignore-walk</strong></td>
		<td valign="top"><code>7.0.0</code></td>
		<td valign="top"><code>8.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>imurmurhash</strong></td>
		<td valign="top"><code>0.1.4</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>ini</strong></td>
		<td valign="top"><code>5.0.0</code></td>
		<td valign="top"><code>6.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>init-package-json</strong></td>
		<td valign="top"><code>7.0.2</code></td>
		<td valign="top"><code>8.2.5</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>ip-address</strong></td>
		<td valign="top"><code>10.1.0</code></td>
		<td valign="top"><code>10.5.0</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 5" src="https://img.shields.io/badge/M-5-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 5" src="https://img.shields.io/badge/M-5-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><br/><img atl="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey?labelColor=lightgrey"/><img atl="high: -1" src="https://img.shields.io/badge/H---1-2e7f74?labelColor=lightgrey"/><img atl="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey?labelColor=lightgrey"/><img atl="low: 0" src="https://img.shields.io/badge/L-0-lightgrey?labelColor=lightgrey"/><!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"><strong>Removed vulnerabilities (2):</strong><br/><ul><li><img alt="high : CVE--2026--69192" src="https://img.shields.io/badge/CVE--2026--69192-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="medium : CVE--2026--42338" src="https://img.shields.io/badge/CVE--2026--42338-lightgrey?label=medium%20&labelColor=fbb552"/></li></ul></td>
		<td valign="top"><strong>Added vulnerabilities (1):</strong><br/><ul><li><img alt="medium : CVE--2026--101910" src="https://img.shields.io/badge/CVE--2026--101910-lightgrey?label=medium%20&labelColor=fbb552"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>ip-regex</strong></td>
		<td valign="top"><code>5.0.0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>is-cidr</strong></td>
		<td valign="top"><code>5.1.1</code></td>
		<td valign="top"><code>6.0.4</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>isexe</strong></td>
		<td valign="top"><code>3.1.5</code></td>
		<td valign="top"><code>4.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>jackspeak</strong></td>
		<td valign="top"><code>3.4.3</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>json-parse-even-better-errors</strong></td>
		<td valign="top"><code>4.0.0</code></td>
		<td valign="top"><code>5.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>libnpmaccess</strong></td>
		<td valign="top"><code>9.0.0</code></td>
		<td valign="top"><code>10.0.3</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>libnpmdiff</strong></td>
		<td valign="top"><code>7.0.5</code></td>
		<td valign="top"><code>8.1.12</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>libnpmexec</strong></td>
		<td valign="top"><code>9.0.5</code></td>
		<td valign="top"><code>10.3.2</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>libnpmfund</strong></td>
		<td valign="top"><code>6.0.5</code></td>
		<td valign="top"><code>7.0.26</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>libnpmhook</strong></td>
		<td valign="top"><code>11.0.0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>libnpmorg</strong></td>
		<td valign="top"><code>7.0.0</code></td>
		<td valign="top"><code>8.0.1</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>libnpmpack</strong></td>
		<td valign="top"><code>8.0.5</code></td>
		<td valign="top"><code>9.1.13</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>libnpmpublish</strong></td>
		<td valign="top"><code>10.0.2</code></td>
		<td valign="top"><code>11.2.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>libnpmsearch</strong></td>
		<td valign="top"><code>8.0.0</code></td>
		<td valign="top"><code>9.0.1</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>libnpmteam</strong></td>
		<td valign="top"><code>7.0.0</code></td>
		<td valign="top"><code>8.0.2</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>libnpmversion</strong></td>
		<td valign="top"><code>7.0.0</code></td>
		<td valign="top"><code>8.0.4</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>lru-cache</strong></td>
		<td valign="top"><code>10.4.3</code></td>
		<td valign="top"><code>11.5.1</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>make-fetch-happen</strong></td>
		<td valign="top"><code>14.0.3</code></td>
		<td valign="top"><code>15.0.6</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>minimatch</strong></td>
		<td valign="top"><code>9.0.9</code></td>
		<td valign="top"><code>3.1.5</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
		<td valign="top"></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"><strong>Removed vulnerabilities (1):</strong><br/><ul><li><img alt="medium : CVE--2026--118764" src="https://img.shields.io/badge/CVE--2026--118764-lightgrey?label=medium%20&labelColor=fbb552"/></li></ul></td>
		<td valign="top"></td>
	</tr><tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>minipass-fetch</strong></td>
		<td valign="top"><code>4.0.1</code></td>
		<td valign="top"><code>5.0.2</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>minipass-flush</strong></td>
		<td valign="top"><code>1.0.5</code></td>
		<td valign="top"><code>1.0.6</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>minipass-sized</strong></td>
		<td valign="top"><code>1.0.3</code></td>
		<td valign="top"><code>2.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>mute-stream</strong></td>
		<td valign="top"><code>2.0.0</code></td>
		<td valign="top"><code>3.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>nanoid</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.3.6</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 3" src="https://img.shields.io/badge/H-3-e25d68"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (4):</strong><br/><ul><li><img alt="high : CVE--2026--67214" src="https://img.shields.io/badge/CVE--2026--67214-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--67213" src="https://img.shields.io/badge/CVE--2026--67213-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--73086" src="https://img.shields.io/badge/CVE--2026--73086-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="medium : CVE--2024--55565" src="https://img.shields.io/badge/CVE--2024--55565-lightgrey?label=medium%20&labelColor=fbb552"/></li></ul></td>
	</tr><tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>node-gyp</strong></td>
		<td valign="top"><code>11.5.0</code></td>
		<td valign="top"><code>12.4.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>nopt</strong></td>
		<td valign="top"><code>8.1.0</code></td>
		<td valign="top"><code>9.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>normalize-package-data</strong></td>
		<td valign="top"><code>7.0.1</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>npm</strong></td>
		<td valign="top"><code>10.9.9</code></td>
		<td valign="top"><code>11.19.1</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>npm-audit-report</strong></td>
		<td valign="top"><code>6.0.0</code></td>
		<td valign="top"><code>7.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>npm-bundled</strong></td>
		<td valign="top"><code>4.0.0</code></td>
		<td valign="top"><code>5.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>npm-install-checks</strong></td>
		<td valign="top"><code>7.1.2</code></td>
		<td valign="top"><code>8.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>npm-normalize-package-bin</strong></td>
		<td valign="top"><code>4.0.0</code></td>
		<td valign="top"><code>5.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>npm-package-arg</strong></td>
		<td valign="top"><code>12.0.2</code></td>
		<td valign="top"><code>13.0.2</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>npm-packlist</strong></td>
		<td valign="top"><code>9.0.0</code></td>
		<td valign="top"><code>10.0.4</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>npm-pick-manifest</strong></td>
		<td valign="top"><code>10.0.0</code></td>
		<td valign="top"><code>11.0.3</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>npm-profile</strong></td>
		<td valign="top"><code>11.0.1</code></td>
		<td valign="top"><code>12.0.2</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>npm-registry-fetch</strong></td>
		<td valign="top"><code>18.0.2</code></td>
		<td valign="top"><code>19.1.1</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>npm-user-validate</strong></td>
		<td valign="top"><code>3.0.0</code></td>
		<td valign="top"><code>4.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>package-json-from-dist</strong></td>
		<td valign="top"><code>1.0.1</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>pacote</strong></td>
		<td valign="top"><code>20.0.1</code></td>
		<td valign="top"><code>21.5.1</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
		<td valign="top"></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"><strong>Removed vulnerabilities (1):</strong><br/><ul><li><img alt="high : CVE--2026--9496" src="https://img.shields.io/badge/CVE--2026--9496-lightgrey?label=high%20&labelColor=e25d68"/></li></ul></td>
		<td valign="top"></td>
	</tr><tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>parse-conflict-json</strong></td>
		<td valign="top"><code>4.0.0</code></td>
		<td valign="top"><code>5.0.1</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>path-key</strong></td>
		<td valign="top"><code>3.1.1</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>path-scurry</strong></td>
		<td valign="top"><code>1.11.1</code></td>
		<td valign="top"><code>2.0.2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>picocolors</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>picomatch</strong></td>
		<td valign="top"><code>4.0.3</code></td>
		<td valign="top"><code>4.0.4</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
		<td valign="top"></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"><strong>Removed vulnerabilities (2):</strong><br/><ul><li><img alt="high : CVE--2026--33671" src="https://img.shields.io/badge/CVE--2026--33671-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="medium : CVE--2026--33672" src="https://img.shields.io/badge/CVE--2026--33672-lightgrey?label=medium%20&labelColor=fbb552"/></li></ul></td>
		<td valign="top"></td>
	</tr><tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>postcss</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>8.4.30</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 2" src="https://img.shields.io/badge/H-2-e25d68"/> <img alt="medium: 3" src="https://img.shields.io/badge/M-3-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (5):</strong><br/><ul><li><img alt="high : CVE--2026--73646" src="https://img.shields.io/badge/CVE--2026--73646-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--45623" src="https://img.shields.io/badge/CVE--2026--45623-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="medium : CVE--2026--69153" src="https://img.shields.io/badge/CVE--2026--69153-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--41305" src="https://img.shields.io/badge/CVE--2026--41305-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2023--44270" src="https://img.shields.io/badge/CVE--2023--44270-lightgrey?label=medium%20&labelColor=fbb552"/></li></ul></td>
	</tr><tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>postcss-selector-parser</strong></td>
		<td valign="top"><code>7.1.1</code></td>
		<td valign="top"><code>7.1.4</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 0" src="https://img.shields.io/badge/H-0-lightgrey"/> <img alt="medium: 1" src="https://img.shields.io/badge/M-1-fbb552"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --><br/><img atl="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey?labelColor=lightgrey"/><img atl="high: 0" src="https://img.shields.io/badge/H-0-lightgrey?labelColor=lightgrey"/><img atl="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey?labelColor=lightgrey"/><img atl="low: -1" src="https://img.shields.io/badge/L---1-2e7f74?labelColor=lightgrey"/><!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"><strong>Removed vulnerabilities (1):</strong><br/><ul><li><img alt="low : CVE--2026--9358" src="https://img.shields.io/badge/CVE--2026--9358-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
		<td valign="top"></td>
	</tr><tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>proc-log</strong></td>
		<td valign="top"><code>5.0.0</code></td>
		<td valign="top"><code>6.1.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>proggy</strong></td>
		<td valign="top"><code>3.0.0</code></td>
		<td valign="top"><code>4.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>promise-retry</strong></td>
		<td valign="top"><code>2.0.1</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>promzard</strong></td>
		<td valign="top"><code>2.0.0</code></td>
		<td valign="top"><code>3.0.1</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>read</strong></td>
		<td valign="top"><code>4.1.0</code></td>
		<td valign="top"><code>5.0.1</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>read-cmd-shim</strong></td>
		<td valign="top"><code>5.0.0</code></td>
		<td valign="top"><code>6.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>read-package-json-fast</strong></td>
		<td valign="top"><code>4.0.0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>retry</strong></td>
		<td valign="top"><code>0.12.0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>rollup</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>3.29.4</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 2" src="https://img.shields.io/badge/H-2-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (2):</strong><br/><ul><li><img alt="high : CVE--2026--27606" src="https://img.shields.io/badge/CVE--2026--27606-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2024--47068" src="https://img.shields.io/badge/CVE--2024--47068-lightgrey?label=high%20&labelColor=e25d68"/></li></ul></td>
	</tr><tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>semver</strong></td>
		<td valign="top"><code>7.7.4</code></td>
		<td valign="top"><code>7.8.5</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>shebang-command</strong></td>
		<td valign="top"><code>2.0.0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>shebang-regex</strong></td>
		<td valign="top"><code>3.0.0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>sigstore</strong></td>
		<td valign="top"><code>3.1.0</code></td>
		<td valign="top"><code>4.1.1</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
		<td valign="top"></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"><strong>Removed vulnerabilities (1):</strong><br/><ul><li><img alt="high : CVE--2026--48815" src="https://img.shields.io/badge/CVE--2026--48815-lightgrey?label=high%20&labelColor=e25d68"/></li></ul></td>
		<td valign="top"></td>
	</tr><tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>socks</strong></td>
		<td valign="top"><code>2.8.7</code></td>
		<td valign="top"><code>2.8.9</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>source-map-js</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>1.0.2</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 1" src="https://img.shields.io/badge/H-1-e25d68"/> <img alt="medium: 0" src="https://img.shields.io/badge/M-0-lightgrey"/> <img alt="low: 0" src="https://img.shields.io/badge/L-0-lightgrey"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (1):</strong><br/><ul><li><img alt="high : CVE--2026--93749" src="https://img.shields.io/badge/CVE--2026--93749-lightgrey?label=high%20&labelColor=e25d68"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>spdx-correct</strong></td>
		<td valign="top"><code>3.2.0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>ssri</strong></td>
		<td valign="top"><code>12.0.0</code></td>
		<td valign="top"><code>13.0.1</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>supports-color</strong></td>
		<td valign="top"><code>9.4.0</code></td>
		<td valign="top"><code>7.2.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>tiny-relative-date</strong></td>
		<td valign="top"><code>1.3.0</code></td>
		<td valign="top"><code>2.0.2</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>tinyglobby</strong></td>
		<td valign="top"><code>0.2.15</code></td>
		<td valign="top"><code>0.2.17</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>tuf-js</strong></td>
		<td valign="top"><code>3.1.0</code></td>
		<td valign="top"><code>4.1.0</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>undici</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>6.28.0</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 4" src="https://img.shields.io/badge/H-4-e25d68"/> <img alt="medium: 3" src="https://img.shields.io/badge/M-3-fbb552"/> <img alt="low: 1" src="https://img.shields.io/badge/L-1-fce1a9"/> <!-- unspecified: 0 --></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (8):</strong><br/><ul><li><img alt="high : CVE--2026--87018" src="https://img.shields.io/badge/CVE--2026--87018-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--19534" src="https://img.shields.io/badge/CVE--2026--19534-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--109869" src="https://img.shields.io/badge/CVE--2026--109869-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2026--109383" src="https://img.shields.io/badge/CVE--2026--109383-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="medium : CVE--2026--85024" src="https://img.shields.io/badge/CVE--2026--85024-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--109932" src="https://img.shields.io/badge/CVE--2026--109932-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--109924" src="https://img.shields.io/badge/CVE--2026--109924-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="low : CVE--2026--18540" src="https://img.shields.io/badge/CVE--2026--18540-lightgrey?label=low%20&labelColor=fce1a9"/></li></ul></td>
	</tr><tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>unique-filename</strong></td>
		<td valign="top"><code>4.0.0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>unique-slug</strong></td>
		<td valign="top"><code>5.0.0</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:heavy_minus_sign:</td>
		<td valign="top"><strong>validate-npm-package-license</strong></td>
		<td valign="top"><code>3.0.4</code></td>
		<td valign="top"></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>validate-npm-package-name</strong></td>
		<td valign="top"><code>6.0.2</code></td>
		<td valign="top"><code>7.0.2</code></td>
	</tr>
	<tr>
		<td valign="top">:heavy_plus_sign:</td>
		<td valign="top"><strong>vite</strong></td>
		<td valign="top"></td>
		<td valign="top"><code>4.4.9</code></td>
	</tr>
	<tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><img alt="critical: 0" src="https://img.shields.io/badge/C-0-lightgrey"/> <img alt="high: 3" src="https://img.shields.io/badge/H-3-e25d68"/> <img alt="medium: 17" src="https://img.shields.io/badge/M-17-fbb552"/> <img alt="low: 3" src="https://img.shields.io/badge/L-3-fce1a9"/> <img alt="unspecified: 1" src="https://img.shields.io/badge/U-1-lightgrey"/></td>
	</tr><tr>
		<td colspan="2"></td>
		<td valign="top"></td>
		<td valign="top"><strong>Added vulnerabilities (24):</strong><br/><ul><li><img alt="high : CVE--2026--112942" src="https://img.shields.io/badge/CVE--2026--112942-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2024--52011" src="https://img.shields.io/badge/CVE--2024--52011-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="high : CVE--2024--23331" src="https://img.shields.io/badge/CVE--2024--23331-lightgrey?label=high%20&labelColor=e25d68"/></li><li><img alt="medium : CVE--2026--53571" src="https://img.shields.io/badge/CVE--2026--53571-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2024--45811" src="https://img.shields.io/badge/CVE--2024--45811-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--24010" src="https://img.shields.io/badge/CVE--2025--24010-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--39365" src="https://img.shields.io/badge/CVE--2026--39365-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--112946" src="https://img.shields.io/badge/CVE--2026--112946-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--112944" src="https://img.shields.io/badge/CVE--2026--112944-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--112943" src="https://img.shields.io/badge/CVE--2026--112943-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2023--49293" src="https://img.shields.io/badge/CVE--2023--49293-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--46565" src="https://img.shields.io/badge/CVE--2025--46565-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--32395" src="https://img.shields.io/badge/CVE--2025--32395-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : GHSA--8jhw--289h--jh2g" src="https://img.shields.io/badge/GHSA--8jhw--289h--jh2g-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2024--31207" src="https://img.shields.io/badge/CVE--2024--31207-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2026--53632" src="https://img.shields.io/badge/CVE--2026--53632-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--31486" src="https://img.shields.io/badge/CVE--2025--31486-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--31125" src="https://img.shields.io/badge/CVE--2025--31125-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2025--30208" src="https://img.shields.io/badge/CVE--2025--30208-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="medium : CVE--2024--45812" src="https://img.shields.io/badge/CVE--2024--45812-lightgrey?label=medium%20&labelColor=fbb552"/></li><li><img alt="low : CVE--2025--58752" src="https://img.shields.io/badge/CVE--2025--58752-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2025--58751" src="https://img.shields.io/badge/CVE--2025--58751-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="low : CVE--2026--112945" src="https://img.shields.io/badge/CVE--2026--112945-lightgrey?label=low%20&labelColor=fce1a9"/></li><li><img alt="unspecified : GHSA--859w--5945--r5v3" src="https://img.shields.io/badge/GHSA--859w--5945--r5v3-lightgrey?label=unspecified%20&labelColor=lightgrey"/></li></ul></td>
	</tr><tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>walk-up-path</strong></td>
		<td valign="top"><code>3.0.1</code></td>
		<td valign="top"><code>4.0.0</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>which</strong></td>
		<td valign="top"><code>5.0.0</code></td>
		<td valign="top"><code>6.0.1</code></td>
	</tr>
	<tr>
		<td valign="top">:infinity:</td>
		<td valign="top"><strong>write-file-atomic</strong></td>
		<td valign="top"><code>6.0.0</code></td>
		<td valign="top"><code>7.0.1</code></td>
	</tr>
	
</table>
</details>
</details>
