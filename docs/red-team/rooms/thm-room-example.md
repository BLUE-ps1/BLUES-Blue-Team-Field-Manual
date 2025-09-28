# THM Room Example

**Date:** 2025-08-XX  
**Platform:** TryHackMe  
**Difficulty:** Medium

## Objective
Enumerate, gain initial access, and escalate privileges.

## Recon
- `nmap -sC -sV -p- -oN nmap_initial.txt 10.10.10.10`

## Exploitation
Example exploit command:
```bash
python3 exploit.py -t 10.10.10.10 -p 8080 -o shell
```

## Post-Exploitation
- `sudo -l`
- `id`
- `cat /etc/passwd`

## Notes
Sanitize any sensitive details before publishing.
