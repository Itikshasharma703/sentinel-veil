# Sentinel Veil — implementation plan

## Product scope
Sentinel Veil is a private-by-default showcase and technical brief for a defensive perimeter safety system. It explains a layered detection concept for difficult terrain without exposing deployment coordinates, operating patterns, or sensitive specifications. The product is explicitly **non-weaponized**: sensing can raise a reviewable alert, but it cannot autonomously engage, target, track a person for harm, or make a consequential decision without an authorized human.

## Implementation approach
- Build a single-page React/Vite experience with anchored sections instead of a dashboard that implies operational authority.
- Use a small client-side simulation to demonstrate how an optical/laser-adjacent signal is never enough by itself: observe → correlate → classify → human review → resolve.
- Keep data local and illustrative. No camera feeds, biometric identification, location data, cloud AI calls, or hardware control are connected in this prototype.
- Include `docs/REPORT.md` as the expanded engineering report and root `README.md` as the step-by-step build and prototype guide.
- Serve `public/manus-routes.json` before the dev server starts, so the route inventory is explicit.
- Keep the managed project private and do not publish automatically. A shareable preview is the only URL delivered until the owner explicitly decides to publish.

## Design direction
- **Design movement:** field-notes editorial + calm mission-control instrumentation; precise, quiet, and human-readable rather than militaristic.
- **Core principles:** signal before spectacle; evidence over confidence; safety rails are visible; every alert has a human handoff.
- **Color philosophy:** deep blue-green conveys night operations and calm; warm signal yellow marks attention without implying danger; mint confirms evidence; coral is reserved for unresolved risk.
- **Layout paradigm:** asymmetric editorial flow with a left reading rail, wide evidence panels, and a vertical “signal path” that carries the visitor through the concept.
- **Signature elements:** a thin perimeter line, a four-stage signal path, and instrument-style micro labels such as `TRUST GATE / HUMAN REVIEW`.
- **Interaction philosophy:** every interactive control explains what it proves and what it does not prove. The demo ends in either `cleared` or `review required`, never automatic action.
- **Animation:** short, low-amplitude pulses for sensor activity; no flashing red alerts; respect reduced-motion preferences; stagger only to clarify sequence.
- **Typography:** use a clean system sans stack for body copy and a condensed mono-like stack for telemetry labels; strong H1, restrained eyebrow labels, generous line-height.
- **Brand essence:** “A calmer way to prove a perimeter signal before people act.” For safety teams and prototype engineers. Personality: rigorous, restrained, accountable.
- **Brand voice:** factual and reassuring. Example lines: “A signal is not a threat.” / “Escalate only when evidence survives the weather.”
- **Wordmark & logo:** a split-ring “SV” mark with one open segment, representing a perimeter that stays observable without pretending to be impenetrable.
- **Signature brand color:** signal saffron `#F6C75B` on deep field `#081A1F`.

## Project structure
```text
client/
  index.html                 # metadata + meaningful no-script fallback
  public/manus-routes.json   # declared page routes
  src/App.tsx                # app shell and route
  src/pages/Home.tsx         # showcase page and interactive concept console
  src/index.css              # visual system and responsive layout
components/                  # starter UI primitives retained for future use
docs/REPORT.md               # expanded engineering report
README.md                    # build, prototype and hardware handoff guide
plan.md                     # this plan
TODO.md                     # outcome-based delivery status
```

## Build workflow
1. Implement content, visual system, and the local simulation.
2. Run TypeScript diagnostics and `pnpm check`.
3. Start the static preview with `pnpm dev:static` on the configured port.
4. Verify the preview and `/manus-routes.json`; capture a screenshot only if visual inspection is needed.
5. Build with `pnpm build:static`.
6. Commit intended files and push to the managed canonical branch for a checkpoint. Keep `auto_publish` off; publication is a separate owner decision.

## Explicit boundaries
- No harmful or high-power laser guidance. Use only compliant, eye-safe optical sensing concepts in future engineering reviews.
- No face recognition, identity inference, biometric watchlists, or persistent person tracking in this prototype.
- No autonomous response, weapon control, or “scan and act” loop.
- No real operational data, coordinates, sensor keys, or site-specific performance claims.
- Any future hardware pilot requires legal, safety, privacy, cybersecurity, and independent field validation review.
