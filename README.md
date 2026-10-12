# Token Monitor AIoTech

**English** · [한국어](README.ko.md)

A Mac menu-bar app for checking AI-tool usage, estimated costs, and provider limits, based on [Javis603/token-monitor](https://github.com/Javis603/token-monitor).

**Status: local development and validation. No public installer is available yet.** This repository contains release information and progress notes—not the development source or an app download.

## The experience

Open a compact usage summary from the menu-bar icon, expand into details or the usage dashboard, and return to the summary. The work includes tool/model comparisons, trends, search and sorting, resizable views, and currency-display choices. Source tests and synthetic UI checks do not guarantee every provider connection or every installed-app flow.

## What is ready—and what is not

| Area | Evidence as of October 12, 2026 |
| --- | --- |
| Local Mac candidate | The collection race fix passed regression checks and was installed locally with the previous app preserved. Reopening produced a new successful collection. The last observation did not prove the collecting indicator returned to idle. |
| Code checks | Node 24.21.0: 4,483 passed, 0 failed, 1 skipped. Electron 43.4.0 collector/native-watcher checks: 17 passed. These are local candidate results, not this documentation repository's CI or public-release acceptance. |
| Collection lifecycle | 12 isolated synthetic lifecycle checks passed. Hidden batching, repeated manual refresh, failure recovery and injected resume events were exercised; real OS sleep/lock and live provider/sync/alert checks remain unverified. |
| CPU and power | One 10-minute observation per app showed core four-process average CPU of 55.84% → 3.45% (100% = one core). Transient children were excluded and workloads differed. This is not a measured whole-app energy reduction. |
| Installation | No public DMG or Homebrew installation is available. Signing, notarization, clean-machine installation and release acceptance remain open. |

**Latest recorded verdict: PASS_WITH_LIMITS.** The corrected candidate was retained after the local check at 06:57 UTC on October 12. The results do not establish its current live state. [Detailed verification](VERIFICATION.md) retains the earlier dated results, the tested candidate identifier and the remaining acceptance criteria. This documentation update does not publish a new app build.

## Reading the numbers correctly

- Provider limits and locally observed token usage are different metrics.
- Agent/tool and model views can describe the same observations. Do not add these views together as independent usage.
- Verify provider/agent attribution and deduplication before presenting their records as a combined total.
- Missing, stale, partial and unavailable data are not zero usage. A minimum remaining percentage needs its provider and time window.
- Estimated costs are not invoices. Check the currency, exchange-rate basis, period and coverage.
- The local candidate batches background usage collection under a separate automatic power-saving policy. Active collection, provider-limit/backoff and alert behavior, and sync freshness are intended to be preserved; live provider/sync/alert verification is still pending. Lower CPU observations alone are not proof of lower app power usage.

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

Next engineering priorities: confirm the post-reopen idle state, run controlled 10-minute comparisons three times per condition, measure whole-app CPU/wakeups/latency and available energy indicators, and verify real OS transitions and provider/sync/alert behavior before public distribution. Public product naming and final platform support remain subject to release review.
