# MTA-STS policy

This directory is source material for the separate HTTPS host
`mta-sts.weber-wis.com`. It must not be deployed as a path below the main
website.

Before publishing `mode: enforce`, verify:

1. the active Microsoft 365 MX target;
2. that the `mx` pattern in `.well-known/mta-sts.txt` matches that target;
3. the `_mta-sts.weber-wis.com` TXT record and policy version;
4. valid HTTPS without redirects at
   `https://mta-sts.weber-wis.com/.well-known/mta-sts.txt`.
