# kharchlog.in → kharchlog.com (GitHub Pages redirect)

Repo: https://github.com/Ahmedhussainpvtt/kharchlog-forwarding

Every path (e.g. `/features/?utm_source=chatgpt.com`) sends the browser to the same path on **kharchlog.com**.

## Enable GitHub Pages

Repo → **Settings → Pages**:
- Source: **Deploy from a branch**
- Branch: **main** / **/(root)**
- Custom domain: **kharchlog.in** (CNAME file is in the repo)

## DNS (GoDaddy)

1. Turn **OFF** Domain Forwarding for `kharchlog.in`
2. Add:

| Type | Name | Value |
|------|------|--------|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `Ahmedhussainpvtt.github.io` |

3. Wait for DNS + HTTPS (~10–30 min)

Test: `https://kharchlog.in/features/?utm_source=chatgpt.com`
→ `https://kharchlog.com/features/?utm_source=chatgpt.com`
