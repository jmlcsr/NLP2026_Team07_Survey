# Project Proposal

## 1. Project Title

**How Reliable Are LLM Judges? A Survey of Evaluation Protocols, Biases, and Validation Methods**

**Project Track:** Track A — Survey

## 2. Team Members & Responsibilities

| Member | Responsibilities |
|---|---|
| 2310412 Hao Purui | Research scope, core questions, evaluation protocols, and taxonomy. |
| 2311871 Liu Xincheng | Evaluation biases, reliability improvements, open problems, and future directions. |

Both members will jointly verify the literature, integrate and proofread the report, and prepare the final presentation.

## 3. Background & Motivation

Large language models are widely used for dialogue, open-domain question answering, summarization, and instruction following. Metrics such as BLEU and ROUGE are insufficient for open-ended responses, while human evaluation is costly and subject to annotator disagreement.

LLM-as-a-Judge uses a large language model to score, compare, rank, or explain model outputs. However, judges may be affected by response position, length, style, self-preference, and prompt formulation, reducing agreement with human judgments or changing model rankings.

Unlike broad existing surveys, this project focuses on judge reliability through the framework of “evaluation protocols—evaluation bases—validation and improvements.” It distinguishes agreement, consistency, and validity and emphasizes when judges genuinely reflect response quality.

## 4. Problem Definition / Research Questions

### 4.1 Research Scope

The project covers LLM evaluation of open-ended generation, dialogue, and question answering, including pairwise/listwise comparison and agreement with human judgments. BLEU, ROUGE, BERTScore, BLEURT, and BARTScore are background baselines; other NLP metrics and RLHF reward-model training are out of scope.

### 4.2 Research Questions

1. How do Point-wise, Pair-wise, and List-wise evaluation protocols, as well as Reference-based, Reference-free, Evidence-based, and Rubric-based evaluation bases, differ in their objectives, output formats, and applicable scenarios?
2. What systematic biases and failure modes affect LLM judges? How do position bias, length/style bias, self-preference, and scoring instability affect evaluation results?
3. Can response-order swapping, repeated sampling and aggregation, Judge Ensemble, human calibration, and external evidence improve evaluation reliability?
4. How should agreement, consistency, and validity be combined to determine whether an LLM judge genuinely reflects response quality, while balancing cost, interpretability, and reproducibility?

### 4.3 Preliminary Taxonomy

The project will develop a three-level taxonomy:

1. **Evaluation protocols:** Point-wise, Pair-wise, and List-wise evaluation;
2. **Evaluation bases:** Reference-based, Reference-free, Evidence-based, and Rubric-based evaluation;
3. **Validation and reliability improvements:** human agreement, test-retest consistency, objective-correctness benchmarks, prompt/rubric design, sampling and aggregation, Judge Ensemble, human calibration, and external evidence.

The comparison will distinguish **agreement**, **consistency**, and **validity**, while considering task type, references, evaluation dimensions, bias, cost, interpretability, and cross-task generalization. Consistency does not guarantee validity: a judge may consistently prefer a format without recognizing answer quality.

## 5. Expected Outcomes

1. Collect and verify at least 20 relevant papers and establish the three-level taxonomy.
2. Create a comparison table covering the strengths, limitations, and use cases of protocols and improvements.
3. Summarize position, length/style, self-preference, and prompt-sensitivity biases, and compare agreement, consistency, and validity.
4. Analyze protocol standardization, bias calibration, objective correctness, multilingual evaluation, and reproducibility, and propose future directions.

## 6. Project Timeline

| Stage | Planned Work |
|---|---|
| Before proposal submission | Finalize the scope, research questions, responsibilities, and initial literature verification. |
| Weeks 1–4 after submission | Screen at least 25 candidate papers and select 20 core papers; refine the taxonomy, comparison table, and interim results. |
| After the midterm milestone | Complete the review, comparison, open-problem analysis, report, slides, and contribution statement. |

The dates of the midterm milestone and final submission will follow the instructor's later announcement.

## References

