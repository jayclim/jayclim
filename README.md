# Jayden Lim

CS @ Cornell (B.S. Computer Science, minor in ECE, graduating May 2028). I build systems
that turn messy real-world signals into something you can act on: computer vision,
retrieval, and agent infrastructure, plus the dashboards that make the output legible.

Software Engineer Intern at **Cisco (Duo Security)** this past summer, working on incident
response and internal SRE tooling. Currently building a plant-telemetry control dashboard
at **NSF CROPPS** and writing mission logic for Cornell's **CUAUV** autonomous submarine
team.

**[jaydenclim.com](https://jaydenclim.com)** · **[LinkedIn](https://linkedin.com/in/jaydenclim)** · jcl399@cornell.edu · Ithaca, NY (from the Bay Area)

---

## Selected work

### [COURTSIDE](https://github.com/jayclim/BadmintonAI) · badminton match intelligence from broadcast video

Solo-built CV system that watches a badminton broadcast and writes the scouting report. It
tracks both players and the shuttle, detects every hit, reads the scoreboard, segments
rallies, and turns all of it into a coach-grade analytics dashboard with AI-annotated video
for every rally. No human labels at inference time.

Thresholds were tuned on one match and tested untouched on a second, so the held-out
numbers are true out-of-distribution: hit detection **F1 87.9**, rally segmentation **F1
97.6**, players located to **0.57 m** on court, score OCR **95.2%**. End to end it
reproduces 84.5% of professionally annotated strokes. Every stage publishes its own
accuracy against ShuttleSet22 ground truth, including the gap between tuned and held out.

Two-tier DuckDB store (per-frame tracks underneath, one row per shot on top) so detection
logic can change without ever reprocessing video.

`Python` `PyTorch` `YOLO11-Pose` `TrackNetV3` `OpenCV` `DuckDB` `Next.js` `TypeScript`

**[Live dashboard](https://badminton.jaydenclim.com/)**

### [PitchLoop](https://github.com/jayclim/pitchloop) · consent-gated outbound sales agent

***Runner-up, Best Use of Zero.xyz · Loop Engineering Hackathon (SF, July 2026) · 65 submissions, 195 participants***

Researches a prospect queue, learns across conversations through evidence-backed
reflections, and acquires or authors the tools it finds missing. Every paid action passes a
real Pomerium allow/deny policy gate under a hard spend ceiling.

I led a team of four and owned the agent core: the plan → policy → enrich → call → diagnose
→ reflect → retry state machine, and the integration across all four vendor layers. We
froze a typed interface contract and a file-ownership map before anyone wrote code, which
is the reason four people shipped one coherent system overnight.

`Python` `FastAPI` `Zero.xyz` `Pomerium` `Nexla`

**[Devpost](https://devpost.com/software/pitchloop)**

### [InvestBot](https://github.com/jayclim/InvestBot) · rule strategies vs LLM agents, scored head to head

Three rule-based strategies against LLM agent swarms over one shared ~100-name universe,
scored on identical fills. Per-fill slippage, 15% stop-loss, position caps, a $60 equity
circuit breaker, benchmarked against SPY. The Dec–Jun walk-forward backtest is kept
strictly separate from the forward-only book, so nothing in the results is fit on data the
agents already saw.

The interesting design question was how to make a rule engine and an LLM swarm comparable
at all. They run on the same universe, the same bars and the same fill model, so the only
variable is how each one decides.

`Python` `Next.js` `Claude API` `MCP`

**[Live dashboard](https://invest-bot-gray.vercel.app/)**

---

## Also

**[Clash Royale Analytics](https://github.com/jayclim/CR-Data)** · scheduled ETL that has
auto-committed **1,300+** times and redeployed itself since launch, unattended.
[Live](https://clash.jaydenclim.com/)

**[DoomGuard](https://github.com/jayclim/DoomGuard)** · Android focus app with a custom
Kotlin native module (UsageStatsManager monitoring, blocking overlay, boot-persistent
foreground service), **78 tests** and GitHub Actions CI.

**[OneCall](https://github.com/jayclim/onecall)** · voice healthcare navigation. A
deterministic red-flag emergency screen runs ahead of any model call, then Moss-grounded
specialty triage over semantic retrieval. FHIR R4, real CMS provider data.

**[FoldEx](https://github.com/jayclim/foldex)** · Finalist (top 5), Cornell Claude Builder
Club Hackathon. Staged async FastAPI + RQ pipeline orchestrating Claude over Ensembl,
ClinVar, gnomAD and AlphaFold. [Live](https://foldex-three.vercel.app/)

---

## Research

Co-author, *Multilabel Classification for Lung Disease Detection*, [arXiv:2412.11452](https://arxiv.org/abs/2412.11452) (2024).
Work done at **Stanford AIMI**: 12,549 chest X-rays, RadGraph-parsed reports, ConvNeXt and
ResNet-50. Data-level downsampling took the model from 0.56 to **0.86 macro-AUROC** and
fixed three classes that had collapsed to 0.00 F1 under the dominant label.

Co-author, *A Novel Hybrid Post-Hartree-Fock and Monte Carlo Algorithm*, [IJCEA / ICCME 2025](https://doi.org/10.18178/ijcea.2025.16.1.41-47). Led an 8-person research team.

---

## Toolbox

**Languages** Python · TypeScript · JavaScript · OCaml · SQL · Java · Swift<br>
**ML & Data** PyTorch · YOLO · OpenCV · pandas · NumPy · scikit-learn · spaCy · DuckDB · PostgreSQL · RAG (AWS Bedrock)<br>
**Web** Next.js · React · React Native · FastAPI · Flask · Django · Tailwind<br>
**Infra** Linux · Docker · AWS · GitHub Actions · CI/CD · Vercel · MCP · OWASP ZAP

---

Cornell Badminton competitive team, 2nd place at Regionals. Which is the actual reason
COURTSIDE exists.
