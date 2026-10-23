# Beetle: A Bilingual Model Suite for Studying How Language Models Learn Language

Welcome to **Beetle** 🪲, a research project for studying **how language exposure shapes what language models learn**, with a focus on bilingual and second-language processing. Beetle was published at **EMNLP 2026** (Oral, top 3%). We release four complementary frameworks for training, building data for, analyzing, and exploring a large suite of controlled language models. Our mission is to make it possible to vary one factor at a time and watch, step by step, how a model's knowledge of language forms. Read the paper: [arxiv.org/abs/2609.22633](https://arxiv.org/abs/2609.22633).

1. [**beetlelm**](https://github.com/beetlelm/beetlelm) 🪲  
   The **training framework**. It ships a **PicoDecoder** (125M LLaMA-style auto-regressive transformer) alongside an **architecture zoo** (BGPT, BeetleMoE, BeetleSSM), and modular **BPE / Unigram / SuperBPE** tokenisation tuned for **equal compression** across languages. Beetle defines the **B1–B5 exposure curricula** and **15 continual-learning strategies** so you can control exactly how and when a model meets each language. Checkpoints are **richly annotated** with **gradients and activations** and saved on a **log2 schedule** for studying learning dynamics, and all checkpoints are **Hugging Face-compatible**. Tutorial: [beetlelm.github.io/docs.html#beetlelm](https://beetlelm.github.io/docs.html#beetlelm).

2. [**beetle-data**](https://github.com/beetlelm/beetle-data) 🗂️  
   The **data pipeline**. It **builds and streams corpora** from **BabyBabelLM**, **FineWeb-2**, and **FineWeb-Edu**, applies **13-gram decontamination**, **trains tokenisers**, and **pretokenises** everything into shards ready for training. This is where the controlled data conditions behind every Beetle model are produced, consistently and reproducibly. Tutorial: [beetlelm.github.io/docs.html#beetle-data](https://beetlelm.github.io/docs.html#beetle-data).

3. [**beetle-analyze**](https://github.com/beetlelm/beetle-analyze) 📊  
   The **evaluation toolkit**. It measures grammatical and cross-lingual competence with **BLiMP** minimal pairs, **MECO** reading-time alignment, **BLiSS** learner grammaticality, **FLORES-200** NLL, and **cross-lingual structural priming**. It **reproduces the paper's results** end to end, so every number can be independently checked. Tutorial: [beetlelm.github.io/docs.html#beetle-analyze](https://beetlelm.github.io/docs.html#beetle-analyze).

4. [**beetle-explorer**](https://github.com/beetlelm/beetle-explorer) 🔭  
   A **no-code Colab** for loading any Beetle checkpoint and generating text. It lets anyone poke at the models directly, no setup required. Tutorial: [beetlelm.github.io/docs.html#beetle-explorer](https://beetlelm.github.io/docs.html#beetle-explorer).

---

## **Further Resources**

**Beetle Model Suite**: We use **beetlelm** to train **285 bilingual** and **45 monolingual** models spanning **21 first languages**, with **~30 checkpoints each** at **100M / 2B / 24B** token scales.
  - Each checkpoint includes weights, **gradients**, and **activations** for interpretability
  - Available on 🤗 [Hugging Face](https://huggingface.co/Beetle-HumanScale) and the associated collections
  - The genuine full-scale final release is **Beetle-FineWeb-24B-4** and **Beetle-FineWeb-24B-5**

**Datasets & Tokenisers**: The controlled corpora and tokenisers behind every model.
  - Stream-ready and decontaminated for easy, reproducible training
  - Available on 🤗 [Hugging Face](https://huggingface.co/Beetle-Data)

**Documentation & Tutorials**: Visit [beetlelm.github.io](https://beetlelm.github.io) for step-by-step tutorials and reference:
  - [Home](https://beetlelm.github.io)
  - [Research](https://beetlelm.github.io/research.html)
  - [Models & Data](https://beetlelm.github.io/models.html)
  - [Framework](https://beetlelm.github.io/framework.html)
  - [Docs](https://beetlelm.github.io/docs.html)

---
## **Our Philosophy: What Makes Beetle Special?**

Beetle is designed for **controlled**, **transparent** experiments that bridge machine learning and cognitive science. Here's how we stand apart:

1. **Vary One Factor at a Time**  
   Every Beetle model isolates a single variable, whether it is the **first language (L1)**, the **exposure curriculum**, or the **data scale**. By holding everything else fixed, we can attribute what a model learns to the conditions it was trained under, rather than to confounds.

2. **Full Training Checkpoints for Interpretability**  
   We save **~30 checkpoints per model** on a log2 schedule, each carrying **gradients and activations** as well as weights. This granular record lets researchers study how linguistic knowledge emerges across training, not just at the end.

3. **Open Models, Data, and Code**  
   Every model, dataset, tokeniser, and line of code is released under the **Apache License 2.0**. Nothing is hidden, so results can be reproduced, extended, and challenged by anyone.

4. **Bridging ML and Cognitive Science**  
   Beetle's evaluations (reading-time alignment, learner grammaticality, cross-lingual priming) connect model behavior to **human language processing**, making the suite as useful for studying bilingual acquisition as for building models.

---

## **Stay Connected**

- **Website**: [beetlelm.github.io](https://beetlelm.github.io) for tutorials, documentation, and results
- **GitHub**: Star our repositories or open issues / pull requests to get involved
- **Hugging Face**: [Beetle-HumanScale](https://huggingface.co/Beetle-HumanScale) and [Beetle-Data](https://huggingface.co/Beetle-Data) for all our models, datasets, and tokenisers

---

## **License**

All Beetle software is open-source under the [Apache License 2.0](LICENSE).

---

## **Citation**

If you use **Beetle** in your research, please cite:

```bibtex
@inproceedings{beetle2026,
    title = "Beetle: A Bilingual Model Suite for Studying How Language Models Learn Language",
    booktitle = "Proceedings of the 2026 Conference on Empirical Methods in Natural Language Processing",
    year = "2026",
    note = "Oral (top 3\%)",
    url = "https://arxiv.org/abs/2609.22633",
}
```

**Happy experimenting!**  
We hope Beetle helps you understand **how language exposure shapes what language models learn**.
