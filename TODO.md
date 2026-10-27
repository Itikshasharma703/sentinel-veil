# Sentinel Veil delivery checklist

## Showcase experience
- [x] The website presents a defensive perimeter-safety concept for difficult areas and clearly states that it is non-weaponized and private-by-default.
- [x] The website explains the signal path as observe → correlate → classify → human review, with an explicit statement that one optical/laser-adjacent signal never creates an automatic action.
- [x] The site includes responsive navigation, hero positioning, system architecture, challenge matrix, prototype roadmap, safety boundaries, and documentation links.
- [x] The site includes a local interactive console that lets a visitor compare a wildlife-like event with a human-review-required event; both flows remain illustrative and do not control hardware.

## Engineering documentation
- [x] `docs/REPORT.md` covers requirements, architecture, false-alarm reduction, weather/terrain resilience, data and AI pipeline, privacy, cybersecurity, testing, and phased implementation.
- [x] `README.md` contains setup steps, project structure, prototype boundaries, and a staged hardware handoff.
- [x] The README and report avoid operationally sensitive deployment coordinates, harmful laser specifications, autonomous engagement logic, and identity surveillance instructions.

## Runtime and quality
- [x] TypeScript diagnostics are registered through the managed WebDev host.
- [x] `client/public/manus-routes.json` declares the complete current page route set.
- [x] Run `pnpm check` and resolve any actionable diagnostics.
- [x] Run the static dev server and verify the preview plus `/manus-routes.json`.
- [x] Run `pnpm build:static` and inspect the generated output.
- [x] Commit the intended files to the managed canonical branch and verify the pushed checkpoint SHA `d99583da2974e0be21610c174a59ab13150eebdd`.
- [x] Keep automatic publishing disabled until the owner decides that the idea is ready for broader sharing.
