# Security policy

Please **don't** report security problems in public issues.
Email yegineni@zohomail.in with the details (version, steps to reproduce). You'll get a reply within
5 working days, and a fix or mitigation plan as soon as possible.

## Recommended deployment
- Use the least-privilege monitoring logins from the setup scripts (SELECT on named msdb tables only,
  not `db_datareader`).
- The desktop app listens on 127.0.0.1 only.
- For a shared installation, use server mode behind HTTPS (the included IIS setup script does this) with
  sign-in on. Until sign-in is on, SQL Monitor answers only requests from the computer it runs on.
- Give each person their own account and the lowest role they need (viewer, operator, admin).
- Back up the data folder including its key file; without the key, saved server passwords can't be read.

## Built-in protections
- Sign-in with hashed passwords, throttling after repeated failures, sign-out on browser close and after
  idle time, audit log of sign-ins and changes.
- Cross-site request protection on every change; secure, `__Host-` cookies behind HTTPS.
- Single sign-on headers are only trusted from listed proxy addresses.
- API tokens are named, role-limited and stored hashed.
