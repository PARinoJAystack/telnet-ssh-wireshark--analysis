# GitHub Workflow — Telnet and SSH in Wireshark

## Recommended repository
**Name:** `telnet-ssh-wireshark-analysis`

**Description:** A hands-on Wireshark lab comparing Telnet plaintext traffic with encrypted SSH sessions, with documented methodology, redacted evidence, and security findings.

## Before starting
- Complete the lab in an authorized, isolated environment.
- Use disposable lab credentials only.
- Capture on the correct interface; the supplied exercise uses loopback (`lo`) and `localhost`.
- Never publish a real password, token, private key, or unredacted packet capture.
- Replace every `TODO` in the report with your actual observations.

## Evidence collection plan
1. `screenshots/01-wireshark-telnet-filter.png` — Telnet packets with the `telnet` display filter.
2. `screenshots/02-telnet-stream-redacted.png` — Follow TCP Stream view with credentials fully redacted.
3. `screenshots/03-wireshark-ssh-filter.png` — SSH packets with the `ssh` display filter.
4. `screenshots/04-ssh-stream.png` — SSH Follow TCP Stream showing encrypted/unreadable session content.
5. `evidence/telnet/observations.md` — concise observations, with no actual credentials.
6. `evidence/ssh/observations.md` — concise observations.
7. `LAB_REPORT.md` — comparison and conclusion based on your own test.

Screenshots listed above are suggestions, not existing evidence. Capture your own and use the listed filenames if convenient.

## Git Bash publishing workflow
From inside the extracted project folder:

```bash
git init
git branch -M main
git add .
git status
```

Inspect the staged files. If anything sensitive appears, unstage it with `git restore --staged PATH` and remove/redact it before proceeding.

```bash
git commit -m "Add Telnet and SSH Wireshark lab documentation"
```

Create an empty repository on GitHub named `telnet-ssh-wireshark-analysis`, then run:

```bash
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/telnet-ssh-wireshark-analysis.git
git push -u origin main
```

Replace the username placeholder with your GitHub username. For future changes:

```bash
git add .
git status
git commit -m "Document Telnet and SSH traffic analysis"
git push
```

## Suggested commit sequence
- `Add project structure and lab methodology`
- `Add redacted Telnet capture evidence`
- `Add SSH capture evidence and comparison`
- `Finalize findings and reflection`

Only use a commit message when the matching work has actually been completed.
