# Methodology

1. Prepare an authorized test workstation and confirm Wireshark can capture on the intended interface.
2. Capture a Telnet login session using disposable lab credentials.
3. Stop capture and apply `telnet`.
4. Use **Follow → TCP Stream** to inspect the session. Record only the security observation; do not copy the password into documentation.
5. Start a separate capture and establish an SSH session to the authorized lab endpoint.
6. Stop capture, apply `ssh`, and inspect **Follow → TCP Stream**.
7. Compare what is readable in each stream and document the findings.
8. Review screenshots and captures for sensitive information before saving or publishing.
9. Complete the lab report and evidence checklist.

The provided lab PDF describes a CyberOps Workstation, loopback (`lo`), and `localhost`. Adapt only as required for your authorized lab, and document any changes.
