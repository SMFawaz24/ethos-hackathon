# Ethos Hackathon Project

This repository contains the project developed for the Ethos Hackathon. The entire project is built using Jupyter Notebooks.

##  Table of Contents
- [About the Project](#-about-the-project)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#-usage)
- [Contributing](#-contributing)
- [License](#-license)
- [Acknowledgments](#-acknowledgments)

##  About the Project

### The Problem
This project was developed for the Saptang Labs Machine Learning Challenge, which addresses a critical limitation in modern Large Language Models (LLMs): their struggle with structured, multi-step logical reasoning. While LLMs can generate fluent text, they often fail to decompose complex problems, leading to unreliable answers. The challenge was to design and build an Agentic AI system that could not only solve logic puzzles but also provide transparent, human-readable reasoning for its conclusions.

### Our Goal
Our primary goal for this hackathon was to build a robust, hybrid system that could successfully tackle both the prediction and the explanation aspects of the challenge. We aimed to create a complete, end-to-end pipeline that:

Predicts the correct answer to a given logic problem with high accuracy.

Provides a clear, step-by-step "reasoning trace" to explain how the answer was reached.

Delivers a fully compliant submission package, including the prediction file, a detailed technical report, and this well-documented code repository.

### Our Solution
To achieve our goal, we implemented a two-part system documented in the ethos.ipynb notebook:

The Prediction Engine: We fine-tuned a bert-base-uncased transformer model for a multi-class classification task. By concatenating the problem statement with all five answer options into a single input, we enabled the model to learn the deep contextual relationships between a problem and its potential solutions. This engine is responsible for generating the correct option predictions for the entire test set.

The Reasoning Engine: Recognizing the difficulty of fully automating high-quality reasoning, we adopted a pragmatic and effective hybrid strategy. For a significant subset of ~40 problems, we manually generated detailed Chain-of-Thought (CoT) solutions to serve as a gold standard for explainability. For the remainder of the dataset, we inserted a professional placeholder, indicating that the prediction was made by the classification model.

This project successfully demonstrates a complete workflow for building a hybrid reasoning system. The final output is a final_submission.csv file that fulfills all requirements of the challenge, showcasing both a powerful predictive model and a clear methodology for generating high-quality reasoning traces.
This project utilizes data analysis and machine learning techniques within Jupyter Notebooks to address the hackathon's theme.

##  Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

You need to have Python and Jupyter Notebook installed on your system. You can install the required libraries using pip:

```sh
pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```

### Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/SMFawaz24/ethos-hackathon.git
   ```
2. Navigate to the project directory:
   ```sh
   cd ethos-hackathon
   ```

##  Usage

1. Start the Jupyter Notebook server:
   ```sh
   jupyter notebook
   ```
2. Open the main notebook file (`.ipynb`) from the Jupyter interface in your browser to see the code, analysis, and results.


##  Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

##  License

Distributed under the MIT License. See `LICENSE` for more information.


##  Acknowledgments

*   Ethos Hackathon Organizers
*   Any third-party libraries or resources used
*   README template inspiration
