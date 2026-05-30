# AGENTS.md

Guidance for AI agents working in this repository.

## Project status

This repository is currently a **scaffold only**: it contains `README.md` (`# my-portfolio`) and no application source, dependency manifests, or service definitions. There is nothing to lint, test, build, or run as an application yet.

When a portfolio stack is added (for example Vite, Astro, or Next.js), update this file with concrete commands and service notes.

## Cursor Cloud specific instructions

### What runs today

No application services are defined. End-to-end product testing is not applicable until source code and a package manager lockfile exist.

### Toolchain available on the VM

The cloud VM includes tooling suitable for typical portfolio development:

| Tool | Notes |
|------|--------|
| Node.js | v22.x (via environment) |
| npm | Available |
| pnpm | Available |
| Python 3 | Available for simple static servers or scripts |
| git | Repository cloned from `derickpaul09/my-portfolio` |

### Lint / test / build

Not configured in the repo. After adding a project (e.g. `package.json`), use the scripts defined there (`npm run lint`, `npm test`, `npm run dev`, etc.) and extend this section.

### Running a placeholder check

Until an app exists, you can confirm the VM can bind a port and serve files from the repo root:

```bash
python3 -m http.server 8080 --directory /workspace
```

Then open or `curl http://127.0.0.1:8080/README.md`.

### Update script behavior

The VM startup update script is a no-op (`true`) because there are no dependencies to refresh. After `package.json` (or equivalent) is added, change the update script to the appropriate install command (e.g. `pnpm install`).
