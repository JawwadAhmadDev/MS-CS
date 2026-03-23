# Research Proposal: Explainable Identification of Human vs. Large Language Model (LLM) Generated Text

## Executive Summary

The rapid proliferation of Large Language Models (LLMs) has led to an unprecedented volume of AI-generated content across digital platforms, raising significant concerns regarding academic integrity, misinformation, and the authenticity of digital discourse. While numerous detection methodologies—ranging from traditional machine learning to advanced transformer-based architectures—have achieved high accuracy, they often operate as "black boxes," providing little insight into the reasoning behind their classifications. This research proposal outlines a comprehensive review article focused on the intersection of human vs. LLM-generated text identification and eXplainable Artificial Intelligence (XAI). 

The proposed review will synthesize current literature to evaluate the effectiveness of various detection paradigms, with a specific emphasis on how explainability techniques like LIME (Local Interpretable Model-agnostic Explanations) and SHAP (SHapley Additive exPlanations) can demystify model decisions. By building upon the foundational framework of "HULLMI: Human vs LLM identification with explainability" [1], this study aims to categorize detection strategies, analyze the role of linguistic and stylistic features, and identify critical research gaps in the development of transparent and trustworthy detection systems. This proposal serves as a roadmap for an MS-level research project, ensuring a rigorous academic approach to a pressing challenge in modern natural language processing.

## Table of Contents

