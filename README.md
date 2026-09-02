<div align="center">

# DEVDOCK

### Local-first GitHub workspace

A focused local developer dashboard for GitHub profiles, repositories, files, activity, issues, pull requests, releases, and repository actions.

![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white) ![Vite](https://img.shields.io/badge/Vite-8-646CFF?logo=vite&logoColor=white) ![License](https://img.shields.io/badge/License-MIT-yellow.svg)

</div>

---

## 🧭 What is DevDock?

DevDock is a local-first GitHub workspace that keeps common GitHub tasks inside one clean dashboard. It combines repository browsing, public user search, activity, file inspection, editing, commits, ZIP downloads, issues, pull requests, releases, account tools, and a dark glassmorphism interface.

## 🖼️ Concept

The visual concept is based on the supplied DevDock dashboard screens: navigation, GitHub connection state, account statistics, metric cards, activity stream, recent activity, and repository workspace.

<p align="center"><a href="./docs/devdock-concept.svg"><img src="./docs/devdock-concept.svg" alt="DevDock dashboard concept" width="1000" /></a></p>

## ✨ Features

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

## 🧰 Tech stack

React 19, TypeScript 5, Vite 8, Tailwind CSS, React Router, Lucide React, Recharts, Vitest, ESLint.

## 📋 Requirements

- Node.js 18+
- npm 9+
- Git

Check versions:

```bash
node --version
npm --version
git --version
```

## 🚀 Quick start

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

**Run the build immediately after installation and before starting Vite.** This verifies TypeScript, Vite, CSS processing, and the dependency tree.

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

Open `Settings -> Account` and enter your GitHub username and a fine-grained Personal Access Token.

Never commit tokens, private keys, secrets, or credential-bearing `.env` files.

## 🔐 GitHub API permissions

For the **full administrative feature set**, the fine-grained token must include the permissions required by the actions you use.

| Operation | Permission |
| --- | --- |
| Repository files / commits | Contents: Read and write |
| Repository administration | Administration: Read and write |
| Issues | Issues: Read and write |
| Pull requests | Pull requests: Read and write |
| Repository metadata | Metadata: Read-only |
| Account actions | Matching account permissions |

For administrative repository controls, **Administration: Read and write** is required. Limit the token to the repositories and permissions you actually need.

## ▶️ Commands

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

## 🗂️ Project structure

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
├── index.html
├── package.json
├── postcss.config.js
├── tailwind.config.js
├── tsconfig.json
├── tsconfig.app.json
├── tsconfig.node.json
└── vite.config.ts
```

## 🎨 Visual style

Near-black surfaces, glass-like panels, subtle borders, compact metadata, restrained cyan/blue accents, rounded cards, clear status states, and responsive navigation.

## 🧯 Troubleshooting

### Build fails

```bash
npm install
npm run build
```

Fix the first TypeScript/Vite error shown by the build.

### Windows clean reinstall

```powershell
Remove-Item -Recurse -Force node_modules
Remove-Item -Force package-lock.json -ErrorAction SilentlyContinue
npm install
npm run build
npm run dev
```

### Linux / macOS clean reinstall

```bash
rm -rf node_modules package-lock.json
npm install
npm run build
npm run dev
```

### Port 5173 is busy

```bash
npm run dev -- --port 5174
```

### GitHub API requests fail

Check username, token validity, repository scope, and the permissions required by the operation.

## 🔧 Development workflow

```bash
git pull
npm install
npm run build
npm run dev
```

After changes:

```bash
npm run lint
npm run test
npm run build
git add .
git commit -m "feat: update DevDock"
git push
```

## 📦 Production

```bash
npm run build
npm run preview
```

Deploy the generated `dist/` directory. Never hard-code a personal GitHub token into a public deployment.

## 📄 License

MIT License.
