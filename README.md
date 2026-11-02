# Binomial Lattice Studio

Peter Ritchken · Executive MBA · version 02

A new standalone studio following the structure of the instructor's Excel workbook. The previous Streamlit studio, original spreadsheet, lecture notes, and homework are preserved.

## Pages

- Start here: orientation, conventions, and free navigation.
- One period: calls on the left, puts on the right; pricing weights and European parity; dividend-adjusted H and B; stock, debt, and net-value lattices.
- Two periods: the same progression with European/American selection and visible rebalancing.
- Three periods: European and American call/put lattices under the same inputs, exercise highlighting, node-level calculations, and a complete worked table.
- Eight periods: one selected call/put and exercise style; 45 nodes; early/final exercise labels; nine-outcome terminal risk-neutral histogram.
- Convergence: European calls on the G tree and American calls on the S tree, a dividend-adjusted European Black–Scholes reference, and a refinement table through as many as 1024 periods.
- Theory practice: 20 tagged questions with hints, retry, answer explanations, and explanations of distractors.

Worked examples use S trees so the stock values, dividend-adjusted hedge, and parity can be inspected together. The convergence page uses the agreed G-tree construction for European claims and S-tree construction for American claims. Both are correct continuous-yield European pricing constructions; their coarse finite-step values need not be identical.

## Use locally

No installation or package download is required. With Node.js installed, run:

```text
node serve.mjs
```

Open `http://127.0.0.1:8766`. Serve the `dist` folder with any static web server or host. ES modules require HTTP; do not double-click index.html using a file URL. Static hosting has no Python, Excel, VBA, database, or external CDN dependency.

The live Site is owner-private by default. Sharing is not changed by this build.

## Files and checks

- `dist/model.js`: numerical engines and restricted symbolic calculator.
- `dist/questions.js`: public practice content, independent of the interface.
- `dist/app.js` and `dist/style.css`: interactions and presentation.
- `tests/model.test.mjs`: independent mathematical and parser checks.
- `tests/browser.cjs`: desktop/mobile browser workflow tests using the bundled Playwright runtime.
- `public_manifest.json`: complete list of files approved for serving to learners.
- `MODEL_NOTES.md`: mathematical conventions and source review.
- `VALIDATION.md`: checks and material limits.

Run `node --test tests/model.test.mjs`. Browser tests need the local server and the Codex bundled Playwright package. QA screenshots/reports are ignored by Git and are not site assets.

No assessed homework solutions or instructor files are included. Inputs and ungraded practice progress remain in local browser storage. No student identities, scores, or submissions are transmitted. Reset controls clear the relevant local work.