1. [Introduction](#1-introduction)
2. [Problem Statement](#2-problem-statement)
3. [Objectives](#3-objectives)
4. [Research Questions](#4-research-questions)
5. [Scope](#5-scope)
6. [Methodology for the Review](#6-methodology-for-the-review)
7. [Significance](#7-significance)
8. [Preliminary Literature Synthesis](#8-preliminary-literature-synthesis)
9. [Conclusion](#9-conclusion)
10. [References](#10-references)

---

## 1. Introduction

The evolution of generative AI, particularly Large Language Models (LLMs) like GPT-4, Llama, and Claude, has revolutionized content creation but also introduced complex challenges in distinguishing between human-authored and machine-generated text. As these models become increasingly sophisticated, the "turing test" of text authenticity is becoming harder to pass, necessitating the development of robust detection tools. However, the mere identification of AI-generated text is no longer sufficient in critical domains such as academia, journalism, and legal proceedings. There is a growing demand for explainability—the ability to understand *why* a piece of text is flagged as AI-generated.

Explainability in AI-generated text detection (AGTD) is crucial for building trust and ensuring fairness. Techniques such as LIME and SHAP have emerged as prominent tools for interpreting complex models, allowing researchers to visualize feature importance and token-level contributions [2], [3]. This proposal advocates for a systematic review of the current state of explainable detection, moving beyond binary classification accuracy to focus on the qualitative insights provided by XAI. The review will explore the synergy between traditional stylometric analysis and modern transformer-based detectors, as highlighted in the HULLMI framework [1].

## 2. Problem Statement

Current methodologies for detecting LLM-generated text suffer from two primary limitations. First, while transformer-based detectors (e.g., RoBERTa, DistilBERT) achieve state-of-the-art accuracy, their internal decision-making processes are opaque, making it difficult for end-users to trust or verify their outputs [5], [13]. Second, there is a lack of consensus on which linguistic features (e.g., perplexity, burstiness, stylistic markers) are most indicative of AI generation across different models and domains [12], [19]. 

Without adequate explainability, detection tools may be prone to biases or false positives, particularly when dealing with non-native English speakers or highly technical content. The absence of a unified framework that integrates high-performance detection with intuitive, human-understandable explanations hinders the deployment of these tools in sensitive environments. This research addresses this gap by proposing a review that evaluates how XAI can be integrated into the detection pipeline to provide both accuracy and interpretability.

## 3. Objectives

The primary objective of this proposed review is to provide a comprehensive evaluation of the current landscape of explainable human vs. LLM text identification. Specific objectives include:

1.  **Categorize Detection Paradigms**: Systematically classify existing detection methods into traditional machine learning (e.g., Random Forest, XGBoost), deep learning (e.g., Transformers), and stylometric approaches [1], [4], [11].
2.  **Evaluate XAI Integration**: Analyze the application of explainability techniques—specifically LIME and SHAP—in the context of text detection and their effectiveness in identifying discriminative linguistic features [7], [8].
3.  **Assess Multi-Modal and Multi-LLM Generalization**: Examine how detection models perform across various LLMs (e.g., GPT-3.5, GPT-4, Llama, Bard) and different text types (e.g., academic abstracts, social media, medical misinformation) [9], [15], [17].
4.  **Identify Research Gaps**: Pinpoint limitations in current explainable detection methods, such as susceptibility to adversarial attacks or lack of robustness in short-sample scenarios [16], [19].

## 4. Research Questions

To guide the review, the following research questions have been formulated:

*   **RQ1**: How do traditional machine learning models compare with transformer-based architectures in terms of detection accuracy and inherent interpretability?
*   **RQ2**: To what extent do post-hoc explainability techniques (LIME, SHAP) accurately reflect the linguistic "fingerprints" left by different LLMs?
*   **RQ3**: Which stylistic and structural features are consistently identified by XAI tools as the strongest indicators of AI-generated text across diverse datasets?
*   **RQ4**: How effective are explainable detection frameworks in identifying sources of text (attribution) vs. simple binary classification (human vs. AI)?

## 5. Scope

The proposed review will focus on scholarly articles published between 2023 and 2026, capturing the most recent advancements in LLM technology and detection strategies. The scope includes:

*   **Models**: LLMs such as GPT series, Llama, Claude, Google Gemini (Bard), and specialized models for research or medical text.
*   **Techniques**: Fine-tuned transformers, ensemble models, stylistic feature extraction, and fingerprinting methods.
*   **Explainability**: Local and global interpretability methods (LIME, SHAP), attention mechanism visualization, and feature attribution.
*   **Domains**: Academic writing, online reviews, medical information, and general-purpose corpora like HC3 or M4.

The review will exclude non-textual AI generation (e.g., image or video detection) and will primarily focus on English-language texts, though multilingual studies will be included if they offer unique explainability insights [3], [11].

## 6. Methodology for the Review

The review will follow a systematic literature review (SLR) methodology to ensure transparency and reproducibility:

1.  **Search Strategy**: Electronic databases including Google Scholar, SciSpace, ArXiv, and IEEE Xplore will be searched using keywords such as "LLM text detection," "Explainable AI," "LIME/SHAP for text," and "human vs AI classification."
2.  **Selection Criteria**: Papers will be screened based on their relevance to the core topic, focusing on those that provide a methodology for both detection and explanation. High priority will be given to papers that introduce novel datasets or benchmarking frameworks like HULLMI [1].
3.  **Data Extraction**: For each selected paper, data will be extracted regarding the detection architecture, the explainability tool used, the datasets employed, and the primary linguistic findings.
4.  **Synthesis and Analysis**: A comparative analysis will be conducted to identify trends (e.g., the shift from hand-crafted features to transformer embeddings) and commonalities in explainability results.
5.  **Quality Assessment**: Each source will be evaluated based on its experimental rigor, sample size, and the clarity of its XAI application.

## 7. Significance

This research proposal is significant for several reasons. For the academic community, it provides a centralized synthesis of the rapidly evolving AGTD field, highlighting the transition toward "Glass-Box" models. For educators and publishers, the focus on explainability offers a pathway toward more justifiable and transparent plagiarism detection tools. Furthermore, by identifying the specific linguistic markers that LLMs over-utilize—such as grammatical standardization or specific word frequencies identified by SHAP [19]—this review can inform the development of more resilient detection systems. Ultimately, the proposal aligns with the MS research methods curriculum by demonstrating a rigorous application of systematic review techniques to a high-impact, contemporary technological challenge.

## 8. Preliminary Literature Synthesis

Preliminary research indicates a clear division in methodologies. Early approaches relied heavily on stylometry and classical ML. For instance, Shah et al. [8] utilized stylistic features like syllable count and punctuation ratios, using LIME and SHAP to show how indices like Simpson’s Index drive classification. Similarly, McGovern et al. [12] explored "fingerprints" through POS tag distributions and frequent tokens, though they focused more on visualization than formal XAI.

The advent of transformers shifted the focus toward deep learning. The HULLMI framework [1] demonstrates that while traditional models like Random Forest and Naive Bayes remain relevant, transformer-based detectors like RoBERTa-Sentinel offer superior performance when paired with LIME for transparency. Other studies have integrated SHAP with DistilBERT to assign feature importance values to specific words, uncovering the reasoning behind detecting short ChatGPT-generated reviews [5], [13].

Recent work has also moved toward multi-label classification and attribution. Najjar et al. [4], [20] and Darwish et al. [17] have leveraged XAI to differentiate between multiple LLMs (Llama, Bard, Claude), showing that feature importance profiles can create "author profiles" for different AI sources. This suggests that explainability is not just a secondary feature but a core component of advanced text attribution frameworks.

## 9. Conclusion

The identification of LLM-generated text is a critical task in the age of generative AI, but it must be accompanied by robust explainability to be truly effective. This proposal has outlined a structured plan for a review article that will evaluate the state of the art in explainable detection. By synthesizing the findings of 10+ core scholarly articles, the resulting review will provide a definitive guide to how XAI techniques like LIME and SHAP are transforming a once-opaque detection process into a transparent and scientifically grounded discipline.

## 10. References

[1] V. Joshi, "HULLMI: Human vs LLM identification with explainability," *arXiv preprint*, 2024. DOI: [10.48550/arxiv.2409.04808](https://doi.org/10.48550/arxiv.2409.04808)

[2] M. Masih et al., "Classifying human vs. AI text with machine learning and explainable transformer models," *Journal of AI Research* (In Press).

[3] M. Hadi et al., "Towards Explainable AI-Generated Text Detection Using Ensemble and Combined Model Training," in *Proc. XAI Conference*, 2023. DOI: [10.5281/zenodo.10433744](https://doi.org/10.5281/zenodo.10433744)

[4] A. Najjar et al., "Leveraging Explainable AI for LLM Text Attribution: Differentiating Human-Written and Multiple LLM-Generated Text," *Information*, vol. 16, no. 9, p. 767, 2025. DOI: [10.3390/info16090767](https://doi.org/10.3390/info16090767)

[5] S. Mitrović et al., "ChatGPT or Human? Detect and Explain. Explaining Decisions of Machine Learning Model for Detecting Short ChatGPT-generated Text," *arXiv preprint*, 2023. DOI: [10.48550/arxiv.2301.13852](https://doi.org/10.48550/arxiv.2301.13852)

[6] J. Mc, "Classifying AI vs. Human Content: Integrating BERT and Linguistic Features for Enhanced Classification," *Current Psychology*, 2025. DOI: [10.1007/s43069-025-00486-1](https://doi.org/10.1007/s43069-025-00486-1)

[7] S. Ali et al., "Interpretable Multi-Label Classification of Human-and Large Language Model-Generated Texts Using Transformer Embeddings and Explainable Artificial Intelligence," *IEEE Access*, 2024.

[8] Y. Shah et al., "Detecting and unmasking AI-generated texts through explainable artificial intelligence using stylistic features," *International Journal of Advanced Computer Science and Applications*, vol. 14, no. 10, 2023. DOI: [10.14569/ijacsa.2023.01410110](https://doi.org/10.14569/ijacsa.2023.01410110)

[9] H. Baharifar et al., "Interpretable AI for Classifying Human-and LLM-Generated Medical Misinformation with Multi-Modal Features," *Health Informatics Journal*, 2025.

[10] Anonymous, "Assessing Classical Machine Learning and Transformer-based Approaches for Detecting AI-Generated Research Text," *arXiv preprint*, 2025. DOI: [10.48550/arxiv.2509.20375](https://doi.org/10.48550/arxiv.2509.20375)

[11] M. Adilazuarda et al., "Beyond Turing: A Comparative Analysis of Approaches for Detecting Machine-Generated Text," *arXiv preprint*, 2023. DOI: [10.48550/arxiv.2311.12373](https://doi.org/10.48550/arxiv.2311.12373)

[12] A. McGovern et al., "Your Large Language Models Are Leaving Fingerprints," *arXiv preprint*, 2024. DOI: [10.48550/arxiv.2405.14057](https://doi.org/10.48550/arxiv.2405.14057)

[13] S. Mitrović et al., "ChatGPT or Human? Detect and Explain. Explaining Decisions of Machine Learning Model for Detecting Short ChatGPT-generated Text," *arXiv preprint*, 2023. DOI: [10.48550/arXiv.2301.13852](https://doi.org/10.48550/arXiv.2301.13852)

[14] L. Breneur et al., "NOTAI. AI: Explainable Detection of Machine-Generated Text via Curvature and Feature Attribution," *Nature Machine Intelligence* (In Review).

[15] M. Iqbal et al., "A Machine Learning Framework for Identifying Sources of AI-Generated Text," *Stat., Optim. Inf. Comput.*, 2025. DOI: [10.19139/soic-2310-5070-2225](https://doi.org/10.19139/soic-2310-5070-2225)

[16] S. Mohammadi et al., "Explainability-based token replacement on llm-generated text," *arXiv preprint*, 2025. DOI: [10.48550/arxiv.2506.04050](https://doi.org/10.48550/arxiv.2506.04050)

[17] Y. Darwish et al., "Leveraging Explainable AI for LLM Text Attribution: Differentiating Human-Written and Multiple LLM-Generated Text," *University of Maryland Repository*, 2025. DOI: [10.13016/m2ikuj-ao0b](https://doi.org/10.13016/m2ikuj-ao0b)

[18] S. Ardeshirifar, "Comparing hand-crafted and deep learning approaches for detecting AI-generated text: performance, generalization, and linguistic insights," *AI and Ethics*, 2025. DOI: [10.1007/s43681-025-00699-4](https://doi.org/10.1007/s43681-025-00699-4)

[19] I. Grabska-Gradzińska et al., "Stylometry recognizes human and LLM-generated texts in short samples," *arXiv preprint*, 2025. DOI: [10.48550/arxiv.2507.00838](https://doi.org/10.48550/arxiv.2507.00838)

[20] A. Najjar et al., "Leveraging Explainable AI for LLM Text Attribution: Differentiating Human-Written and Multiple LLMs-Generated Text," *arXiv preprint*, 2025. DOI: [10.48550/arxiv.2501.03212](https://doi.org/10.48550/arxiv.2501.03212)
