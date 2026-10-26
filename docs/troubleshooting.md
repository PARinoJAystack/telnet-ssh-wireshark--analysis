# Troubleshooting Notes

## No Telnet packets appear
- Confirm the capture started before initiating the test session.
- Verify the selected interface is the one carrying the test traffic. For a localhost exercise, use loopback if supported by the workstation.
- Confirm the Telnet service is running and accepting connections on the target system.
- Check whether the service is listening on the expected port in your own lab.

## No SSH packets appear
- Confirm SSH is enabled and listening on the target endpoint.
- Verify the capture interface and start capture before connecting.
- Confirm the SSH client can connect independently of Wireshark.

## Display filter shows no packets
- Use the protocol filter matching the traffic you generated (`telnet` or `ssh`).
- If the traffic is not dissected as expected, inspect TCP packets and confirm the connection/port and capture interface.

## Follow TCP Stream looks different from expected
- Confirm you selected a packet from the correct session.
- Telnet session data may be readable as plaintext.
- SSH session payload is encrypted; protocol negotiation metadata may still be identifiable.
- Never save or publish an unredacted Telnet stream containing credentials.

## Git safety check
Before committing, run:
```bash
git status
git diff --cached --stat
git diff --cached
```
Remove secrets and sensitive captures from staging before commit.
