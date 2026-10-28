# Stride

A dark, mobile-friendly running companion for choosing your next goal and training towards it.

[Open Stride on GitHub Pages](https://becseai7.github.io/stride/)

[Original Sites deployment](https://stride-pace-planner.genialsnail2053.chatgpt.site)

## Features

- Race history for 5K, 10K, and half marathon results, with dates and race context.
- An editable faster goal, current-fitness reference, and cautious history-based scenarios.
- Weekly training templates, strength exercises, recovery and fuelling guidance.
- Optional age and gender benchmark comparisons with linked sources.
- A simple live run screen with phone GPS, kilometre pace sounds, pause/resume, and a location-free demo.
- Daily energy and time-since-last-run check-ins, with editable pace, time, and distance.
- Optional browser-local history saving.

## Run locally

No build step, dependencies, or API keys are needed. Serve the `dist` directory with a static web server, for example:

```sh
python3 -m http.server 5173 --directory dist
```

Open http://localhost:5173. HTTPS or localhost is required for browser geolocation. Fonts load from Google Fonts, with local fallbacks.

## Source map

| File | Purpose |
| --- | --- |
| `dist/index.html` | App markup and input forms |
| `dist/style.css` | Base layout and responsive styles |
| `dist/dark.css` | Dark athletic visual design |
| `dist/app.js` | Race history, planning UI, benchmarks and local saving |
| `dist/model.js` | History trends and training templates |
| `dist/benchmarks.js` | Sourced age/category comparison standards |
| `dist/run.js` | Live run UI, audio, geolocation and wake lock |
| `dist/run-model.js` | Distance, kilometre splits and pace calculations |
| `.openai/hosting.json` | Existing Sites deployment configuration |

## Deployment

GitHub Pages publishes `dist/` using `.github/workflows/pages.yml`. Changes to `dist/` or the Pages workflow on `main` deploy automatically; the workflow can also be run manually from Actions. The public site is https://becseai7.github.io/stride/.

The original Sites deployment is separate and does not update from GitHub pushes. The included Sites project ID identifies that deployment and is not a credential.

## Practical limits

Training targets and timelines are transparent planning heuristics, not validated individual performance predictions. A goal is an ambition, not a guaranteed outcome. Comparison standards describe a running-community sample, not the general population; source links and interpolation details are in the app.

Live GPS and sound need a compatible browser, location permission, and the page kept active. Locked-screen or background tracking is not reliable. GPS quality varies; interrupted splits are marked rather than given a pace alert. This is a phone web app, not a native Garmin Connect IQ app. Outdoor GPS and device-specific behaviour still need field testing.

History is only stored on the device when the user chooses to save it. GPS coordinates remain in memory and are not uploaded or persisted.

## Verification to date

- Browser checks of the planning flow, editable targets, local history restore, dark mobile layout and running demo.
- Model checks for plateaus, declining or insufficient histories, recovery settings and weekly schedules.
- Checks of benchmark interpolation and supported ages/categories.
- Simulated GPS tests for kilometre crossings, split timing, pace classification, weak fixes, jumps and signal gaps.

No third-party logos or brand assets are included. External references and benchmark sources are linked from the app.
