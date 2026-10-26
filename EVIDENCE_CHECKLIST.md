# Evidence Checklist

Mark an item only after collecting and reviewing your own evidence.

- [ ] Record OS/workstation and Wireshark version in `LAB_REPORT.md`.
- [ ] Capture Telnet traffic in the authorized lab.
- [ ] Save screenshot showing the `telnet` display filter.
- [ ] Inspect Follow TCP Stream and document plaintext exposure.
- [ ] Redact username/password and any sensitive data from screenshots.
- [ ] Capture SSH traffic in the authorized lab.
- [ ] Save screenshot showing the `ssh` display filter.
- [ ] Inspect Follow TCP Stream and document the encrypted session view.
- [ ] Complete the comparison table in `LAB_REPORT.md`.
- [ ] Review packet captures for sensitive content; do not publish raw captures by default.
- [ ] Check screenshots for passwords, tokens, private information, and unrelated traffic.
- [ ] Run `git status` and inspect staged files before every commit.
- [ ] Push to GitHub and verify the README renders correctly.

## Suggested screenshot names
- `screenshots/01-wireshark-telnet-filter.png`
- `screenshots/02-telnet-stream-redacted.png`
- `screenshots/03-wireshark-ssh-filter.png`
- `screenshots/04-ssh-stream.png`
