# Ariel Stone Beti

> **En bref (français).** Étudiant de 19 ans à l'Université d'Ottawa, né au Cameroun, résident
> permanent du Canada. Je construis des systèmes dont on peut vérifier chaque affirmation, et je
> cherche un stage ou une occasion de recherche en génie logiciel, en systèmes d'IA ou en génie
> biomédical.

I'm Stone, a 19-year-old student at the University of Ottawa. I entered university through the
Interdisciplinary Arts program, and I am working on a transfer to the dual degree in Biomedical
Mechanical Engineering and Computing Technology. Before that, I spent a year in Computer Systems
Technology at Collège Boréal in Toronto. I was born in Cameroon and I'm a permanent resident of
Canada.

I like building things whose claims can be checked: exact results where exactness is possible,
pass/fail thresholds written down before the experiment, and a plain account of what did not work.

**Looking for:** an internship or a research opportunity in software engineering, AI systems or
biomedical engineering.

## Research: troncons

**Serving gpt-oss-120b, a 63.4 GB model, on a laptop with 16 GB of RAM and an 8 GB RTX 4060.**
The weights stay compressed on disk and are decoded only when a computation needs them; the host
working set peaks at 384 MB, and the GPU footprint is set by the card, not by the model.

- **A synonymous codon for zero.** MXFP4 has two codes for zero (+0 and −0), and no computation of
  the engines considered depends on the sign. I proved that folding −0 into +0 before entropy
  coding saves exactly P(V = 0) · H(S | V = 0) bit per weight, and checked it on all 180 expert
  tensors of gpt-oss-20b and gpt-oss-120b to within 1.7 × 10⁻⁴ bit.
- **Lossless.** In version 1.2 of the engine's file format, the fold removes 1.80 GB from
  gpt-oss-120b (3.26 % of its expert-weight bits); the engine's logits stay identical to the bit
  over 5,120 steps on both models.
- **Measured honestly.** On this laptop, v1.2 generates 2.890 tokens/s against 1.988 for v1.0
  (×1.454; an independent judge measured ×1.442). The smaller file alone would allow at most
  +3.4 %; a crossed experiment traces the rest of the gain to the pattern of disk read requests
  on this machine, and the write-up says it is not a portable result.
- Written up in three technical volumes, in English and French. A short paper is in preparation;
  the code is not public yet.

**How I work:** I directed this project with Claude Code. I set the goals, declared the success
criteria before any measurement, and had every key result redone by independent reviewer agents
before I believed it; the agents wrote most of the code and the reports.

## Selected projects

| Project | What it is | Stack |
|---|---|---|
| [recompose](https://github.com/stoneariel491-sudo/recompose) | Turning a scanned math book into typeset source that provably says the same thing: verification instruments tested by planting known defects, hypotheses written before results. | Python, NumPy |
| [moderation-pipeline-prototype](https://github.com/stoneariel491-sudo/moderation-pipeline-prototype) | Research prototype: where can an attacker exploit the seams between moderation stages (selective classification, Dung argumentation, bridging), and can they be defended? Each defense is measured against a naive baseline. | Python, pytest |
| [vigie](https://github.com/stoneariel491-sudo/vigie) | A native Windows app for watching coding agents think, live: their reasoning, messages, tool calls and images. Built with the agents it watches. | Rust, wgpu, WGSL |
| [veilleuse](https://github.com/stoneariel491-sudo/veilleuse) | A full-screen flip clock and floating study timer, with a hand-made glass effect that Windows does not provide, written up as a short paper. | Rust, wgpu, WGSL |

Also: [discoveries](https://github.com/stoneariel491-sudo/discoveries), the admission-control
technique from the moderation prototype written up as a paper, a practitioner guide and an
explainer, in English and French.

## Beyond code

- Represented Ontario at the **11th Parlement francophone des jeunes** in Yaoundé, Cameroon
  (July 2026).
- Member of the **Youth Climate Ambassador** program with Skills for Change in Toronto.

**Languages:** French, English.
**Tools I use most:** Python, Rust, TypeScript, CUDA, LaTeX, Git.
