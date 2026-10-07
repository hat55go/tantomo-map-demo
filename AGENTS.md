# Deployment-only demo repository

## Purpose and success condition

Serve the approved, mobile-first Tantomo MAP development demo through GitHub Pages. Success means the public HTTPS URL loads the map and store details, with no unapproved photographs, credentials, private business data, or billable Google API requests.

## Stack and directories

- Prebuilt React / TypeScript / Vite application, with MapLibre GL JS and a self-contained worker.
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
- Retain the development notice, benefit information date, linked GSI pale tile attribution, and extra source credit at zoom 7–8.
- Distinguish store/facility coordinates from approximate address-block points. Keep unresolved locations searchable without invented pins or unknown-branch navigation links.
- Include the attributed public ODbL extract for OSM-derived store positions, but no private review caches or merchant intake data.
- The tile service has no availability guarantee; do not replace it with a paid service without approval.
- Do not add analytics, paid services, new permissions, or production claims without explicit approval.
- Never commit credentials, `.env` contents, unapproved images, internal documents, or private application data.
