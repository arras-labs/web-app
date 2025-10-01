# Web App

## Purpose
Front-end application (end-user & operator UI). Reads on-chain and calls server APIs.

## Responsibilities
- Implement user workflows and views
- Use **read-only** on-chain calls where appropriate
- Delegate **writes** to `backend-api`

## Interfaces (in / out)
- **Out:** HTTP to **backend-api**
- **In (artefacts):** **ABIs** from `contracts` for client-side decoding (read-only)

## Interactions with other repositories
- **backend-api:** main data/API provider
- **contracts:** ABIs for client-side types/decoding
- **deploy:** local dev orchestration and environment wiring

## Directory layout (provisional)
- `src/` application code
- `public/` static assets
- `Dockerfile` container build

## Local development
- Install dependencies: `npm ci`
- Start the dev server (see `package.json` scripts)
- Env in `.env.local` (never commit secrets)

## Testing
- Unit/component tests as added (e.g. Vitest/Jest/RTL)

## CI/CD
- Lint & tests on PR/push
- Build (and optionally containerise) on push to `main`

## Versioning & releases
- Front-end artefacts or container images; deployed via `deploy`
