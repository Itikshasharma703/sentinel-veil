# Sentinel Veil — AI Perimeter Safety

Sentinel Veil is a private-by-default showcase for a **defensive, human-supervised perimeter monitoring concept**. It demonstrates how an optical/laser-adjacent signal can be checked against additional evidence before an authorized operator reviews an alert.

> A signal is not a threat. An alert is not a verdict.

## Safety boundary

This project is intentionally non-weaponized. It does not include autonomous engagement, harmful/high-power laser guidance, identity or face recognition, biometric watchlists, covert mass surveillance, or hardware control. All event handling ends in `cleared` or `review required`.

Do not add real coordinates, operational layouts, credentials, site-specific performance claims, or sensitive deployment details to this repository or the showcase site.

## What is included

- React/Vite showcase website with an interactive illustrative signal-path console.
- Architecture overview and challenge/mitigation matrix.
- Detailed engineering report in [`docs/REPORT.md`](docs/REPORT.md).
- Phased hardware/prototype handoff, privacy, cybersecurity, and validation guidance.
- Managed WebDev route manifest at `client/public/manus-routes.json`.

## Run locally

```bash
pnpm install --frozen-lockfile
pnpm check
pnpm dev:static
```

Open the preview on the configured port (default `3000`). The app is static and uses only local illustrative state; it does not connect to cameras, sensors, AI APIs, databases, or external hardware.

Build the static output:

```bash
pnpm build:static
```

## Project structure

```text
client/src/pages/Home.tsx  # showcase page and local simulation
client/src/index.css       # visual system and responsive styles
client/index.html          # metadata and no-script summary
client/public/manus-routes.json
plan.md                    # implementation and design plan
TODO.md                    # delivery outcomes
README.md                  # this handoff guide
docs/REPORT.md             # expanded engineering report
```

## How to extend safely

1. Add simulator scenarios before adding physical hardware.
2. Define evidence quality, abstention, reason codes, and stop conditions before training a model.
3. Use certified, eye-safe, non-invasive sensors only after legal and independent safety review.
4. Keep identity recognition and persistent person tracking out of scope.
5. Keep any alert pathway human-reviewed; never connect the demo to actuation or force.
6. Test by weather, terrain, lighting, wildlife, sensor health, power, communications, and operator workload—not only by distance.
7. Run a permissioned, clearly marked test site with consent and an independent observer.

## Suggested next folders for a future prototype

```text
prototype/
  simulator/       # synthetic event generator and replay runner
  edge/            # sensor health + timestamp + quality gate only
  fusion/          # modality alignment and abstention logic
  review-ui/       # evidence card with reason codes and audit record
  test-data/       # synthetic/consented data, never operational data
  safety/          # approvals, stop conditions, privacy and cyber review
```

## Private-by-default note

The managed project is not configured for automatic publication. Share the preview only with intended reviewers, and publish only after removing operationally sensitive content and completing the required safety/privacy review.
