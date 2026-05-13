# numbatmath-landing

Public marketing + legal site for **Numbat Math** at <https://numbatmath.com>.

Static HTML served by GitHub Pages. No build step.

## Pages

- `index.html` — landing page (hero, features, company info)
- `privacy.html` — privacy policy (source of truth: copy + paste from the iOS app repo's `PRIVACY_POLICY.md`)

## Deployment

- **CNAME** file pins the custom domain to `numbatmath.com`.
- **.nojekyll** disables GitHub's default Jekyll processing — we ship plain HTML.
- Push to `main` and GitHub Pages serves from the repo root.

## DNS setup at Namecheap (one-time)

Point `numbatmath.com` at GitHub Pages by adding these records in **Namecheap → Domain List → Manage → Advanced DNS**:

| Type | Host | Value | TTL |
|---|---|---|---|
| A | @ | 185.199.108.153 | Auto |
| A | @ | 185.199.109.153 | Auto |
| A | @ | 185.199.110.153 | Auto |
| A | @ | 185.199.111.153 | Auto |
| CNAME | www | yousefandsanad-lang.github.io | Auto |

Remove any existing "URL Redirect" records that conflict with these.

In GitHub: **Settings → Pages → Custom domain** → enter `numbatmath.com` → wait for the green check → tick "Enforce HTTPS" once the certificate provisions (5–15 min).

## Updating the privacy policy

The canonical source is `PRIVACY_POLICY.md` in the iOS app repo. When that file changes:

1. Copy the changes into `privacy.html` here (keep the existing HTML structure).
2. Bump the "Last updated" date in both places.
3. Commit + push. GitHub Pages redeploys in ~30 seconds.

## Operator

Yousef and Sanad LLC, d/b/a Numbat Math. Contact: <support@numbatmath.com>.
