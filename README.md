[README.md](https://github.com/user-attachments/files/33802387/README.md)
# mattslote.com
Website for sharing projects
# mattslote.com

Static site listing personal app projects. No build step.

- `index.html` renders cards from `projects.json`
- To add or update a project, edit `projects.json` and push. Cloudflare redeploys automatically.

## Deploy on Cloudflare Pages (one-time)

1. Push this folder to a GitHub repo.
2. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git → pick the repo.
3. Framework preset: None. Build command: leave empty. Build output directory: `/`.
4. After the first deploy, add `mattslote.com` under the project's Custom domains.

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
