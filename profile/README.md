# Eigan

**Inside the box thinking.**

Language models are not black boxes. We read what's inside them, in your infrastructure, in
real time.

Internal activations carry legible, structured representations of human-meaningful concepts —
deception, threat, data exfiltration, authorization. Eigan reads them, alerts on them, and
steers them in real time, so that security and regulated teams can deploy AI they can actually
supervise.

Mechanistic interpretability requires direct access to the model, which means the model has to
be hosted rather than called through someone else's API. For most products that is a
constraint. For us it is the point: the teams who most need to supervise a model are the same
teams who already require it to run inside their own boundary.

---

## Research

Our methods are published, and the reference implementation and datasets are open.

**The Concept Allocation Zone: Tracking How Concepts Form Across Transformer Depth**
[arXiv:2605.24856](https://arxiv.org/abs/2605.24856)

Concept formation in transformers is depth-extended rather than a single-layer event. We
formalize the depth interval within which a concept becomes measurably separable, and derive
boundary detection without manual layer sweeps. Validated across 34 models from 8 architectural
families.

**Geometric Evolution Maps: Extracting Stable Concept Probes from Transformer Residual Streams**
[arXiv:2605.25848](https://arxiv.org/abs/2605.25848)

Concept probe directions rotate substantially during assembly and do not settle until a
characteristic handoff layer. Probes extracted at the handoff are at least as precise as
conventional peak-layer probes in 68.5% of 391 model × concept ablation experiments, across 23
architectures from 70M to 14B parameters (model-level Wilcoxon W=214, N=23, p=0.010,
one-sided).

**rosetta_tools** — reference implementation for both papers, archived at
[doi:10.5281/zenodo.20361433](https://doi.org/10.5281/zenodo.20361433). Released alongside a
public dataset of pre-extracted activations across the full model corpus and the contrastive
concept datasets.

Both papers report the predictions that failed alongside the ones that held. We intend to keep
doing that.

---

## What is open, and what is not

**Open:** methodology, evaluation sets, benchmark harnesses, reference implementations, and
results — including negative results.

**Closed:** Spectre CIA, our inference-time concept monitor — the product, its inference
pipeline, and its tuning.

We would rather state the boundary plainly than leave it to be discovered.

---

## Contact

[eigan.ai](https://eigan.ai) · george@eigan.ai
