# Link Prediction with NASA GES-DISC Dataset

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![License][license-shield]][license-url]

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <!-- Removed the logo as per your request -->
  
  <h3 align="center">NASA GES-DISC Link Prediction</h3>

  <p align="center">
    Implementing Link Prediction Methods on the NASA GES-DISC Knowledge Graph Dataset
    <br />
    <a href="https://github.com/ryan0980/NASA-GES-DISC-Dataset-Prediction"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/ryan0980/NASA-GES-DISC-Dataset-Prediction">View Demo</a>
    ·
    <a href="https://github.com/ryan0980/NASA-GES-DISC-Dataset-Prediction/issues">Report Bug</a>
    ·
    <a href="https://github.com/ryan0980/NASA-GES-DISC-Dataset-Prediction/issues">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#dataset">Dataset</a></li>
        <li><a href="#approaches">Approaches</a></li>
        <li><a href="#results">Results</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#how-to-run">How to Run</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#evaluation-metrics">Evaluation Metrics</a></li>
    <li><a href="#conclusion">Conclusion</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#license">License</a></li>
  </ol>
</details>

## About The Project

<!-- Removed the logo as per your request -->

This project is part of the **CSCI 6365 Advanced Machine Learning** coursework. It involves implementing and comparing two link prediction methods on the NASA GES-DISC knowledge graph dataset.

### Dataset

The **NASA GES-DISC knowledge graph** consists of:

- **Nodes:** Entities such as Datasets, Data Centers, Projects, Platforms, Instruments, Publications, and Science Keywords.
- **Edges:** Relationships between these entities, like "uses", "contains", "published_by", etc.

Dataset files include:

- `nodes.csv`: Node information with attributes.
- `train_edges.csv`: Edges used for training.
- `val_links.csv`: Edges used for validation.
- `test_links.csv`: Edges used for testing.

### Approaches

#### Method 1: Embedding-Based Approach Using Node2Vec

- **Generate node embeddings** using **Node2Vec**.
- **Create positive and negative samples** for link prediction.
- **Train a Logistic Regression model** using concatenated node embeddings.
- **Evaluate** using AUC, F1 Score, and Accuracy.

#### Method 2: Alternative Approach Using Singular Value Decomposition (SVD)

- **Construct the adjacency matrix** of the graph.
- **Apply SVD** to obtain low-dimensional node representations.
- **Predict links** by computing the dot product of node embeddings.
- **Evaluate** using AUC, F1 Score, and Accuracy.

### Results

| **Method**                      | **AUC**  | **F1 Score** | **Accuracy** |
|---------------------------------|----------|--------------|--------------|
| **Node2Vec + Logistic Regression** | 0.9694   | 0.9328       | 92.86%       |
| **SVD-Based Approach**          | 0.5950   | 0.5241       | 43.26%       |

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

- **Python 3.7+**
- **pip** package manager

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/ryan0980/NASA-GES-DISC-Dataset-Prediction.git
   cd NASA-GES-DISC-Dataset-Prediction
   ```

2. **Install required dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Download the dataset:**

   - Download the dataset from [Zenodo](https://zenodo.org/record/11492533) and place the files in the `data/` directory.

### How to Run

1. **Run the Jupyter Notebook:**

   - Open and execute the `Link_Prediction_NASA_GES_DISC.ipynb` notebook to reproduce the results.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Usage

Use this project to:

- Understand how to implement link prediction methods on real-world graph data.
- Learn how to use Node2Vec for generating node embeddings.
- Compare different approaches for link prediction tasks.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Evaluation Metrics

- **AUC (Area Under the ROC Curve):** Measures the ability to distinguish between positive and negative links.
- **F1 Score:** Harmonic mean of precision and recall.
- **Accuracy:** Proportion of correct predictions.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Conclusion

- **Performance Comparison:**
  - The embedding-based approach significantly outperformed the SVD-based method.
  - Incorporating node attributes and more advanced models could further improve results.

- **Future Work:**
  - Explore heuristic-based methods or graph neural networks for link prediction.
  - Integrate node properties into embeddings.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Acknowledgments

- **Instructor:** Prof. Sardar Hamidian, CSCI 6365 Advanced Machine Learning, The George Washington University
- **Instructor:** Prof. Armin Mehrabian, CSCI 6365 Advanced Machine Learning, The George Washington University

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Contact

Shi Qiu - [LinkedIn](https://www.linkedin.com/in/shi1qiu) - [shiqiu@example.com](mailto:tusrau@gmail.com)

Project Link: [https://github.com/ryan0980/NASA-GES-DISC-Dataset-Prediction](https://github.com/ryan0980/NASA-GES-DISC-Dataset-Prediction)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## License

This project is licensed under the **Do What The F*ck You Want To Public License** (WTFPL). See the [`LICENSE`](https://github.com/ryan0980/NASA-GES-DISC-Dataset-Prediction/blob/main/LICENSE) file for more details.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/ryan0980/NASA-GES-DISC-Dataset-Prediction.svg?style=for-the-badge
[contributors-url]: https://github.com/ryan0980/NASA-GES-DISC-Dataset-Prediction/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/ryan0980/NASA-GES-DISC-Dataset-Prediction.svg?style=for-the-badge
[forks-url]: https://github.com/ryan0980/NASA-GES-DISC-Dataset-Prediction/network/members
[stars-shield]: https://img.shields.io/github/stars/ryan0980/NASA-GES-DISC-Dataset-Prediction.svg?style=for-the-badge
[stars-url]: https://github.com/ryan0980/NASA-GES-DISC-Dataset-Prediction/stargazers
[issues-shield]: https://img.shields.io/github/issues/ryan0980/NASA-GES-DISC-Dataset-Prediction.svg?style=for-the-badge
[issues-url]: https://github.com/ryan0980/NASA-GES-DISC-Dataset-Prediction/issues
[license-shield]: https://img.shields.io/badge/License-WTFPL-brightgreen.svg?style=for-the-badge
[license-url]: http://www.wtfpl.net/about/

