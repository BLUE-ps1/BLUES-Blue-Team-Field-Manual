# Nmap Cheatsheet

## Common Scans
- Full TCP port scan: `nmap -p- -T4 -oN fullscan.txt 10.10.10.10`
- Service/version scan: `nmap -sC -sV -p22,80 10.10.10.10`
- OS detection: `nmap -O 10.10.10.10`

## Useful NSE scripts
- Default scripts: `nmap -sC`
- Vulnerability scan: `nmap --script vuln 10.10.10.10`

---
*Tip:* save outputs to `/notes/scans/` and reference them in writeups.
