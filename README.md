# Cloudflare Turnstile (cloudflare-turnstile)

Cloudflare Turnstile is Cloudflare's free, smart CAPTCHA alternative
that verifies real users without sending traffic through Cloudflare's
network. It runs non-interactive client-side challenges (proof-of-work,
proof-of-space, web API probing, browser-integrity checks) and returns
a short-lived token that the relying server validates against the
Turnstile siteverify endpoint. Turnstile offers three widget modes —
Managed (risk-adapted), Non-interactive (no user gesture), and Invisible
(fully hidden) — and is designed to run on any website regardless of
whether the site is proxied through Cloudflare. The product is targeted
at developers who want a privacy-respecting reCAPTCHA replacement.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/cloudflare-turnstile/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/cloudflare-turnstile/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Provider
- **Access:** Public

## Tags

- CAPTCHA
- Bot Defense
- Cloudflare
- Turnstile
- Privacy
- reCAPTCHA Alternative
- Edge Security

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-23

## APIs

### Turnstile Siteverify API

The Turnstile siteverify endpoint accepts a token produced by the
browser widget along with the site's secret key and an optional
remote IP and idempotency key, and returns a JSON verdict with
success, hostname, action, cdata, and any error codes. This is the
canonical server-side check that authorizes a form submission or
API call protected by Turnstile.

- **Human URL:** [https://developers.cloudflare.com/turnstile/get-started/server-side-validation/](https://developers.cloudflare.com/turnstile/get-started/server-side-validation/)
- **Base URL:** `https://challenges.cloudflare.com/turnstile/v0/siteverify`

#### Tags

- Siteverify
- Server-Side
- Token Verification

#### Properties

- [Documentation](https://developers.cloudflare.com/turnstile/get-started/server-side-validation/)
- [API Reference](https://developers.cloudflare.com/turnstile/get-started/server-side-validation/)
- [Endpoint U R L](https://challenges.cloudflare.com/turnstile/v0/siteverify)
- [Postman Collection](collections/cloudflare-turnstile.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudflare-turnstile.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Turnstile Client Widget

The Turnstile client widget renders the challenge in the browser.
It is loaded via a script tag at challenges.cloudflare.com/turnstile/v0/api.js
and configured with a sitekey, optional theme, action, cdata, and
callback functions. Widgets can be Managed, Non-interactive, or
Invisible.

- **Human URL:** [https://developers.cloudflare.com/turnstile/get-started/client-side-rendering/](https://developers.cloudflare.com/turnstile/get-started/client-side-rendering/)
- **Base URL:** `https://challenges.cloudflare.com/turnstile/v0/api.js`

#### Tags

- JavaScript
- Widget
- Frontend
- Managed
- Invisible

#### Properties

- [Documentation](https://developers.cloudflare.com/turnstile/get-started/client-side-rendering/)
- [Script U R L](https://challenges.cloudflare.com/turnstile/v0/api.js)
- [Examples](https://github.com/cloudflare/turnstile-demo-workers)
- [Postman Collection](collections/cloudflare-turnstile.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudflare-turnstile.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Turnstile Pre-Clearance

Pre-clearance lets a successful Turnstile challenge set a cookie
that Cloudflare-proxied properties can honor to skip subsequent
bot challenges for the same visitor, which is useful for single-page
applications and API-heavy flows.

- **Human URL:** [https://developers.cloudflare.com/turnstile/concepts/pre-clearance-support/](https://developers.cloudflare.com/turnstile/concepts/pre-clearance-support/)
- **Base URL:** `https://challenges.cloudflare.com/turnstile/v0/api.js`

#### Tags

- Pre-Clearance
- Cookies
- SPA

#### Properties

- [Documentation](https://developers.cloudflare.com/turnstile/concepts/pre-clearance-support/)
- [Postman Collection](collections/cloudflare-turnstile.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudflare-turnstile.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cloudflare Turnstile Management API

Turnstile widgets and analytics are managed through the broader
Cloudflare API, which exposes endpoints to list, create, update,
and rotate Turnstile sitekeys, retrieve analytics, and integrate
with account-level settings.

- **Human URL:** [https://developers.cloudflare.com/api/operations/challenges-widget-list-challenge-widgets](https://developers.cloudflare.com/api/operations/challenges-widget-list-challenge-widgets)
- **Base URL:** `https://api.cloudflare.com/client/v4`

#### Tags

- Management
- Provisioning
- Analytics

#### Properties

- [Documentation](https://developers.cloudflare.com/turnstile/reference/)
- [API Reference](https://developers.cloudflare.com/api/operations/challenges-widget-list-challenge-widgets)
- [Postman Collection](collections/cloudflare-turnstile.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudflare-turnstile.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Product Page](https://www.cloudflare.com/products/turnstile/)
- [Documentation](https://developers.cloudflare.com/turnstile/)
- [API Reference](https://developers.cloudflare.com/turnstile/reference/)
- [Dashboard](https://dash.cloudflare.com/?to=/:account/turnstile)
- [Blog](https://blog.cloudflare.com/turnstile-private-captcha-alternative/)
- [GitHub Organization](https://github.com/cloudflare)
- [Demos](https://github.com/cloudflare/turnstile-demo-workers)
- [Pricing](https://developers.cloudflare.com/turnstile/community/limits-and-pricing/)
- [L L Ms Txt](https://developers.cloudflare.com/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
