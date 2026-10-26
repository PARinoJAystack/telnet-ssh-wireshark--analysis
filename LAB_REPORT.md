# Lab Report: Examining Telnet and SSH in Wireshark

## 1. Objective
Compare a Telnet session and an SSH session in Wireshark, focusing on the visibility of session data and the security benefit of encryption.

## 2. Environment
| Item | Actual value |
|---|---|
| Date performed | TODO |
| OS / lab workstation | TODO |
| Wireshark version | TODO |
| Capture interface | TODO |
| Client and server endpoint | TODO |
| Telnet service details | TODO |
| SSH service details | TODO |

## 3. Methodology
Summarize the steps you actually followed. Include the display filters used and how you opened Follow → TCP Stream.

TODO

## 4. Observations

### Telnet
- Display filter used: `telnet`
- Was session content readable in Follow TCP Stream? TODO
- What kinds of information were visible? Describe without reproducing credentials. TODO
- Evidence filename: TODO

### SSH
- Display filter used: `ssh`
- Was the interactive session content readable in Follow TCP Stream? TODO
- What did the stream look like compared with Telnet? TODO
- Evidence filename: TODO

## 5. Comparison

| Property | Telnet | SSH |
|---|---|---|
| Default transport port | TCP 23 (conventional) | TCP 22 (conventional) |
| Session confidentiality | No encryption by default | Encrypts session traffic |
| Credentials / commands visible as plaintext in captured stream | Typically yes | Protected by encryption after protocol setup |
| Appropriate for secure remote administration | No, avoid on untrusted networks | Yes, when configured securely |

## 6. Security analysis
Explain the risk of plaintext credentials and session content on Telnet. Explain how SSH encryption protects confidentiality and why host-key verification and secure configuration still matter.

TODO

## 7. Reflection question
**Why is SSH preferred over Telnet for remote connections?**

Draft your answer from your observations: SSH encrypts the session, helping protect credentials and command data from being read by someone who can observe the network. Telnet does not encrypt its session by default, so sensitive information can be exposed in plaintext. SSH must still be configured and used securely.

## 8. Conclusion
Summarize what your own captures demonstrated. Do not claim results you did not observe.

TODO

## 9. Evidence index
| Evidence | Relative path | Redacted / safe to share? |
|---|---|---|
| Telnet display-filter screenshot | TODO | TODO |
| Telnet stream screenshot | TODO | TODO |
| SSH display-filter screenshot | TODO | TODO |
| SSH stream screenshot | TODO | TODO |
