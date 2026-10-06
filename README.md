# AI-SRE Engineering

Independent engineering and research into AI-assisted Site Reliability Engineering.

**Read it as a site: <https://krishnakvr.github.io/ai-sre-engineering/>**

## In short

An AI-assisted incident workflow and the SRE platform underneath it, built and run on a single rented
server. When a bad deploy degrades a service:

- An SLO alert starts an investigation. Nobody is involved.
- The investigation collects evidence and asks a small self-hosted language model one question.
- A pull request reverting the responsible commit is open **17 seconds after the alert arrives**.
- Nothing changes in the cluster until someone authorized for the service approves.
- A separate account merges, and recovery is confirmed from telemetry.

| Result | Measured |
|---|---|
| Alert to a fix ready for approval | 17 s |
| Drills where the right commit was named | 5 of 5 |
| Approval by someone not authorized | Refused and logged; nothing changed |
| Hosted AI APIs used | None |

## Where to go

- [Introduction](docs/index.md): the summary, architecture, decisions and limits.
- [From Alert to a Fix Ready for Approval in 17 Seconds](docs/ai-sre/01-alert-to-fix-ready-for-approval.md):
  the first technical piece.
- The technical pieces are under [`docs/`](docs/), in four groups: AI-SRE and AI engineering, SRE and
  reliability, platform and infrastructure, and engineering judgment. More are added as they are
  written.

## Licence

Text and images are licensed under [Creative Commons Attribution 4.0 International](LICENSE).
