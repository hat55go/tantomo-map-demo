# Deployment-only demo repository

## Purpose and success condition

Serve the approved, mobile-first Tantomo MAP development demo through GitHub Pages. Success means the public HTTPS URL loads the map and store details, with no unapproved photographs, credentials, private business data, or billable Google API requests.

## Stack and directories

- Prebuilt React / TypeScript / Vite application, with Leaflet.
- `docs/`: generated deployment artifacts and `.nojekyll`; Pages source is `main:/docs`.
- Source development and internal documentation live in a separate private repository.
- Local run, test, lint, and build commands: not configured in this deployment repository.

## Updates and Git

- Build and verify in the private source project; never hand-edit minified assets here.
- Copy only the verified demo artifacts and preserve `.nojekyll`.
- Use `feature/<name>` branches and pull requests after the initial scaffold commit.
- Use concise English Conventional Commits.
- Do not publish unrelated files, force-push, or discard user changes.

## Verification and safety

- Before each commit, inspect the complete staged changes and scan for secrets and private data.
- Verify the deployed HTML and assets match the intended build.
- Check mobile layout, map loading, search, store cards, and destination-only external map links.
- Ensure review-only photos and Google API scripts cannot load, including with development query flags.
- Retain the development notice, information date, and visible linked GSI tile attribution.
- Do not add analytics, paid services, new permissions, or production claims without explicit approval.
- Never commit credentials, `.env` contents, unapproved images, internal documents, or private application data.
