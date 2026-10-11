# app-store-pages

Redirect only.

## Public iOS API endpoint bootstrap

`https://kerothebosa.github.io/app-store-pages/config.json` is a **public, stable bootstrap address** that newer iOS builds can poll periodically. Its `apiBaseURL` is the **HTTPS API origin**, not the marketing website. The JSON must never contain API keys, authentication tokens, user information, or private configuration.

Before moving the API to a different domain, update `site/config.json` with the new HTTPS origin and merge/deploy this Pages repository. New iOS builds can then discover the endpoint without another App Store release. Old iOS builds that do not have bootstrap support still need a new app release.

Stable `/privacy/`, `/terms/`, and `/support/` redirect pages remain unchanged and independent of API bootstrap.
