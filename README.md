
</div>

---

### 🧬 About Me & Research Focus

I operate at the convergence of **First-Principles LLM Systems Engineering** and **Computational Oncology / Protein Language Models**.

My work focuses on eliminating "black-box wrapper dependencies": building, deriving, and mathematically verifying modern deep architectures directly from **tensor calculus and silicon hardware physics** up to **mechanistic post-training alignment**, and grounding attention mechanics in **clinical drug resistance and cancer genomics**.

- ⚡ **LLM Silicon Systems Engineering**: Building the complete modern Transformer backbone from scratch in pure PyTorch ([`llm-engineering-lab`](https://github.com/elham715/llm-engineering-lab)) — from RoPE 2D complex rotation planes, scale-invariant RMSNorm, and GQA stride broadcasting to LoRA associative matrix memory, DPO closed-form Bradley-Terry loss, and Leviathan speculative decoding.
- 🔬 **Protein Language Models & Oncology**: Pioneering mechanistic attention disruption in oncogenic kinases ([`oncogenic-attention-disruption`](https://github.com/elham715/oncogenic-attention-disruption)) — proving that Meta's ESM-2 self-attention maps autonomously quantify covalent drug resistance (EGFR C797S / Osimertinib) and align with experimental crystal structures (PDB `2J6M`, $r_s = 0.4464$) without 3D training labels.
- 📐 **Rigorous Engineering Standard**: Zero external black-box frameworks for core algorithms, verified mathematical invariants (analytical gradchecks $\le 10^{-10}$, step-0 LoRA identity, RMSNorm scale invariance), and 30+ passing unit tests.

---

### 🏆 Featured Research & Engineering Laboratories

#### 1. 🧬 Mechanistic Attention Disruption in Oncogenic Kinases
*Repository: [**`oncogenic-attention-disruption`**](https://github.com/elham715/oncogenic-attention-disruption)* • [![Tests](https://img.shields.io/badge/Tests-9%2F9%20Passing-brightgreen.svg)](https://github.com/elham715/oncogenic-attention-disruption) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **Unsupervised quantification of clinical cancer drug resistance in human EGFR kinase via Meta's ESM-2 Transformer Self-Attention:**

$$\mathbf{A}_{ij} = \text{Softmax}\left(\frac{\mathbf{q}_i \mathbf{k}_j^T}{\sqrt{d_k}}\right), \quad \Delta \mathbf{A} = |\mathbf{A}_{\text{mutant}} - \mathbf{A}_{\text{wildtype}}|$$

* **Zero-Coordinate Resistance Discovery**: ESM-2 autonomously pinpoints the fatal Osimertinib resistance mutation **C797S** as the **#2 top disrupted residue** ($\text{ADI} = 9.3 \times 10^{-5}$) and the **Met793 hinge donor** as **#3**, capturing covalent bond loss and allosteric active-site transmission without 3D training coordinates.
* **Crystallographic PDB Alignment**: Evaluated against the human EGFR crystal structure (**PDB `2J6M`**), achieving a **0.4464 Spearman rank correlation** between internal ESM-2 attention weights and ground-truth spatial proximity ($1/D_{ij}$ in $\text{\AA}$) across 306 $C_\alpha$ atoms.
* **Production Package**: Full CLI runner (`run_analysis.py`), interactive 1-click tutorial notebook, and 9 verified unit tests.

---

#### 2. ⚡ LLM Engineering Lab (Silicon Physics to Post-Training)
*Repository: [**`llm-engineering-lab`**](https://github.com/elham715/llm-engineering-lab)* • [![Tests](https://img.shields.io/badge/Tests-21%2F21%20Passing-brightgreen.svg)](https://github.com/elham715/llm-engineering-lab) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **A zero-black-box systems repository implementing 7 modern LLM engines from scratch in pure PyTorch:**

| # | Engine | Mathematical & Systems Core | Status | Verification |
|---|---|---|:---:|:---:|
| **01** | [`01_gpt2_from_scratch/`](https://github.com/elham715/llm-engineering-lab/tree/main/01_gpt2_from_scratch) | **Full GPT-2 (124M)**: Causal MHA, `Conv1D` weight transfer from OpenAI checkpoints, weight tying, and Top-K/Top-p sampling. | **Verified** 🟢 | [test_model.py](https://github.com/elham715/llm-engineering-lab/blob/main/01_gpt2_from_scratch/test_model.py) |
| **02** | [`02_chronosteer_studio/`](https://github.com/elham715/llm-engineering-lab/tree/main/02_chronosteer_studio) | **ChronoSteer Studio**: Real-time interpretability UI (`bfloat16` CPU + WebSockets). Dynamic KV time-travel rewind, Layer-6 contrastive steering, and 360° future-word wheel. | **Verified** 🟢 | Live Web GUI |
| **03** | [`03_bpe_tokenizer/`](https://github.com/elham715/llm-engineering-lab/tree/main/03_bpe_tokenizer) | **Byte-Level BPE**: 256-byte UTF-8 base vocab, iterative pair frequency counting, regex pre-tokenization, zero `<unk>` guarantee, verified round-trip on Bengali and biochemical sequences. | **Verified** 🟢 | [test_bpe.py](https://github.com/elham715/llm-engineering-lab/blob/main/03_bpe_tokenizer/test_bpe.py) |
| **04** | [`04_modern_architecture_gqa_rope/`](https://github.com/elham715/llm-engineering-lab/tree/main/04_modern_architecture_gqa_rope) | **LLaMA-3 / Mistral Backbone**: Rotary Position Embeddings (RoPE 2D complex rotation), scale-invariant RMSNorm ($c \cdot x \equiv x$), SwiGLU gating ($\lfloor \frac{8}{3}d \rfloor$), and GQA zero-copy broadcasting. | **Verified** 🟢 | 6/6 Passing |
| **05** | [`05_lora_peft_from_scratch/`](https://github.com/elham715/llm-engineering-lab/tree/main/05_lora_peft_from_scratch) | **LoRA & QLoRA NF4**: $W_0 + \frac{\alpha}{r} (BA)$ with $B=0$, associative matrix memory trick $(x A^T) B^T$ ($O(r)$ memory), zero-latency weight merging, and 16-quantile NormalFloat4 quantization. | **Verified** 🟢 | 6/6 Passing |
| **06** | [`06_preference_optimization_dpo/`](https://github.com/elham715/llm-engineering-lab/tree/main/06_preference_optimization_dpo) | **Direct Preference Optimization (DPO)**: Closed-form Bradley-Terry preference loss, analytical partition function $Z(x)$ cancellation, autoregressive target shift (`:-1` vs `1:`), and prompt masking (`-100`). | **Verified** 🟢 | 5/5 Passing |
| **07** | [`07_inference_kvcache_speculative_decoding/`](https://github.com/elham715/llm-engineering-lab/tree/main/07_inference_kvcache_speculative_decoding) | **High-Throughput Inference Engine**: Dynamic zero-reallocation static KV cache and Leviathan/Chen Speculative Decoding with rejection sampling for $2\times\text{–}3\times$ speedup preserving exact target distribution. | **Verified** 🟢 | 4/4 Passing |

---

#### 3. 🔬 Seminal Paper Reproductions
*Repository: [**`first-principles-ai-lab`**](https://github.com/elham715/first-principles-ai-lab)*

* **Sequence Foundations (5 Papers)**:
  * **Elman (1990)** *"Finding Structure in Time"*: Pure NumPy SRN, manual BPTT, analytical gradcheck ($\le 6.93 \times 10^{-11}$), and vanishing gradient proof — *Completed & Verified* 🟢
  * **Hochreiter & Schmidhuber (1997)** *"LSTM"*: Constant Error Carousel (CEC) & additive gating — *Completed* 🟢
  * **Bengio et al. (2003)**, **Sutskever et al. (2014)**, **Bahdanau et al. (2014)** — *In Progress* 🟡
* **Modern Transformer Core (6 Papers)**:
  * **Vaswani (2017)** *Attention* + **Radford (2019)** *GPT-2* + **Zhang (2019)** *RMSNorm* + **Shazeer (2020)** *SwiGLU* + **Su (2021)** *RoPE* + **Ainslie (2023)** *GQA* — *Fully Implemented & Verified in `llm-engineering-lab`* 🟢
* **Alignment & High-Throughput Inference**:
  * **Rafailov et al. (2023)** *DPO* + **Hu et al. (2021)** *LoRA* + **Leviathan et al. (2022)** *Speculative Decoding* — *Verified* 🟢

---

#### 4. 🩺 Biomedical Vision & Signal Intelligence
*Repositories: [**`biomedical-cnn-lab`**](https://github.com/elham715/biomedical-cnn-lab) • [**`biomedical-sequence-lab`**](https://github.com/elham715/biomedical-sequence-lab)*

* **COPD Respiratory Acoustic ConvNet**: Converting stethoscope recordings (ICBHI 2017) into 2D Log-Mel Spectrograms with Grad-CAM explainability to classify COPD vs. Healthy.
* **Neuroscience EEG ShallowConvNet (Schirrmeister et al., 2017)**: Decoding motor imagery from raw 64-channel PhysioNet EEG brainwaves and visualizing learned Alpha/Beta cortical frequency filters.
* **PaccMann & Oncolytic Peptides**: Multi-modal SMILES $\times$ transcriptomic drug sensitivity modeling and antimicrobial peptide generation.

---

### 🛠️ Technical Arsenal

<div align="center">

| Domain | Systems, Tools & Mathematical Foundations |
|---|---|
| **Foundation Models & LLM Systems** | Autoregressive Transformers, Causal Attention, RoPE 2D Rotations, GQA, RMSNorm, SwiGLU Gating, LoRA / QLoRA NF4, Static KV-Cache, Speculative Decoding, DPO Alignment |
| **Protein Language Models & Bio-ML** | Meta ESM-2, Multi-Head Attention Extraction, Perturbation Analysis ($\Delta \mathbf{A}$), Structural Alignment, PDB $C_\alpha$ Euclidean Coordinates, Contact Precision @ $L/5$ |
| **Deep Learning & Computer Vision** | Elman RNNs, LSTMs, ResNets, 2D Log-Mel Spectrogram CNNs, ShallowConvNet EEG, Grad-CAM Explainability |
| **Mathematical & Silicon Hygiene** | Analytical Gradients (`gradcheck` $\le 10^{-10}$), BPTT Jacobians, Associative Matrix Contraction, Scale Invariance Invariants, FP32 Numerical Overflow Guards |
| **Languages, Runtimes & Tooling** | Python, PyTorch, NumPy, SciPy, BioPython, Starlette, WebSockets, Git, Linux, LaTeX |

</div>

---

<div align="center">

<!-- GitHub Streak Card -->
<img src="https://github-readme-streak-stats.herokuapp.com/?user=elham715&theme=tokyonight&hide_border=true" width="49%" />

<!-- Top Languages Card -->
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=elham715&layout=compact&theme=tokyonight&hide_border=true" width="49%" />

</div>
