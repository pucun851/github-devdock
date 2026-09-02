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

This preview shows the real DevDock interface used as the visual reference for the project.

<p align="center"><a href="./docs/devdock-concept.svg"><img src="./docs/devdock-concept.svg" alt="DevDock interface concept" width="1000" /></a></p>

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

### 5. Connect GitHub API

DevDock uses a **GitHub Personal Access Token (PAT)** for GitHub API access. For the complete feature set, create a **fine-grained personal access token** and allow it to access the repositories you need.

👉 **Create a GitHub fine-grained token:**

https://github.com/settings/personal-access-tokens/new

GitHub's official token documentation: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens

Inside DevDock, open:

```text
Settings → Account
```

Then enter:

```text
GitHub username
GitHub Personal Access Token
```

### 🔐 Required permissions

For the **full administrative feature set**, the token must include the permissions required by the operations you use.

| Operation | Fine-grained permission |
| --- | --- |
| Read repository data | Metadata: Read-only |
| Create / edit / delete repository files | Contents: Read and write |
| Create commits | Contents: Read and write |
| Repository administration | **Administration: Read and write** |
| Issues | Issues: Read and write |
| Pull requests | Pull requests: Read and write |
| Repository metadata | Metadata: Read-only |

**Important:** if you want DevDock to perform repository administration actions, **Administration → Read and write is required**.

Fine-grained tokens can be restricted to selected repositories and specific permissions. GitHub recommends fine-grained tokens when they fit the use case. citeturn698448search4turn698448search2

### ⚠️ Security

Treat your token like a password. Never commit it to GitHub, place it in source code, or publish it in screenshots/logs. citeturn698448search4

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

Near-black surfaces, glass-like panels, subtle borders, compact metadata, restrained accents, rounded cards, clear status states, and responsive navigation.

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

Check your username, token validity, selected repository access, and the permissions required by the operation. Administrative actions require **Administration: Read and write**.

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

## 📚 Official GitHub API docs

- Personal access tokens: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens
- Fine-grained token permissions: https://docs.github.com/en/rest/authentication/permissions-required-for-fine-grained-personal-access-tokens
- REST API reference: https://docs.github.com/en/rest

## 📄 License

MIT License.
