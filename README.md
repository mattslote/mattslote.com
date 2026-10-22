# mattslote.com

Static site listing personal app projects. No build step.

- `public/index.html` renders cards from `public/projects.json`
- To add or update a project, edit `public/projects.json` and push to `main`. Cloudflare redeploys automatically.
- Only `public/` is served (see `wrangler.jsonc`). Keep everything else out of it.

## Hosting

Cloudflare Workers (static assets), deployed by Workers Builds on each push with `npx wrangler deploy`.
Live at https://mattslote-com.mattslote.workers.dev. Custom domain: Workers & Pages, mattslote-com, Settings, Domains & Routes, Add, Custom domain.

## projects.json entry

```json
{
  "slug": "my-app",
  "name": "My App",
  "status": "In development",
  "summary": "One or two sentences.",
  "tags": ["tag"],
  "updated": "YYYY-MM-DD",
  "notes": ["Short bullet", "Another"],
  "link": "https://example.com"
}
```

`link` is optional (leave empty to hide it). Cards sort by `updated`, newest first.
