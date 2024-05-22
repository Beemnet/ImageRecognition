# MNIST Java Project

This project involves working with the MNIST dataset, which consists of handwritten digits, and performing various tasks including reading data, reshaping it, and performing basic statistical learning.

## Table of Contents

1. [Project Structure](#project-structure)
2. [Requirements](#requirements)
3. [Usage](#usage)
4. [Tasks Overview](#tasks-overview)
   - [Part A: Reading Data from CSV](#part-a-reading-data-from-csv)
   - [Part B: Reshaping Data](#part-b-reshaping-data)
   - [Part C: Refactoring Code](#part-c-refactoring-code)
   - [Part D: Analyzing the Distribution of the Dataset](#part-d-analyzing-the-distribution-of-the-dataset)
   - [Part E: Calculating the Average Representant](#part-e-calculating-the-average-representant)
   - [Part F: Performing the First Classification](#part-f-performing-the-first-classification)

## Project Structure

```plaintext
.
├── src
│   ├── main
│   │   ├── java
│   │   │   ├── Image.java
│   │   │   ├── ImageCsvDAO.java
│   ├── test
│   │   ├── java
│   │   │   ├── TestA.java
│   │   │   ├── TestB.java
│   │   │   ├── TestC.java
│   │   │   ├── TestD.java
│   │   │   ├── TestE.java
│   │   │   ├── TestF.java
├── mnist_train.csv
├── mnist_test.csv
└── README.md
```

## Requirements

- Java Development Kit (JDK)
- Integrated Development Environment (IDE) such as IntelliJ IDEA or Eclipse
- [mnist_train.csv](mnist_train.csv) and [mnist_test.csv](mnist_test.csv) files are provided under the `/data` folder

## Usage

1. Clone the repository and open it in your IDE.
2. Run the test classes to see the implementation in action.

## Tasks Overview

### Part A: Reading Data from CSV

1. **Extract raw data:**

   - Created a program to read all lines from the `mnist_train.csv` and `mnist_test.csv` files.
   - Converted each line into an array of `String` using the `split` function.
   - Converted the array of `String` into an array of `double`, excluding the header line.

2. **Test Class:**
   - `TestA` should demonstrate reading and processing the CSV files.

### Part B: Reshaping Data

1. **Transform data:**

   - Added logic to transform the array of `double` (from the 784 columns) into a 2D square matrix (28x28).
   - Implemented a `showMatrix` method to print the matrix in the console using `xx` for values above 100 and `..` for others.
   - Used this method on the matrix extracted and print the first column.

2. **Test Class:**
   - `TestB` demonstrates reshaping and displaying the matrix.

### Part C: Refactoring Code

1. **Refactor into classes:**

   - Created an `Image` class with fields `label` and `dataMatrix`.
   - Created an `ImageCsvDAO` class with a method `getAllImages()` to read data from CSV files.

2. **Test Class:**
   - `TestC` demonstrates the functionality of the refactored classes.

### Part D: Analyzing the Distribution of the Dataset

1. **Calculate distribution:**

   - Implemented a `calculateDistribution` method to count occurrences of each digit in the dataset.

2. **Test Class:**
   - `TestD` demonstrates the distribution calculation.

### Part E: Calculating the Average Representant

1. **Train centroids:**

   - Implemented a `trainCentroids` method to compute the average matrix (centroid) for each digit from the `mnist_train.csv`.

2. **Test Class:**
   - `TestE` demonstrates centroid calculation.

### Part F: Performing the First Classification

1. **Classify images:**

   - Loaded `mnist_test.csv` as a list of `Image` instances.
   - Isolate the first 10 occurrences of the digit "0".
   - Calculate the distance between these instances and each centroid to classify the images.

2. **Test Class:**
   - `TestF` demonstrates image classification.

## Installation

This project requires the following dependencies:

1. [JUnit](https://junit.org/junit5/) - for unit testing
2. [OpenCSV](https://opencsv.sourceforge.net/) - for reading/writing CSV files

To use this project, please follow these steps:

1. Download the latest versions of the JUnit and OpenCSV JAR files from their respective websites.
2. Add the downloaded JAR files to your project's library or classpath.
3. You should now be able to use the functionalities provided by these libraries in your code.

## Conclusion

This project provides a hands-on approach to working with the MNIST dataset using Java, covering data extraction, transformation, and basic classification techniques. The tasks are structured to build upon each other, ensuring a comprehensive understanding of handling and analyzing large datasets in Java.

## This project uses guidelines provided by Thomas BROUSSARD from EPITA.
