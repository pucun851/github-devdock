# DEVDOCK

Local-first GitHub workspace.

## Concept

<p align="center"><a href="./docs/devdock-concept.svg"><img src="./docs/devdock-concept.svg" alt="DevDock dashboard concept" width="1000" /></a></p>

The concept is based on the provided DevDock dashboard screens: navigation, GitHub connection state, account statistics, metrics, activity stream, recent activity, and repository workspace.

## Quick start

### 1. Clone

```bash
git clone https://github.com/pucun851/github-devdock.git
cd github-devdock
```

### 2. Install dependencies

```bash
npm install
```

### 3. Build the project

Run the build immediately after installation and before starting Vite. This verifies TypeScript, Vite, CSS processing, and the dependency tree.

```bash
npm run build
```

A successful build creates `dist/`.

### 4. Start development

```bash
npm run dev
```

Open the URL printed by Vite, normally `http://localhost:5173/`.

### 5. Connect GitHub

Open `Settings -> Account` and enter your GitHub username and fine-grained Personal Access Token.

## GitHub API permissions

For the full administrative feature set:

| Operation | Permission |
| --- | --- |
| Repository files / commits | Contents: Read and write |
| Repository administration | Administration: Read and write |
| Issues | Issues: Read and write |
| Pull requests | Pull requests: Read and write |
| Repository metadata | Metadata: Read-only |
| Account actions | Matching account permissions |

For administrative repository controls, **Administration: Read and write** is required. Limit the token to the repositories and permissions you actually need. Never commit tokens or secrets.

## Commands

```bash
npm run dev
npm run build
npm run preview
npm run test
npm run lint
```

Recommended verification:

```bash
npm install
npm run build
npm run lint
npm run test
npm run dev
```

## Features

- GitHub profile and repository dashboard
- Public user and repository search
- Contribution calendar
- Repository file browser
- Text editing and commit support
- ZIP downloads
- Issues, pull requests, and releases
- Account tools
- Russian / English UI
- Configurable refresh interval
- Local browser credential storage
- Dark glassmorphism developer UI

## Structure

```text
github-devdock/
├── docs/
│   ├── concept.md
│   └── devdock-concept.svg
├── src/
│   ├── App.tsx
│   ├── main.tsx
│   ├── index.css
│   └── styles/
│       └── index.css
├── tests/
├── package.json
├── postcss.config.js
├── tailwind.config.js
├── tsconfig.json
├── tsconfig.app.json
├── tsconfig.node.json
└── vite.config.ts
```

## Troubleshooting

Build errors:

```bash
npm install
npm run build
```

Windows clean reinstall:

```powershell
Remove-Item -Recurse -Force node_modules
Remove-Item -Force package-lock.json -ErrorAction SilentlyContinue
npm install
npm run build
npm run dev
```

Port change:

```bash
npm run dev -- --port 5174
```

If GitHub requests fail, check token validity, repository scope, and the permissions required by the operation.

## Production

```bash
npm run build
npm run preview
```

Deploy the generated `dist/` directory. Never hard-code a personal GitHub token into a public deployment.

## License

MIT License.
