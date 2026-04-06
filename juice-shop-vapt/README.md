# Vulnerability Assessment - OWASP Juice Shop
Passive web application security assessment conducted as part of a cybersecurity internship task.

## Website Tested 
| Field | Details |
|-------|--------|
| Target | https://juice-shopherokuapp.com |
| Type | Intentionally vulnerable web application (OWASP) |
| Date | 05 April, 2026 |
| Analyst | Mubeen |

## Scope & Ethics
This assessment was strictly passive and read-only. No exploitation, active attacks, or data modification were performed. OWASP Juice Shop is a deliberately vulnerable application built for security training - testing it is fully authorised and ethical.

## Tools Used 
| Tool | Version | Purpose |
|------|---------|---------|
| Nmap | 7.95 | Network port scanning & service fingerprinting |
| OWASP ZAP | 2.17.0 | Passive traffic interception & header analysis |
| BrowserDevTools | Firefox | HTTP response header inspection |

## Findings Summary 
| ID | Finding | Severity | Tool |
|----|--------|----------|-------|
| F-01 | Missing Content Security Policy | High | DevTools |
| F-02 | CORS Wildcard Misconfiguration | Medium | ZAP |
| F-03 | Missing HSTS Header | Medium | DevTools + ZAP |
| F-04 | Server & Infrastructure Disclosure | Low | Nmap + DevTools |
| F-05 | Unexpected Open Port - FTP (21) | Low | Nmap |
| F-06 | X-Content-Type-Options Missing on API | Low | ZAP |
| F-07 | Unix Timestamp Disclosure | Low | ZAP |
| F-08 | Admin & Sensitive API Endpoints Exposed | Info | ZAP |

Total: 0 Critical | 1 High | 2 Medium | 4 Low | 1 Informational

## Key Learnings 
- How to use Nmap to fingerprint open ports and identify infrastructure
- How to read and interpret HTTP reponse headers for security misconfigurations
- How to use OWASP ZAP passive scan to detect vulnerabilities without active exploitation
- The difference between passive and active security assessment
- How to write a professional VAPT report with findings, risk levels, and remediation steps

## References
- OWASP Juice Shop
- OWASPZAP
- Mozilla HTTP Headers Reference
- Content Security Policy Guide


**This project is part of my cybersecurity learning portfolio. All testing was conducted ethically on an intentionally vulnerable application.**
