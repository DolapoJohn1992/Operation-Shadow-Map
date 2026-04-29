# Perimeter Assessment Report: Operation Shadow Map

## Phase 1: Nmap Findings
* **Live IPs Discovered:**
  1. 172.88.0.10
  2. 172.88.0.15
  3. 172.88.0.20

* **Service/Version Breakdown:**
  * IP 172.88.0.10: nginx 1.14.2
  * IP 172.88.0.15: Cache Database (Ports filtered)
  * IP 172.88.0.20: Apache httpd 2.4.41

## Phase 2: Vulnerability Audit (Nikto)
* **Web Server 1 (172.88.0.10):**
  * Finding: The anti-clickjacking X-Frame-Options header is not present.
* **Web Server 2 (172.88.0.20):**
  * Finding: The anti-clickjacking X-Frame-Options header is not present.

## Phase 3: Risk Triage & Justification
* **Top Priority Finding:** Outdated Nginx 1.14.2 on 172.88.0.10.
* **Risk Justification:** This is the highest priority because the likelihood of exploitation is high due to publicly available exploits for this 2018 software version, and the impact is critical as it could allow unauthorized access to the DMZ.
