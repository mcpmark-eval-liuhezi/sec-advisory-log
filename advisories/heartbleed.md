# Advisory: CVE-2014-0160

## Heartbleed (OpenSSL TLS/DTLS heartbeat buffer over-read)

Research note recorded from GitHub's Security Advisory Database (GHSA).

| Field | Value (as returned by the database) |
|---|---|
| GHSA ID | GHSA-w8r8-w5w4-4w4v |
| CVE | CVE-2014-0160 |
| Severity | high |
| CVSS v3.1 | 7.5 (CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N/A:N) |
| Affected package | Not returned by the database — the advisory record lists no structured `affected` packages (empty list). The affected software is stated only in the advisory text: OpenSSL. |
| Vulnerable version range | Not returned by the database. Per the advisory text: OpenSSL 1.0.1 before 1.0.1g. |
| First patched version | Not returned by the database. Per the advisory text: OpenSSL 1.0.1g. |
| Summary | The (1) TLS and (2) DTLS implementations in OpenSSL 1.0.1 before 1.0.1g do not properly handle Heartbeat Extension packets, which allows remote attackers to obtain sensitive information from process memory via crafted packets that trigger a buffer over-read, as demonstrated by reading private keys, related to d1_both.c and t1_lib.c, aka the Heartbleed bug. |
| Published | 2022-05-13T01:14:41Z |
| Advisory URL | https://github.com/advisories/GHSA-w8r8-w5w4-4w4v |

### Notes

- This GHSA is classified as `unreviewed` (not `reviewed`) by the GitHub Advisory Database, and its structured `affected` list is empty; consequently no package name, vulnerable version range, or first patched version is exposed in the API response. The OpenSSL package/version details above come from the advisory's own description text, quoted verbatim.
- CWES recorded: CWE-119 (Improper Restriction of Operations within the Bounds of a Memory Buffer), CWE-125 (Out-of-bounds Read).
- Security-release note: severity **high** (CVSS 7.5).