The following references have been verified through ACL Anthology, arXiv, OpenReview, PMLR, or official conference pages. The final report will cite at least 20 papers, with recent work from 2024–2026 forming the main body of the review.

1. Lianmin Zheng et al. 2023. [Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena](https://arxiv.org/abs/2306.05685). NeurIPS 2023, Datasets and Benchmarks Track.
2. Yang Liu, Dan Iter, Yichong Xu, Shuohang Wang, Ruochen Xu, and Chenguang Zhu. 2023. [G-Eval: NLG Evaluation using GPT-4 with Better Human Alignment](https://aclanthology.org/2023.emnlp-main.153/). EMNLP 2023.
3. Jiawei Gu et al. 2024. [A Survey on LLM-as-a-Judge](https://arxiv.org/abs/2411.15594). arXiv:2411.15594.
4. Peiyi Wang et al. 2024. [Large Language Models are not Fair Evaluators](https://aclanthology.org/2024.acl-long.511/). ACL 2024.
5. Guiming Hardy Chen, Shunian Chen, Ziche Liu, Feng Jiang, and Benyou Wang. 2024. [Humans or LLMs as the Judge? A Study on Judgement Bias](https://aclanthology.org/2024.emnlp-main.474/). EMNLP 2024.
6. Wei-Lin Chiang et al. 2024. [Chatbot Arena: An Open Platform for Evaluating LLMs by Human Preference](https://proceedings.mlr.press/v235/chiang24b.html). ICML 2024, PMLR 235, 8359–8388.
7. Sijun Tan et al. 2025. [JudgeBench: A Benchmark for Evaluating LLM-based Judges](https://arxiv.org/abs/2410.12784). ICLR 2025.
8. Anna Bavaresco et al. 2025. [LLMs instead of Human Judges? A Large Scale Empirical Study across 20 NLP Evaluation Tasks](https://aclanthology.org/2025.acl-short.20/). ACL 2025.
9. Lin Shi, Chiyu Ma, Wenhua Liang, Xingjian Diao, Weicheng Ma, and Soroush Vosoughi. 2025. [Judging the Judges: A Systematic Study of Position Bias in LLM-as-a-Judge](https://aclanthology.org/2025.ijcnlp-long.18/). IJCNLP-AACL 2025.
10. Hui Huang et al. 2025. [An Empirical Study of LLM-as-a-Judge for LLM Evaluation: Fine-tuned Judge Model is not a General Substitute for GPT-4](https://aclanthology.org/2025.findings-acl.306/). Findings of ACL 2025.
11. Aman Singh Thakur et al. 2025. [Judging the Judges: Evaluating Alignment and Vulnerabilities in LLMs-as-Judges](https://aclanthology.org/2025.gem-1.33/). GEM 2025.
12. Yilun Zhou et al. 2025. [Evaluating Judges as Evaluators: The JETTS Benchmark of LLM-as-Judges as Test-Time Scaling Evaluators](https://arxiv.org/abs/2504.15253). ICML 2025.
13. Yusuke Yamauchi, Taro Yano, and Masafumi Oyamada. 2026. [An Empirical Study of LLM-as-a-Judge: How Design Choices Impact Evaluation Reliability](https://aclanthology.org/2026.gem-main.19/). GEM 2026.
14. Zhengyu Hu, Linxin Song, Jieyu Zhang, Zheyuan Xiao, Tianfu Wang, Zhengyu Chen, Nicholas Jing Yuan, Jianxun Lian, Kaize Ding, and Hui Xiong. 2025. [Explaining Length Bias in LLM-Based Preference Evaluations](https://aclanthology.org/2025.findings-emnlp.358/). Findings of EMNLP 2025, 6763–6794.
15. Pat Verga, Sebastian Hofstätter, Sophia Althammer, Yixuan Su, Aleksandra Piktus, Arkady Arkhangorodsky, Minjie Xu, Naomi White, and Patrick Lewis. 2024. [Replacing Judges with Juries: Evaluating LLM Generations with a Panel of Diverse Models](https://arxiv.org/abs/2404.18796). arXiv preprint, arXiv:2404.18796.
