# Biologically informed deep learning for discovery of drug targets for PIK3CA mutated breast cancers

![Project Banner](banner0.png) 
## 🚀 Introduction

Welcome to the official repository for the **BI-BRCA-Net-LLM**! This project introduces BI-BRCA-Net, a biologically informed, explainable deep learning methodology, to investigate the mechanistic differences between PIK3CA mutant and wild type breast cancer based on the recently published P-Net architecture [1]. By integrating multiomics data (including DNA copy number, gene expression levels, methylation, and gene mutations) through an explainable neural network architecture, BI-BRCA-Net leverages existing biological knowledge to validate functional interactions. It aims to identify and later to experimentally confirm the functional modules and pathways prevalent in PIK3CA mutant breast cancer [2]. The objective is to use Large Language Models (LLMs) to invent novel hypotheses on how to limit the growth of cancer cells by targeting identified pathways, validated through the suppression of critical pathway genes and evaluating their effects on cellular proliferation.


```diff
- Important note: The agentic LLM workflow is still prone to hallucinating. Always double-check the generated hypotheses for biological validity. Treat this solution as an interesting experiment.

```

## 📚 Overview

![Project Banner](banner.png) 



## 📚 Features

- **BI-BRCA-Net Introduction**: Presenting BI-BRCA-Net, a biologically informed, explainable deep learning methodology designed to explore the mechanistic differences between PIK3CA mutant and wild type breast cancer, building on the recently published P-Net architecture.

- **Multiomics Data Integration**: BI-BRCA-Net integrates various multiomics data types, including DNA copy number, gene expression levels, methylation, and gene mutations, through an explainable neural network architecture. This approach leverages existing biological knowledge to validate functional interactions.


- **Hypothesis Generation Using LLMs**: Utilizing Large Language Models (LLMs), BI-BRCA-Net generates novel hypotheses on limiting cancer cell growth by targeting identified pathways. These hypotheses are validated by suppressing critical pathway genes and evaluating their effects on cellular proliferation.

- **High-Quality Output**: Ensures the use of state-of-the-art language models to produce high relevance and quality of generated ideas, with in-vitro and in-silico validation recommendations.

- **User-Friendly Interface**: Features an easy-to-use interface for seamless hypothesis generation and validation, facilitating the process for researchers and clinicians (work in progress).





## 🌟 Demo

Check out our [live demo]() to see the app in action! Currently, the hypothesis generator part of the model is hosted here.

## 🛠️ Installation

To get started, clone this repository (a modified version of Pnet) and install the necessary dependencies:

```bash
git clone https://github.com/Paureel/BI-BRCA-NET
cd LLM-SCIGEN-BRCA
pip install -r requirements.txt
```


## 🚀 Usage

1. For the biologically informed deep learning part fit your model using one of the notebooks shown in the BI-BRCA-NET repository.

2. To generate scientific ideas, simply run the following command to launch the app:

```bash
streamlit run app.py
```



## 🧩 How It Works

The model is based on the Reflexion agentic workflow by Shinn et al. https://github.com/langchain-ai/langgraph/blob/main/examples/reflexion/reflexion.ipynb. By inputting a custom prompt, the model generates a series of potential ideas or research questions that could inspire your next scientific endeavor.

The final output is a csv file, with the following columns:

- **Hypotheses short description**: One sentence description of the hypothesis.
- **Generated Hypotheses**: Long description of the generated hypothesis.
- **Novelty**: 1-10 score on novelty.
- **What is not novel**: Description of what is not novel.
- **Missing**: What is missing from the description of the hypothesis.
- **Superfluous**: What is redundant in the description of the hypothesis.
- **Flag**: Is there anything unusual about the input?
- **References**: References from the literature.
- **Biohazard**: Is there anything dangerous in the generated hypothesis?
- **Relations to literature**: Description on how the hypothesis relates to the published papers in the field.



## 🤝 Contributing

Contributions are welcome! If you'd like to contribute to this project, please fork the repository and create a pull request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.

## 🙌 Acknowledgements

This project was conceived during Breast cancer genomics hackathon event 
organized by the Susan G Komen for the Cure and University of Texas Southwestern in 
2023 and currently supported by Susan G Komen for the Cure (OG241196018


## 🌐 Connect with Us

- [GitHub Issues](https://github.com/Paureel/scientific-idea-generator/issues)
- [Discussions](https://github.com/Paureel/scientific-idea-generator/discussions)
- [Twitter/X](https://x.com/aurel_pr)
- [LLM-SCI-GEN](https://github.com/Paureel/LLM-SCI-GEN) Papers about scientific hypothesis generation with large language models (LLMs), maintained by me. Check it out if you are interested in this topic.

## 📜 References

[1] Elmarakeby, Haitham A et al. “Biologically informed deep neural network for prostate cancer discovery.” Nature vol. 598,7880 (2021): 348-352. doi:10.1038/s41586-021-03922-4
[2] Reinhardt K et al. "PIK3CA-mutations in breast cancer. Breast Cancer" Res Treat. 2022 Dec;196(3):483-493. doi: 10.1007/s10549-022-06637-w. PMID: 36279023
[3] Börcsök, Judit et al. “Identification of a Synthetic Lethal Relationship between Nucleotide  Excision Repair Deficiency and Irofulven Sensitivity in Urothelial Cancer.” Clinical cancer research vol. 27,7 (2021): 2011-2022. doi:10.1158/1078-0432.CCR-20-3316