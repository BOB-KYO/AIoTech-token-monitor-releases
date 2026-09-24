# Token Monitor AIoTech

**English** · [한국어](README.ko.md)

A Mac menu-bar app for checking AI-tool usage, estimated costs, and provider limits, based on [Javis603/token-monitor](https://github.com/Javis603/token-monitor).

**Status: local development and validation. No public installer is available yet.** This repository contains release information and progress notes—not the development source or an app download.

## The experience

Open a compact usage summary from the menu-bar icon, expand into details or the usage dashboard, and return to the summary. The work includes tool/model comparisons, trends, search and sorting, resizable views, and currency-display choices. Source tests and synthetic UI checks do not guarantee every provider connection or every installed-app flow.

## What is ready—and what is not

| Area | Current evidence |
| --- | --- |
| Local Mac app | Earlier maintenance was packaged, backed up and applied locally. Summary/detail navigation and changing values were user-confirmed. This is not a public release. |
| Later calculation candidate | Source validation completed: 147 related tests and 13 equivalence replay cases passed. This later candidate is not installed. |
| Collector baseline | 18 isolated queries over 100 synthetic sessions / 9,000 messages checked period totals and deletion behavior. This is not an optimized before/after comparison. |
| CPU and power | High CPU remains unresolved. Synthetic results vary by workload; installed-app CPU and Energy Impact reductions are not established. |
| Installation | Public DMG downloads and Homebrew installation are not available. Signing, notarization and clean-machine installation remain release gates. |

Engineering evidence above is from September 23, 2026 and earlier. This September 24 documentation update does not represent a new app build or new performance measurements.

## Reading the numbers correctly

- Provider limits and locally observed token usage are different metrics.
- Agent/tool and model views can describe the same observations. Do not add these views together as independent usage.
- Verify provider/agent attribution and deduplication before presenting their records as a combined total.
- Missing, stale, partial and unavailable data are not zero usage. A minimum remaining percentage needs its provider and time window.
- Estimated costs are not invoices. Check the currency, exchange-rate basis, period and coverage.
- Preserve collection and limit-alert timing while optimizing calculation work. Lower synthetic CPU time alone is not proof of lower app power usage.

## Project direction

The intended structure separates the personal Mac app, an independent small-team server, and optional AIoTech-specific integrations. The privacy requirement is to keep prompts, responses, credentials and original paths on personal devices. This describes the design boundary, not completed validation of every team-server or integration feature. Monitoring and aggregation are designed without LLM calls.

## Downloads and source

There is no supported public installation command yet. The planned distribution paths are a signed/notarized Mac app download and a Homebrew Cask installing the same verified app. Do not treat a GitHub source archive as an installer.

Development-source backups are kept separate from this public repository. Private repository access does not make code embedded in a future Electron app impossible to extract. Upstream notices are preserved; final product distribution terms are still being reviewed.

## Detailed records

The detailed records below are currently in Korean; this page and the linked Korean overview carry the same project status.

- [Installation readiness — 한국어](INSTALL.md)
- [Verification scope and limitations — 한국어](VERIFICATION.md)
- [Change history — 한국어](CHANGELOG.md)
- [Third-party notices — 한국어](THIRD_PARTY_NOTICES.md)
- [Upstream MIT license](LICENSES/token-monitor-MIT.txt)

Next engineering priorities: equivalent period/attribution/cost results, comparable multi-workload performance tests, and approved packaged-app UI/CPU/power verification before public distribution. Public product naming and final platform support remain subject to release review.
