<<<<<<< HEAD

# MLP & RBF Neural Networks for Autism Spectrum Disorder (ASD) Screening

> An educational project implementing two neural network models, Multi-Layer Perceptron (MLP) and Radial Basis Function (RBF), to screen for Autism Spectrum Disorder using a real-world clinical dataset.




## Table of Contents
- [About The Project](#about-the-project)
- [Workflow](#workflow)
- [Performance Results](#performance-results)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [How to Reproduce Results](#how-to-reproduce-results)
- [Dataset](#dataset)
- [License](#license)



## About The Project

Early detection of Autism Spectrum Disorder (ASD) can significantly improve a child's quality of life. This project serves as an educational exercise to explore the implementation of two powerful neural network architectures on a real-world classification problem.

We implement and evaluate:
1.  **Multi-Layer Perceptron (MLP):** A classic feedforward neural network.
2.  **Radial Basis Function (RBF) Network:** A network that uses radial basis functions as activation functions.

The goal is to demonstrate the end-to-end workflow, from data preprocessing to model training and evaluation, providing a practical example for learning about these models.

## Workflow
This project follows a two-step process. The user must run the notebooks in sequential order to reproduce the final results.

`01_Data_Preprocessing.ipynb` -> `cleaned_autism_data.csv` -> `02_Neural_Network_Models.ipynb` -> **Final Results**

1.  The first notebook cleans and prepares the raw data.
2.  It saves the processed data as a new CSV file.
3.  The second notebook loads this cleaned data to train and evaluate the neural network models.

## Performance Results

The final performance of each model on the test dataset is summarized below. While the primary goal was implementation and learning, these metrics show how each model performed on this specific dataset.

| Model | Accuracy |
| :--- | :---: |
| **MLP** | **86.67%** |
| **RBF** | **90.0%** |

*For this particular task, the RBF model yielded a higher accuracy score.*

## Getting Started

Follow these instructions to set up and run the project locally.

### Prerequisites

- Python 3.8+
- pip (Python package installer)

### Installation

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/MonaNorouzi/autism-screening-nn.git](https://github.com/MonaNorouzi/autism-screening-nn.git)
    cd autism-screening-nn
    ```

2.  **Create and activate a virtual environment:**
    ```sh
    python -m venv venv
    # On Windows
    .\venv\Scripts\activate
    # On macOS/Linux
    source venv/bin/activate
    ```

3.  **Install the required packages:**
    Make sure your `requirements.txt` file includes `jupyterlab` or `notebook`.
    ```sh
    pip install -r requirements.txt
    ```


## How to Reproduce Results

To get the final results, you must run the two notebooks in order.

**Step 1: Run the Preprocessing Notebook**

-   Open and run all cells in the `01_Data_Preprocessing.ipynb` notebook.
-   This will use the raw dataset and generate a new file named `cleaned_autism_dataf.csv` in the `data/` directory.

**Step 2: Run the Neural Network Notebook**

-   After the cleaned file is created, open and run all cells in the `02_Neural_Network_Models.ipynb` notebook.
-   This notebook will load `cleaned_autism_dataf.csv`, train the MLP and RBF models, and print their performance metrics.



## Dataset

This project utilizes the **"Autism Spectrum Disorder Screening Data for Children"** dataset from the UCI Machine Learning Repository.

- **Source:** [Autistic Spectrum Disorder Screening Data for Children, UCI](https://archive.ics.uci.edu/dataset/419/autistic+spectrum+disorder+screening+data+for+children)


## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

