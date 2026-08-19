<div align="center">
  <img src="assets/hero.svg" width="100%" alt="Jayden Lim. CS @ Cornell. I build computer vision and agent systems, then the dashboards that make them legible.">
</div>

<p align="center">
  <a href="https://jaydenclim.com"><img src="https://img.shields.io/badge/Portfolio-jaydenclim.com-cdfa50?style=for-the-badge&logo=googlechrome&logoColor=cdfa50&labelColor=0b0d0c" alt="Portfolio"></a>
  <a href="https://linkedin.com/in/jaydenclim"><img src="https://img.shields.io/badge/LinkedIn-jaydenclim-2fd4c4?style=for-the-badge&logo=linkedin&logoColor=2fd4c4&labelColor=0b0d0c" alt="LinkedIn"></a>
  <a href="mailto:jcl399@cornell.edu"><img src="https://img.shields.io/badge/Email-jcl399%40cornell.edu-ff8b5e?style=for-the-badge&logo=gmail&logoColor=ff8b5e&labelColor=0b0d0c" alt="Email"></a>
</p>

<br>

<table>
<tr>
<td width="50%" valign="top">
  <a href="https://github.com/jayclim/BadmintonAI"><img src="assets/card-courtside.svg" width="100%" alt="COURTSIDE: broadcast video in, scouting report out"></a>
  <p align="center"><a href="https://badminton.jaydenclim.com/"><b>↗ Live dashboard</b></a> &nbsp;·&nbsp; <a href="https://github.com/jayclim/BadmintonAI">Code</a></p>
</td>
<td width="50%" valign="top">
  <a href="https://github.com/jayclim/pitchloop"><img src="assets/card-pitchloop.svg" width="100%" alt="PitchLoop: outbound sales agent, hackathon runner-up"></a>
  <p align="center"><a href="https://devpost.com/software/pitchloop"><b>↗ Devpost</b></a> &nbsp;·&nbsp; <a href="https://github.com/jayclim/pitchloop">Code</a></p>
</td>
</tr>
<tr>
<td width="50%" valign="top">
  <a href="https://github.com/jayclim/InvestBot"><img src="assets/card-investbot.svg" width="100%" alt="InvestBot: rule strategies against LLM swarms"></a>
  <p align="center"><a href="https://invest-bot-gray.vercel.app/"><b>↗ Live dashboard</b></a> &nbsp;·&nbsp; <a href="https://github.com/jayclim/InvestBot">Code</a></p>
</td>
<td width="50%" valign="top">
  <a href="https://github.com/jayclim/DoomGuard"><img src="assets/card-doomguard.svg" width="100%" alt="DoomGuard: Android focus app with a custom Kotlin native module"></a>
  <p align="center"><a href="https://github.com/jayclim/DoomGuard"><b>↗ Code</b></a> &nbsp;·&nbsp; <a href="https://github.com/jayclim/DoomGuard#readme">Readme</a></p>
</td>
</tr>
</table>

<br>

<div align="center">
  <a href="https://badminton.jaydenclim.com/"><img src="assets/courtside-annotated.gif" width="100%" alt="COURTSIDE: a live rally with pose skeletons, shuttle trail, shot classification and machine-read score drawn on the broadcast, next to a 2D replay animated from the tracks"></a>
  <p><i><b>COURTSIDE, mid-rally.</b> Pose skeletons, the shuttle trail, the shot call with its confidence,<br>the score read straight off the scoreboard, and a 2D replay animated from the tracks.<br>Nothing here was labelled by hand.</i></p>
</div>

<details>
<summary><b>&nbsp;How COURTSIDE scores against human annotators</b></summary>

<br>

Thresholds were tuned on one match and tested untouched on a second, so the held-out column is true
out-of-distribution performance. Ground truth is ShuttleSet22.

