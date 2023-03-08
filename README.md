<p align="center"><img src="https://raw.githubusercontent.com/has-co-de/.github/has-co.de.png" height="128"></p>
<h1 align="center">Open Domains</h1>

<p align="center">
  <a href="https://github.com/has-co-de/register/tree/main/domains"><img src="https://img.shields.io/github/directory-file-count/has-co-de/register/domains?label=domains&style=for-the-badge&type=file"></a>
  <a href="https://github.com/has-co-de/register/issues"><img src="https://img.shields.io/github/issues-raw/has-co-de/register?label=issues&style=for-the-badge"></a>
  <a href="https://github.com/has-co-de/register/pulls"><img src="https://img.shields.io/github/issues-pr-raw/has-co-de/register?label=pull%20requests&style=for-the-badge"></a>
</p>

<p align="center">Free subdomains for personal sites, open-source projects, and more.</p>

## Notice

While we do support NS records we now only now accept NS records for valid reasons.

We have the right to take away your subdomain with no notice.

## Domains

> Wildcard domains (like `*.also.has-co.de`) are supported too, but the reason for their registration should be very clear and described in detail.

### Unsupported Services

We currently do not support Cloudflare (for NS), Netlify (for website) or Vercel (for websites).

## Register a Domain

1. **Star** and **[Fork](https://github.com/has-co-de/register/fork)** this repository
2. Add a new file called `example.has-co.de.json` in the `/domains` folder to register `example` subdomain
3. Edit it (below is just an **example**, provide a **valid** JSON file with your needs, the format is very strict; format you can [check here](https://jsonlint.com)):

```json
{
  "$schema": "../schemas/domain.schema.json",

  "description": "Project Description",

  "domain": "has-co.de",
  "subdomain": "example",

  "owner": {
    "repo": "https://github.com/username/repo",
    "email": "hello@example.com"
  },

  "record": {
    "A": ["1.1.1.1", "1.0.0.1"],
    "AAAA": ["::1", "::2"],
    "CNAME": "example.com",
    "MX": ["mx1.example.com", "mx2.example.com"],
    "NS": ["ns1.example.com", "ns2.example.com"],
    "TXT": ["example_verification=1234567890"]
  },

  "proxy": false
}
```

4. Your pull request will be reviewed and merged. Please don't ignore the pull request checklist. If you ignore the checklist, your pull request will be ignored too. _Make sure to keep an eye on it in case we need you to make any changes!_
5. After the pull request is merged, please allow up to 24 hours for the changes to propagate _(usually, it takes 5..15 minutes)_
6. Enjoy your new domain!

*Domains used for illegal purposes will be removed and permanently banned. Please, provide a clear description of your resource in the pull request.*