# DEVDOCK

## Quick start

```bash
git clone https://github.com/pucun851/github-devdock.git
cd github-devdock
npm install
npm run build
npm run dev
```

Run `npm run build` immediately after `npm install` to verify TypeScript, Vite, CSS tooling, and dependencies before starting the dev server.

The concept preview is in `docs/devdock-concept.svg`.

## GitHub API permissions

For the full administrative feature set, the fine-grained GitHub token must include the permissions required by each operation.

| Operation | Permission |
| --- | --- |
| Files / commits | Contents: Read and write |
| Repository administration | Administration: Read and write |
| Issues | Issues: Read and write |
| Pull requests | Pull requests: Read and write |
| Repository metadata | Metadata: Read-only |
| Account actions | Matching account permissions |

Never commit tokens, private keys, secrets, or credential-bearing `.env` files.

## Commands

`npm run dev` - development server.

`npm run build` - production build in `dist/`.

`npm run preview` - preview production build.

`npm run test` - Vitest.

`npm run lint` - ESLint.

## Troubleshooting

Windows clean reinstall:

```powershell
Remove-Item -Recurse -Force node_modules
Remove-Item -Force package-lock.json -ErrorAction SilentlyContinue
npm install
npm run build
npm run dev
```

Port 5173 busy:

```bash
npm run dev -- --port 5174
```

## License

MIT License.
