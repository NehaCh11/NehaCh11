## Neha Chaudhary

AI engineer. Currently splitting time between PhD research on speech as a
signal for cardiac conditions, and building AI agent systems.

### Automations

A running log — one row per automation I've built. Everything here is deployed
and running on a schedule, not written once and shelved. Where it runs is a
link, so you can check the runs yourself.

| # | Automation | What it does | Lives in | Runs on |
| --- | --- | --- | --- | --- |
| 1 | [arxiv-digest](https://github.com/NehaCh11/research-automations/tree/main/arxiv-digest) | Tracks new arXiv papers across seven speech, cardiac and audio-ML topics and commits a dated digest, skipping anything already reported | [research-automations](https://github.com/NehaCh11/research-automations) | [Actions](https://github.com/NehaCh11/research-automations/actions/workflows/arxiv-digest.yml), daily 07:00 UTC |

### How I build these

Five rules, learned mostly by breaking them:

- **It has to run.** Every automation is executed against the real service
  before it lands, and its real output is committed. No untested code.
- **Standard library first.** A dependency is added only when the task cannot be
  done without it.
- **Idempotent.** Running twice does not duplicate work or double-post.
- **State is visible.** Anything a job remembers between runs is a file in the
  repo, not a hidden cache — reviewable, and a bad run is fixable with an edit.
- **Degrade, don't crash.** A scheduled job that loses one query should still
  deliver the rest and say what it missed.

### Research

PhD work on whether speech carries a usable signal for detecting cardiac
conditions — acoustic feature analysis, sequence models over voice recordings,
and the evaluation traps that make results in this area look better than they
are. Methods and negative results both; the latter are usually more useful.

### Also working on

AI agent systems — multi-agent orchestration, retrieval pipelines, and
domain-specific analysers. Most of it is in the repo list.
