# Advisory: CVE-2021-44228

## Log4Shell (Remote code injection in Log4j)

Research note recorded from GitHub's Security Advisory Database (GHSA).

| Field | Value (as returned by the database) |
|---|---|
| GHSA ID | GHSA-jfh8-c2jp-5v3q |
| CVE | CVE-2021-44228 |
| Severity | critical |
| CVSS v3.1 | 10.0 (CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:C/C:H/I:H/A:H/E:H) |
| Affected package | Maven: org.apache.logging.log4j:log4j-core |
| Vulnerable version range | >= 2.13.0, < 2.15.0 |
| First patched version | 2.15.0 |
| Summary | Remote code injection in Log4j |
| Published | 2021-12-10T00:40:56Z |
| Advisory URL | https://github.com/advisories/GHSA-jfh8-c2jp-5v3q |

### Additional ranges from the same advisory

| Package | Vulnerable range | First patched |
|---|---|---|
| org.apache.logging.log4j:log4j-core | >= 2.0-beta9, < 2.3.1 | 2.3.1 |
| org.apache.logging.log4j:log4j-core | >= 2.4, < 2.12.2 | 2.12.2 |
| com.guicedee.services:log4j-core | <= 1.2.1.2-jre17 (last affected) | none listed |
| org.ops4j.pax.logging:pax-logging-log4j2 | >= 1.8.0, < 1.9.2 | 1.9.2 |
| org.ops4j.pax.logging:pax-logging-log4j2 | >= 1.10.0, < 1.10.8 | 1.10.8 |
| org.ops4j.pax.logging:pax-logging-log4j2 | >= 1.11.0, < 1.11.10 | 1.11.10 |
| org.ops4j.pax.logging:pax-logging-log4j2 | >= 2.0.0, < 2.0.11 | 2.0.11 |

### Notes

- The advisory's own summary states that any Log4J version prior to v2.15.0 is affected, and recommends upgrading to 2.16.0 where possible, because the 2.15.0 patch did not disable attacker-controlled JNDI lookups in all situations.
- Only `org.apache.logging.log4j:log4j-core` is directly affected; `log4j-api` should be kept at the same version.
- Backports of the fix exist in 2.3.1, 2.12.2, and 2.12.3.
- Security-release note: severity **critical** (CVSS 10.0).
