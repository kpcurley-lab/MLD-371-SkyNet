# Validation record

Date: September 10, 2026. Tested the tutorial website, not a student-generated agenda implementation.

## Passed

- Local HTTP preview returns 200 and serves the authored HTML, CSS and JavaScript.
- JavaScript syntax check (`node --check dist/app.js`) and tracked diff whitespace check (`git diff --check`).
- All eight lesson navigation links reach their matching fragment URLs.
- All 20 checkboxes can be selected. Per-section counts match 1, 2, 2, 1, 2, 7, 3, 2; overall reaches 100%.
- A single checkpoint reports 5%; both the single-check state and the full 100% state survive reload.
- OS selector shows matching macOS/Windows instructions; macOS preference survives reload; Windows selection restores Windows instructions.
- Reset opens a native modal with initial focus on Keep progress. Cancel retains progress. Escape dismisses without clearing. Confirm clears all checkmarks, and 0% survives reload. Test progress was cleared before handoff.
- Keyboard Space toggles a checkbox. Tab moves to the next link with a visible 3px focus outline. Native dialog cancellation via Escape works.
- Agenda-prompt and Git-version copy buttons report success through the live status area.
- Visual inspection at 390×844 and 1366×900; layout-width checks at 320 and 390 show no document-level horizontal overflow. Mobile lesson navigation scrolls within its own rail. Long prompt text wraps inside its panel.
- No browser console errors observed in the tested preview.

## Content and publication review

Opened official OpenAI, GitHub, Git, Microsoft and Apple documentation supporting the setup instructions. Links are adjacent to related instructions; the guide displays a last-verified date. The OpenAI app naming redirect is disclosed. A Git book link that returned 404 was replaced with GitHub's verified introduction. Sources are not guarantees that every account or installed version exposes identical menus.

GitHub Pages availability and workflow requirements were checked against official documentation. The workflow is manual-only (`workflow_dispatch`) and uploads only `dist`, never repository metadata or local preview files. It has not been executed. No external registration, visibility change, commit, push or publication was performed.

## Limits / remaining checks

- Browser clipboard readback returned an empty value even though the page's Clipboard API call resolved successfully. Actual pasted payloads were not independently verified; check these in the target browser before class. The app catches rejected copy calls and provides manual-selection guidance, but that rejection path was not forced in browser QA.
- Storage-blocked and corrupt-storage behavior was reviewed in code, not exercised in a browser with storage disabled. Both storage access and parsing are guarded; the guide renders as static HTML independently of JavaScript.
- No full screen-reader audit, exhaustive keyboard traversal, physical phone test, Safari or Firefox run, or browser-level JavaScript-disabled test was performed.
- Did not install student tools, create student accounts, accept invitations, authenticate student Git, generate a separate agenda app, or perform a real student commit/push. Those are tutorial instructions, not completed tests.
- The owner's GitHub plan, repository Pages eligibility and organization policies have not been confirmed. Hosting requires explicit approval and an eligibility check without changing visibility.
- Published-origin asset loading, signed-out visitor access and the deployment workflow must be tested after publication is approved.

## Repeat before class

Open each lesson; check and uncheck progress; reload; cancel and confirm reset; switch OS; copy each command/prompt and paste into a harmless text editor; keyboard-traverse controls; inspect phone widths; verify official source links and date. Use a test browser profile to exercise blocked storage and clipboard permission failures. Do not mark student reflections or agenda checks complete on their behalf.
