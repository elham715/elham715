<div align="center">

# Hi, I'm Elham 👋
### *AI Research Engineer | Foundation Models, Systems Engineering & Computational Oncology*

[![GitHub followers](https://img.shields.io/github/followers/elham715?style=for-the-badge&logo=github&color=24292e)](https://github.com/elham715)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin)](https://linkedin.com)
[![Email](https://img.shields.io/badge/Email-elham4ml.ai@gmail.com-EA4335?style=for-the-badge&logo=gmail)](mailto:elham4ml.ai@gmail.com)

```
"What I cannot create, I do not understand." — Richard Feynman
```

</div>

---

### 🧬 About Me & Research Focus

I operate at the convergence of **First-Principles LLM Systems Engineering** and **Computational Oncology / Protein Language Models**.

My work focuses on eliminating "black-box wrapper dependencies": building, deriving, and mathematically verifying modern deep architectures directly from **tensor calculus and silicon hardware physics** up to **mechanistic post-training alignment**, and grounding attention mechanics in **clinical drug resistance, non-coding cancer genomics, and metabolic reaction networks**.

- ⚡ **LLM Silicon Systems Engineering**: Building the complete modern Transformer backbone from scratch in pure PyTorch ([`llm-engineering-lab`](https://github.com/elham715/llm-engineering-lab)) — from RoPE 2D complex rotation planes, scale-invariant RMSNorm, and GQA stride broadcasting to LoRA associative matrix memory, DPO closed-form Bradley-Terry loss, and Leviathan speculative decoding.
- 🔬 **Protein Language Models & Structural Oncology**: Pioneering mechanistic attention disruption in oncogenic kinases ([`oncogenic-attention-disruption`](https://github.com/elham715/oncogenic-attention-disruption)) — proving that Meta's ESM-2 self-attention maps autonomously quantify covalent drug resistance (EGFR C797S / Osimertinib) and align with experimental crystal structures (PDB `2J6M`, $r_s = 0.4464$) without 3D training labels.
- 🧬 **Multimodal Chemistry, Promoters & Metabolic Graphs**: 
  - Cross-attending small-molecule inhibitor SMILES with 128 hallmark cancer genes ([`cross-attention-drug-synergy`](https://github.com/elham715/cross-attention-drug-synergy)).
  - Modeling 512 bp non-coding regulation and In Silico Saturation Mutagenesis at *TERT* promoter hotspots $C228T$/$C250T$ ([`promoter-variant-transformer`](https://github.com/elham715/promoter-variant-transformer)).
  - Predicting oncogenic *IDH1* $R132H$ oncometabolite shunts via Floyd-Warshall shortest-path distance (SPD) Graphormer attention ([`biopath-reaction-transformer`](https://github.com/elham715/biopath-reaction-transformer)).
- 📐 **Rigorous Engineering Standard**: Zero external black-box frameworks for core algorithms, verified mathematical invariants (analytical gradchecks $\le 10^{-10}$, step-0 LoRA identity, RMSNorm scale invariance), and **61 verified unit tests** across all repositories.

---

### 🏆 Featured Research & Engineering Laboratories

#### 1. ⚡ LLM Engineering Lab (Silicon Physics to Post-Training Alignment)
*Repository: [**`llm-engineering-lab`**](https://github.com/elham715/llm-engineering-lab)* • [![Tests](https://img.shields.io/badge/Tests-21%2F21%20Passing-brightgreen.svg)](https://github.com/elham715/llm-engineering-lab) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **A zero-black-box systems repository implementing 7 modern LLM engines from scratch in pure PyTorch:**

| # | Engine | Mathematical & Systems Core | Status | Verification |
|---|---|---|:---:|:---:|
| **01** | [`01_gpt2_from_scratch/`](https://github.com/elham715/llm-engineering-lab/tree/main/01_gpt2_from_scratch) | **Full GPT-2 (124M)**: Causal MHA, `Conv1D` weight transfer from OpenAI checkpoints, weight tying, and Top-K/Top-p nucleus sampling. | **Verified** 🟢 | [test_model.py](https://github.com/elham715/llm-engineering-lab/blob/main/01_gpt2_from_scratch/test_model.py) |
| **02** | [`02_chronosteer_studio/`](https://github.com/elham715/llm-engineering-lab/tree/main/02_chronosteer_studio) | **ChronoSteer Studio**: Real-time interpretability UI (`bfloat16` CPU + WebSockets). Dynamic KV time-travel rewind, Layer-6 contrastive steering, and 360° future-word wheel. | **Verified** 🟢 | Live Web GUI |
| **03** | [`03_bpe_tokenizer/`](https://github.com/elham715/llm-engineering-lab/tree/main/03_bpe_tokenizer) | **Byte-Level BPE**: 256-byte UTF-8 base vocab, iterative pair frequency counting, regex pre-tokenization, zero `<unk>` guarantee, verified round-trip on Bengali and biochemical sequences. | **Verified** 🟢 | [test_bpe.py](https://github.com/elham715/llm-engineering-lab/blob/main/03_bpe_tokenizer/test_bpe.py) |
| **04** | [`04_modern_architecture_gqa_rope/`](https://github.com/elham715/llm-engineering-lab/tree/main/04_modern_architecture_gqa_rope) | **LLaMA-3 / Mistral Backbone**: Rotary Position Embeddings (RoPE 2D complex rotation), scale-invariant RMSNorm ($c \cdot x \equiv x$), SwiGLU gating ($\lfloor \frac{8}{3}d \rfloor$), and GQA zero-copy broadcasting. | **Verified** 🟢 | 6/6 Passing |
| **05** | [`05_lora_peft_from_scratch/`](https://github.com/elham715/llm-engineering-lab/tree/main/05_lora_peft_from_scratch) | **LoRA & QLoRA NF4**: $W_0 + \frac{\alpha}{r} (BA)$ with $B=0$, associative matrix memory trick $(x A^T) B^T$ ($O(r)$ memory), zero-latency weight merging, and 16-quantile NormalFloat4 quantization. | **Verified** 🟢 | 6/6 Passing |
| **06** | [`06_preference_optimization_dpo/`](https://github.com/elham715/llm-engineering-lab/tree/main/06_preference_optimization_dpo) | **Direct Preference Optimization (DPO)**: Closed-form Bradley-Terry preference loss, analytical partition function $Z(x)$ cancellation, autoregressive target shift (`:-1` vs `1:`), and prompt masking (`-100`). | **Verified** 🟢 | 5/5 Passing |
| **07** | [`07_inference_kvcache_speculative_decoding/`](https://github.com/elham715/llm-engineering-lab/tree/main/07_inference_kvcache_speculative_decoding) | **High-Throughput Inference Engine**: Dynamic zero-reallocation static KV cache and Leviathan/Chen Speculative Decoding with rejection sampling for $2\times\text{–}3\times$ speedup preserving exact target distribution. | **Verified** 🟢 | 4/4 Passing |

---

#### 2. 🧬 The 4 Bio-ML & Genomic Transformer Laboratories

```
┌─────────────────────────────────┬──────────────────────────────────────────┬───────────┬──────────────┐
│ Repository                      │ Biological & Architectural Core          │ Tests     │ CPU Training │
├─────────────────────────────────┼──────────────────────────────────────────┼───────────┼──────────────┤
│ oncogenic-attention-disruption  │ Meta ESM-2 Attention & EGFR C797S PDB    │  9 /  9 🟢│ Inference    │
│ cross-attention-drug-synergy    │ SMILES × 128 RNA-seq Cross-Attention     │ 12 / 12 🟢│ 90.8s        │
│ promoter-variant-transformer    │ RoPE Enformer TERT Promoter ISM          │ 11 / 11 🟢│ 121.1s       │
│ biopath-reaction-transformer    │ Graphormer Floyd-Warshall SPD Attention  │  8 /  8 🟢│ 13.0s        │
└─────────────────────────────────┴──────────────────────────────────────────┴───────────┴──────────────┘
```

##### A. 🔬 [Mechanistic Attention Disruption in Oncogenic Kinases](https://github.com/elham715/oncogenic-attention-disruption)
* **Zero-Coordinate Resistance Discovery**: Proves Meta's ESM-2 autonomously detects the fatal Osimertinib resistance mutation **C797S** as the **#2 top disrupted residue** ($\text{ADI} = 9.3 \times 10^{-5}$) and the **Met793 hinge donor** as **#3**, capturing covalent bond loss and allosteric active-site transmission without 3D training labels.
* **Crystallographic PDB Alignment**: Evaluated against the human EGFR crystal structure (**PDB `2J6M`**), achieving a **0.4464 Spearman rank correlation** between internal ESM-2 attention weights and ground-truth spatial proximity ($1/D_{ij}$ in $\text{\AA}$) across 306 $C_\alpha$ atoms.

##### B. 💊 [Bi-modal Cross-Attention for Anticancer Drug Sensitivity](https://github.com/elham715/cross-attention-drug-synergy)
* **Chemical $\longleftrightarrow$ Pathway Crosstalk**: Modernizing PaccMann (*Cell Reports Methods / IBM Research, 2021*) into a full bi-modal Transformer. Fuses small-molecule inhibitor SMILES with 128 landmark cancer genes partitioned across 8 canonical oncogenic hallmark pathways (`RTK_EGFR`, `PI3K_AKT_MTOR`, `RAS_RAF_MEK_MAPK`, `CELL_CYCLE_CDK`, `DNA_DAMAGE_REPAIR`, `APOPTOSIS_SURVIVAL`, `ANGIOGENESIS`, `EPIGENETIC`).
* **Performance**: Finished 15-epoch CPU training in **90.8s** with test Spearman $\rho = 0.3123$ and Pearson $r = 0.2997$ across GDSC cell lines.

##### C. 🧬 [RoPE Enformer for Non-Coding Cancer Driver Mutations](https://github.com/elham715/promoter-variant-transformer)
* **In Silico Saturation Mutagenesis (ISM)**: Models the 512 bp human *TERT* promoter with Rotary Position Embeddings (RoPE), a $4\times$ Enformer-style downsampling stem ($512 \to 128$ bp, $10\times$ CPU speedup), and 4-layer Transformer backbone.
* **Hotspot Reactivation**: Evaluates all $512 \times 3 = 1,536$ single-nucleotide mutations, accurately capturing the de novo `GGAA` GABP/ETS transcription factor motif creation at canonical hotspot mutations **`C228T`** ($-124\text{ C}>\text{T}$) and **`C250T`** ($-146\text{ C}>\text{T}$).

##### D. ⚡ [Graphormer SPD Attention for Metabolic Networks](https://github.com/elham715/biopath-reaction-transformer)
* **Geodesic Spatial Bias**: Injects discrete all-pairs Floyd-Warshall Shortest-Path Distance (SPD) matrices into Multi-Head Attention ($\mathbf{A}_{ij} = \frac{\mathbf{q}_i \mathbf{k}_j^T}{\sqrt{d_k}} + \mathbf{B}_{\text{SPD}(i,j)}$) across 25 human metabolites and 16 canonical enzymes.
* **Oncogenic *IDH1* $R132H$ Neomorphic Shunt**: Trained in **13.0s** on CPU with **Spearman $\rho = 0.9453$** on primary flux and **$\rho = 0.8764$** on oncometabolites, capturing the **$1.81\times$ surge** in 2-hydroxyglutarate (2-HG) accumulation.

---

#### 3. 🔬 Seminal Paper Reproductions
*Repository: [**`first-principles-ai-lab`**](https://github.com/elham715/first-principles-ai-lab)*

* **Sequence Foundations (5 Papers)**:
  * **Elman (1990)** *"Finding Structure in Time"*: Pure NumPy SRN, manual BPTT, analytical gradcheck ($\le 6.93 \times 10^{-11}$), and vanishing gradient proof — *Completed & Verified* 🟢
  * **Hochreiter & Schmidhuber (1997)** *"LSTM"*: Constant Error Carousel (CEC) & additive gating — *Completed* 🟢
  * **Bengio et al. (2003)**, **Sutskever et al. (2014)**, **Bahdanau et al. (2014)** — *In Progress* 🟡
* **Modern Transformer Core (6 Papers Unified in One Engine)**:
  * **Vaswani (2017)** *Attention* + **Radford (2019)** *GPT-2* + **Zhang (2019)** *RMSNorm* + **Shazeer (2020)** *SwiGLU* + **Su (2021)** *RoPE* + **Ainslie (2023)** *GQA* — *Fully Implemented & Verified in `llm-engineering-lab`* 🟢
* **Alignment & High-Throughput Inference**:
  * **Rafailov et al. (2023)** *DPO* + **Hu et al. (2021)** *LoRA* + **Leviathan et al. (2022)** *Speculative Decoding* — *Verified* 🟢

---

#### 4. 🩺 Biomedical Vision & Signal Intelligence
*Repositories: [**`biomedical-cnn-lab`**](https://github.com/elham715/biomedical-cnn-lab) • [**`biomedical-sequence-lab`**](https://github.com/elham715/biomedical-sequence-lab)*

* **COPD Respiratory Acoustic ConvNet**: Converting stethoscope recordings (ICBHI 2017) into 2D Log-Mel Spectrograms with Grad-CAM explainability to classify COPD vs. Healthy.
* **Neuroscience EEG ShallowConvNet (Schirrmeister et al., 2017)**: Decoding motor imagery from raw 64-channel PhysioNet EEG brainwaves and visualizing learned Alpha/Beta cortical frequency filters.
* **Oncolytic Peptide Modeling**: Predicting tumor-lysing antimicrobial peptide activity directly from amino-acid sequences via BiLSTM with additive attention.

---

### 🛠️ Technical Arsenal

<div align="center">

| Domain | Systems, Tools & Mathematical Foundations |
|---|---|
| **Foundation Models & LLM Systems** | Autoregressive Transformers, Causal Attention, RoPE 2D Rotations, GQA, RMSNorm, SwiGLU Gating, LoRA / QLoRA NF4, Static KV-Cache, Speculative Decoding, DPO Alignment |
| **Protein & Genomic Transformers** | Meta ESM-2, Attention Disruption ($\Delta \mathbf{A}$), PDB $C_\alpha$ Euclidean Coordinates, Contact Precision @ $L/5$, Enformer 1D Conv Stem, In Silico Saturation Mutagenesis (ISM) |
| **Graph & Chemical Learning** | Graphormer Shortest-Path Distance (SPD) Bias, Floyd-Warshall DP, SMILES Tokenization, Bilinear Multimodal Interaction Pooling |
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
