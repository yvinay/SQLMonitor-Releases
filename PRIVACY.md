# Privacy statement (beta)

**Short version: the software sends nothing about you or your databases to the developer.**

## What is stored, and where
- Server addresses, settings, collected metrics, query text, deadlock reports and history are stored on the
  computer where the software runs (`%APPDATA%\SQLMonitor` for the desktop app), or on your own server for
  a central installation.
- Passwords, API keys and webhook URLs are stored in Windows Credential Manager, or an encrypted file when no
  credential store is available. They are never written to the settings file in plain text.

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
