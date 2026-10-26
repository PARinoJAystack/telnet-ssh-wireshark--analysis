# Git Bash Commands

Run these commands in Git Bash after extracting the ZIP.

## 1. Enter the project directory
```bash
cd /c/Users/YOUR_USERNAME/Downloads/telnet-ssh-wireshark-github-workflow
```
Replace the example path with the actual extracted folder location.

## 2. Review files and configure Git identity
```bash
git status
git config --global user.name "Your Name"
git config --global user.email "your-github-email@example.com"
```
If your Git identity is already configured, you do not need to set it again.

## 3. Initialize and commit
```bash
git init
git branch -M main
git add .
git status
```
Review `git status` carefully. Confirm no credentials, private keys, or unredacted packet captures are staged. Then:
```bash
git commit -m "Add Telnet and SSH Wireshark lab documentation"
```

## 4. Create the GitHub repository
Recommended repository name: `telnet-ssh-wireshark-analysis`

Suggested description:
`A hands-on Wireshark lab comparing Telnet plaintext traffic with encrypted SSH sessions, with documented methodology, redacted evidence, and security findings.`

On GitHub, create a **new empty repository** with that name. Do not initialize it with a README, license, or .gitignore because this project already contains those files.

## 5. Connect and push
Replace `YOUR_GITHUB_USERNAME` with your GitHub username:
```bash
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/telnet-ssh-wireshark-analysis.git
git push -u origin main
```
If `origin` already exists, inspect it first:
```bash
git remote -v
```
If it points to the wrong repository, correct it with:
```bash
git remote set-url origin https://github.com/YOUR_GITHUB_USERNAME/telnet-ssh-wireshark-analysis.git
git push -u origin main
```

## 6. Later updates
```bash
git add .
git status
git commit -m "Add redacted Telnet and SSH evidence"
git push
```

## Authentication note
GitHub no longer accepts an account password for HTTPS Git operations. Follow GitHub's current sign-in prompt or configure a Personal Access Token / SSH authentication securely. Never put a token in a command, file, screenshot, or repository.
