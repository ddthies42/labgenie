# LabGenie — Health Results Dashboard (Prototype)

An interactive prototype of the LabGenie patient-facing lab results experience:
a login screen, a results dashboard, recent and past results views, and the
LabGenie chat assistant.

## View it

**Live:** open `index.html` in any browser — no install, no build step. It is a
single self-contained file and works offline.

If this repo has GitHub Pages enabled (Settings → Pages → deploy from `main`,
root), the prototype is served at the Pages URL directly.

## The flow

1. **Login** — enter anything in the email and password fields and press
   **Log in**. There is no real authentication; the button advances the flow.
2. **Dashboard** — summary of recent lab results, flagged values, and next steps.
3. **Recent / Past results** — detail views, including result ranges over time.
4. **LabGenie chat** — the assistant panel, reachable from the results views.
   Responses are scripted, not live.

## What's in here

| Path | What it is |
| --- | --- |
| `index.html` | The built, self-contained prototype. **Open this one.** |
| `Health Results Dashboard.dc.html` | Source for the main design — login + all dashboard screens. |
| `LabGenieChat.dc.html` | Source for the chat assistant panel. |
| `RangeBar.dc.html` | Source for the result-range indicator component. |
| `support.js` | Runtime the source files load. |
| `logo-icon.png` | LabGenie mark. |
| `uploads/` | Reference React/TypeScript codebase the prototype was modelled on. Not used to build or run the prototype. |
| `.gitignore` | Excludes build output — notably `.bundles/`, a bundler cache directory that should never be committed. |

`index.html` is compiled output. To change the design, edit the `.dc.html`
source files and rebuild — don't hand-edit `index.html`.

## Caveats

- Prototype only: no backend, no real auth, no persistence. Nothing entered is
  stored or sent anywhere.
- All patient data shown is fabricated sample content.
- Designed for desktop widths (roughly 980px and up).
