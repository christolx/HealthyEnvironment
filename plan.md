# LingkunganSehat — Development Execution Plan

## Phase 1 — Stabilize Current App

* Define target platforms, backend runtime, and deployment environment.
* Fix analyzer warnings and replace the broken template test.
* Fix location denial, disabled service, network failure, and empty-data flows.
* Replace the endless refresh loop with cancellable, non-overlapping refresh.
* Preserve manually selected location during refresh.
* Separate location and local time; remove layout/data formatting hacks.
* Remove debug/dead code and add tests for existing AQI and risk logic.

## Phase 2 — Secure API Boundary

* Add a small backend/proxy for WeatherAPI; keep the API key server-side.
* Define typed request/response contracts for current and forecast data.
* Validate location input; add timeout, normalized errors, rate limiting, and basic caching.
* Make the Flutter app use only the internal API.
* Verify no credential or sensitive API response is logged or shipped to clients.

## Phase 3 — Forecast Data Foundation

* Add typed models for current conditions and hourly forecast.
* Include time, temperature, humidity, UV, AQI, condition, and rain probability.
* Parse timestamps using location timezone; exclude past hours.
* Confirm forecast AQI availability for the selected WeatherAPI plan.
* Add loading, retry, empty, stale-data, and partial-data states.
* Test parsing, timezone handling, and API failures.

## Phase 4 — Risk & Recommendation Logic

* Document and validate risk thresholds, weights, and AQI standard.
* Extract risk calculation into pure reusable logic for current and hourly data.
* Build lower-risk window selection with defined duration, tie, and no-result behavior.
* Simplify recommendations; remove duplicates and make actions explicit.
* Test boundaries, missing data, ties, and lower-risk window selection.

## Phase 5 — UI/UX & Theme

* Improve mobile hierarchy for location/time, current risk, metrics, recommendations, and forecast.
* Add horizontal hourly forecast and lower-risk time presentation.
* Add accessible loading, error, retry, and stale-data indicators.
* Implement app-wide light/dark themes; remove hardcoded incompatible colors.
* Persist theme preference locally.
* Test small screens, text scaling, contrast, and key interactions.

## Phase 6 — Release & Evaluation

* Run analyzer, unit/widget tests, and production builds in CI.
* Verify permissions, API-key isolation, backend limits, and release config per target platform.
* Deploy backend and selected Flutter targets; run production smoke tests.
* Prepare short usage guidance for forecast, risk windows, and theme controls.
* Conduct socialization and a short post-survey; record findings for the next iteration.

## Done Criteria

* Analyzer and tests pass; supported production builds succeed.
* Location, refresh, manual search, offline, and denied-permission flows remain usable.
* Forecast and lower-risk recommendations handle timezone and missing data correctly.
* WeatherAPI key exists only server-side.

## Notes
* After each phase, accurately scope changes and stage them as conventional commits.
* App is currently running and accessible @ localhost:38801
