# vulscan using Nessus on the local network 


```markdown
# Task 3 – Basic Vulnerability Scan

## Objective
Perform a basic vulnerability scan on a local machine using Nessus Essentials to identify and document security risks.

---

## Tool Used
- **Nessus Essentials** (Free Edition)
- **Scan Type:** Basic Network Scan
- **Target:** `192.168.204.140`
- **OS:** Linux Kernel 6.12.32-amd64 on Debian 6.4

---

## Steps Performed
1. Installed Nessus Essentials from the official Tenable website.
2. Activated the scanner with a free license key.
3. Accessed Nessus in a web browser at `https://localhost:8834`.
4. Created a new scan named **basic** targeting `192.168.204.140`.
5. Launched the scan and waited for completion (~7 minutes).
6. Reviewed and documented vulnerabilities found.

---

## Scan Summary
| Severity  | Count |
|-----------|-------|
| Critical  | 0     |
| High      | 0     |
| Medium    | 1     |
| Low       | 0     |
| Info      | 60    |

**Total vulnerabilities:** 61

---

## Notable Findings
### 1. SQLite < 3.50.2 Memory Corruption
- **Severity:** Medium (CVSS 6.4)
- **Description:** Vulnerable SQLite versions may allow memory corruption, potentially leading to crashes or arbitrary code execution.
- **Recommendation:** Update SQLite to version 3.50.2 or later.

### 2. Multiple Informational Issues
- **Node.js Multiple Issues** – Outdated version, may contain module vulnerabilities.
- **Tenable Nessus Multiple Issues** – Informational scan results.
- **DNS / SSL / SSH Multiple Issues** – Configuration and certificate-related findings.
- **Apache HTTP Server Multiple Issues** – Outdated modules/misconfigurations.
- **Docker Multiple Issues** – Minor configuration exposures.
- **Netstat Portscanner** – Open service enumeration.

---

## Recommendations
- Patch **SQLite** immediately.
- Update Node.js, Apache HTTP Server, and Docker to latest stable versions.
- Harden SSH and SSL configurations.
- Close or restrict unnecessary open ports.

---

## Screenshots
![Nessus Scan Results](scan_results.png)

---

## Key Learnings
- Nessus Essentials can quickly identify vulnerabilities and configurations needing review.
- Even with no critical/high vulnerabilities, medium and informational findings are important for hardening.
- Regular scans help maintain a proactive security posture.

---

## References
- [Nessus Essentials Download](https://www.tenable.com/products/nessus/nessus-essentials)
- [CVSS Scoring System](https://www.first.org/cvss/)
```


