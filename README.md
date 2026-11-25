# Website monitoring

GitHub Actions checks the six websites in this repository. Each workflow can also run manually.

| Workflow | Schedule | What it reports |
| --- | --- | --- |
| Uptime check | Every five minutes | Retries a failed homepage request and opens a labeled outage issue if the retry fails. Closes the issue after recovery. |
| Lighthouse CI | Mondays at 6:00 a.m. Central | Saves mobile performance, accessibility, best practices and SEO scores in `lighthouse/latest.json`. Opens an issue for scores below target. |
| Sitemap link check | Mondays at 6:30 a.m. Central | Checks URLs in each sitemap, including child sitemaps. Opens an issue when it finds problems. |
| SSL and security headers | Mondays at 7:00 a.m. Central | Checks certificate expiry and response headers. Opens an issue for certificates with fewer than 21 days left or a missing header. |
