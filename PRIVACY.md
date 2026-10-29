# Privacy statement (beta)

**Short version: the software sends nothing about you or your databases to the developer.**

## What is stored, and where
- Server addresses, settings, collected metrics, query text, session details (user, machine, application),
  blocking and deadlock reports and history are stored on the computer where the software runs
  (`%APPDATA%\SQLMonitor` for the desktop app), or on your own server for a shared installation
  (`%ProgramData%\SQLMonitor`, readable only by administrators and the service account).
- Passwords, API keys and webhook URLs are stored in Windows Credential Manager, or an encrypted file whose
  key is kept separately. They are never written to the settings file in plain text.
- On a shared installation: user names, password hashes (never the passwords) and an audit log of sign-ins
  and changes, on your server.
- Inventory reports are generated on demand and downloaded to your computer. Passwords, password hashes,
  job step commands and mail content are never read.

## Network connections the software makes
| Connection | When | What is sent |
|---|---|---|
| Your database servers | While monitoring | Read-only monitoring queries |
| `api.github.com` | Update check, every 6 hours (can be turned off) | A request for the public release list; no identifiers |
| `api.anthropic.com` | Only if you turn on AI explanations and add your own key | The selected finding and query text with literal values replaced by `?` (query text can be excluded) |
| Slack / Teams / PagerDuty / your webhooks | Only if you configure notification routes | Alert messages |

## Telemetry
None. There is no usage tracking, crash reporting or analytics in the beta.

## Feedback
Feedback you post on GitHub is public and subject to GitHub's privacy policy. Don't include server names,
query text or other confidential information unless you are comfortable making it public.

## Contact
yegineni@zohomail.in
