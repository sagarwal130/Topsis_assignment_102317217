# TOPSIS Implementation in Python

This project implements the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method using Python.

## 📌 Features
- Command line program
- Handles incorrect parameters
- Handles file not found
- Validates numeric columns
- Validates weights and impacts
- Generates ranked output CSV

## 📂 Usage

python topsis.py <InputDataFile> <Weights> <Impacts> <OutputFileName>

Example:

python topsis.py data.csv "1,1,1,1,1" "+,+,+,+,+" output.csv

## 📊 Input Requirements

- Input file must contain 3 or more columns
- First column = Alternatives
- Remaining columns = Numeric criteria
- Number of weights must equal number of criteria
- Impacts must be '+' or '-'
- Weights and impacts must be comma separated

## 🧮 Method Used

1. Normalize decision matrix
2. Multiply by weights
3. Determine ideal best and worst
4. Calculate distance from ideal solutions
5. Compute performance score
6. Rank alternatives
