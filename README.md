# Examining Telnet and SSH in Wireshark

## Project overview
This project documents a controlled lab comparing Telnet and SSH traffic in Wireshark. The objective is to observe why Telnet exposes session data in plaintext while SSH protects session contents through encryption.

> **Safety and privacy:** Perform this exercise only on your own lab workstation or systems for which you have explicit permission. The supplied lab uses localhost. Do not capture other people's traffic or commit real passwords, tokens, private keys, or sensitive packet captures to GitHub.

## Learning objectives
- Capture a Telnet session on the loopback (`lo`) interface.
- Use the `telnet` display filter and **Follow → TCP Stream** to inspect the session.
- Observe that Telnet may expose usernames and passwords in plaintext.
- Capture an SSH session and inspect it using the `ssh` display filter and **Follow → TCP Stream**.
- Compare the visibility of application data in Telnet and SSH.
- Explain why SSH is preferred for remote administration.

## Lab environment
Fill in the actual details used in your lab:
- Workstation / OS: `TODO`
- Wireshark version: `TODO`
- Telnet client/server: `TODO`
- SSH client/server: `TODO`
- Capture interface: `lo` (loopback), if following the supplied lab
- Test target: `localhost`

## Repository structure
```text
.
├── README.md
├── .gitignore
├── LICENSE
├── COMMANDS.md
├── EVIDENCE_CHECKLIST.md
├── LAB_REPORT.md
├── docs/
│   ├── methodology.md
│   └── troubleshooting.md
├── evidence/
│   ├── telnet/
│   └── ssh/
├── screenshots/
├── captures/
├── notes/
└── scripts/
```

## Procedure summary

### Part 1 — Telnet
1. Start Wireshark and capture on `lo` (or the appropriate lab interface).
2. In a separate terminal, connect to the authorized lab endpoint.
3. Enter only disposable lab credentials. Stop the capture after the test login.
4. Apply the display filter `telnet`.
5. Select a Telnet packet and choose **Follow → TCP Stream**.
6. Record what is visible, but **do not save or publish the actual password**. Redact credentials in screenshots and notes.

### Part 2 — SSH
1. Start a new capture on the same lab interface.
2. Connect to the authorized SSH endpoint.
3. Stop the capture and apply the display filter `ssh`.
4. Select an SSH packet and choose **Follow → TCP Stream**.
5. Record how the session differs from Telnet. SSH payload should not expose the interactive session's credentials or commands as readable plaintext in the stream.

### Part 3 — Compare and conclude
Complete `LAB_REPORT.md` using observations from your own run. Add redacted screenshots to `screenshots/` and supporting evidence to `evidence/`. Do not upload unredacted captures containing credentials.

## Key findings (complete from your own observations)
- Telnet stream observation: `TODO`
- SSH stream observation: `TODO`
- Security implications: `TODO`
- Conclusion: `TODO`

## Evidence
Use `EVIDENCE_CHECKLIST.md` to track the evidence you collect. The repository intentionally contains placeholders only; no screenshots, packet captures, or lab results have been fabricated.

## How to publish
Follow `GITHUB_WORKFLOW.md` or the Git Bash commands in `COMMANDS.md`. Review every file before committing to ensure that it contains no credentials or private data.
