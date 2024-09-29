# Self-Organizing Map (SOM) for Book Dataset

This project implements a Self-Organizing Map (SOM) to cluster and visualize a book dataset based on numerical features such as rating, number of ratings, and number of reviews. The SOM helps to map and organize similar books onto a grid based on their feature similarity.

## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Dataset](#dataset)
- [Installation](#installation)
- [Running the Project](#running-the-project)
- [Explanation of the Code](#explanation-of-the-code)
- [Output](#output)
- [References](#references)

## Introduction

Self-Organizing Maps are a type of unsupervised neural network used for dimensionality reduction and clustering. This project applies SOM to a dataset of books, where the SOM organizes books based on their ratings, number of ratings, and number of reviews.

The goal of this assignment is to:
- Understand how SOMs work.
- Preprocess and normalize the book dataset.
- Train a SOM using the `MiniSom` Python library.
- Visualize the trained SOM with an enhanced output grid.

## Prerequisites

- Python 3.x
- Jupyter Notebook or Google Colab
- The following Python libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `minisom`
  - `scikit-learn`

To install the necessary dependencies, run:

```bash
pip install pandas numpy matplotlib scikit-learn minisom
```

## Dataset

The dataset used in this project is a CSV file named `book_details.csv`, which contains the following columns:

- `title`: The title of the book.
- `author`: The author of the book.
- `rating`: Average rating of the book.
- `no_of_ratings`: Total number of ratings for the book.
- `no_of_reviews`: Total number of reviews for the book.
- `description`: A brief description of the book.
- `genres`: Genres the book belongs to.

Only the numerical columns (`rating`, `no_of_ratings`, `no_of_reviews`) are used for SOM training.

## Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/som-book-dataset.git
```

2. Change to the project directory:

```bash
cd som-book-dataset
```

3. Install the required dependencies:

```bash
pip install -r requirements.txt
```

(You can create a `requirements.txt` file by listing the libraries and their versions if necessary.)

## Running the Project

1. **Load the Dataset**: Ensure the `book_details.csv` file is located in the project directory or the correct path is provided in the script.

2. **Run the SOM Training**: Open and run the Python script `som_book_clustering.py` in a Python environment (Jupyter Notebook or Google Colab).

3. **Results**: The SOM will output a grid where similar books (based on numerical features) are organized into clusters. Each book is represented by its index, and the U-Matrix (distance map) is displayed with a color-coded heatmap.

### Example Command to Run the Script:
```bash
python som_book_clustering.py
```

## Explanation of the Code

- **Step 1: Loading the Dataset**:
  The dataset is loaded from a CSV file and specific numerical columns are selected for SOM training.
  
- **Step 2: Data Cleaning and Preprocessing**:
  The dataset is cleaned by removing commas and special characters in the numerical columns. Missing values are handled by dropping rows with NaNs.
  
- **Step 3: Normalization**:
  The numerical data is scaled to a range between 0 and 1 using `MinMaxScaler` from `scikit-learn`.
  
- **Step 4: SOM Initialization and Training**:
  A 10x10 SOM grid is initialized, and training is performed for 1000 iterations. A random seed is set for reproducibility.
  
- **Step 5: Visualization**:
  The trained SOM is visualized using a U-Matrix (distance map), and the data points are labeled on the grid. Similar books are clustered together on the map.

## Output

- **Self-Organizing Map (SOM) Grid**:
  The output will display a grid where each book is plotted based on its similarity to others in terms of ratings, number of reviews, and number of ratings.
  
- **Distance Map (U-Matrix)**:
  A heatmap is generated showing the distances between neighboring neurons. Areas with lower distances indicate similar clusters of books.

### Sample Visualization:
(Sample output image here)

- Each red index on the grid represents a book.
- The background colors represent distances between neurons, with a color bar to indicate distance values.

## References

- [MiniSom Documentation](https://github.com/JustGlowing/minisom)
- [Self-Organizing Maps - An Overview](https://en.wikipedia.org/wiki/Self-organizing_map)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

### Optional Enhancements:
- Include a sample output image in the "Output" section.
- Add a `requirements.txt` file in the repository with necessary dependencies like this:

```
pandas==1.3.3
numpy==1.21.2
matplotlib==3.4.3
scikit-learn==0.24.2
minisom==2.2.9
```

This should give a complete and professional README for your college assignment!
