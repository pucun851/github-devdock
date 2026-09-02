# DevDock

DevDock is a local-first GitHub workspace for browsing GitHub data and performing common repository operations from one interface.

## Highlights

- GitHub profile and repository dashboard
- Public user and repository search
- Contribution calendar with year switching
- Repository file browser with folder navigation
- Text editor with commit support
- File and folder upload helpers
- Repository ZIP downloads
- Issues, pull requests and releases views
- Star, watch, follow and unfollow actions where GitHub permissions allow them
- Account tools such as profile, email, organizations, notifications, SSH keys and gists
- Russian / English UI
- Configurable refresh interval
- Local credential storage in the browser
- Dark glassmorphism UI inspired by modern developer portfolio interfaces

## Local setup

```bash
npm install
npm run build
npm run dev
```

Then open the local Vite URL shown in the terminal.

## GitHub access

Open **Settings → Account** and provide:

- GitHub username
- Fine-grained Personal Access Token

The application stores these values locally in the browser. Do not commit a token, `.env` file, or other credentials to Git.

For write operations, the token needs the minimum GitHub permissions required by the specific action.

## Notes

DevDock is a local client. GitHub remains the source of truth for account and repository data.