| Stage | Tuned | Held out |
|---|---|---|
| Hit detection | **F1 87.9** | F1 85.8 |
| Rally segmentation | **F1 97.6** | F1 94.0 |
| Player → court metres | **0.57 m** median | 0.64 m |
| Landing position | **0.55 m** median | 1.12 m |
| Score OCR | **95.2%** | 97.3% |

End to end the label-free chain reproduces **84.5% / 79.5%** of annotated strokes. Player detection
and shot classification come from pretrained third-party models; hit detection, landings, rally
segmentation, score OCR and the analytics are mine. Full breakdown in the
[repo](https://github.com/jayclim/BadmintonAI#readme).

<br>

<a href="https://badminton.jaydenclim.com/"><img src="assets/courtside-lab.jpg" width="100%" alt="COURTSIDE AI Lab: live score-OCR crops, the AI-vs-labels confusion matrix, and per-class recall"></a>

<sub>The AI Lab page publishes the gap between the pipeline and the human labels, per stage, rather than only the wins.</sub>

</details>

<details>
<summary><b>&nbsp;More things I've built</b></summary>

<br>

| | |
|---|---|
| **[Clash Royale Analytics](https://github.com/jayclim/CR-Data)** | Scheduled ETL that has auto-committed **1,300+** times and redeployed itself since launch, unattended. [Live ↗](https://clash.jaydenclim.com/) |
| **[OneCall](https://github.com/jayclim/onecall)** | Voice healthcare navigation. A deterministic red-flag screen runs ahead of any model call, then specialty triage over semantic retrieval. FHIR R4, real CMS provider data. |
| **[FoldEx](https://github.com/jayclim/foldex)** | Finalist (top 5), Cornell Claude Builder Club Hackathon. Async FastAPI + RQ pipeline orchestrating Claude over Ensembl, ClinVar, gnomAD and AlphaFold. [Live ↗](https://foldex-three.vercel.app/) |
| **[Veto](https://github.com/jayclim/Veto)** | MCP budget-guardrail server. Agents with receipts. |

</details>

<details>
<summary><b>&nbsp;Where I've worked</b></summary>

<br>

**Cisco** · Software Engineer Intern, Duo Security · Summer 2026<br>
Migrated Duo onto Cisco's internal multi-tenant incident platform as its third tenant org, designed
and owned the end-to-end incident-response pipeline replacing the outgoing third-party tool, and
built the retrieval layer of an internal SRE assistant on AWS Bedrock.

**NSF CROPPS** · Software Engineer · Mar 2026 – present<br>
React/Flask control dashboard for 57 networked research plants, 6 IoT device systems, live camera
feed at 15 FPS over Flask.

**CUAUV** · Software Engineer · Oct 2025 – present<br>
Bin-search mission logic in Python/asyncio on the team's RoboSub vehicle. 7-channel RGB + surface-normal
+ depth YOLO detector across 10 classes, ~20% detection improvement over RGB-only.

**Stanford AIMI** · Research Intern · Jun 2024<br>
12,549 chest X-rays, RadGraph-parsed reports. Data-level downsampling took the model from 0.56 to
**0.86 macro-AUROC** and fixed three classes that had collapsed to 0.00 F1.

</details>

<details>
<summary><b>&nbsp;Research</b></summary>

<br>

- **Multilabel Classification for Lung Disease Detection** · [arXiv:2412.11452](https://arxiv.org/abs/2412.11452) (2024)
- **A Novel Hybrid Post-Hartree-Fock and Monte Carlo Algorithm** · [IJCEA / ICCME 2025](https://doi.org/10.18178/ijcea.2025.16.1.41-47). Led an 8-person research team.

</details>

<details>
<summary><b>&nbsp;Toolbox</b></summary>

<br>

<img src="assets/stack.svg" width="100%" alt="Toolbox: languages, ML and data, web, infrastructure">

</details>

<br>

<div align="center">
  <sub>Fun fact! I love badminton and I am on the Cornell Badminton team!</sub>
</div>
