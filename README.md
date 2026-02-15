# TOPSIS Implementation in Python

This project implements the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method using Python.

---

## 📌 Features
- Command line program
- Handles incorrect parameters
- Handles file not found
- Validates numeric columns
- Validates weights and impacts
- Generates ranked output CSV

---

## 📂 Usage

```bash
python topsis.py <InputDataFile> <Weights> <Impacts> <OutputFileName>
```

### Example:

```bash
python topsis.py data.csv "1,1,1,1,1" "+,+,+,+,+" output.csv
```

---

## 📊 Input Requirements

- Input file must contain **3 or more columns**
- First column = Alternatives
- Remaining columns = Numeric criteria
- Number of weights must equal number of criteria
- Impacts must be `'+'` or `'-'`
- Weights and impacts must be comma separated

---

## 🧮 Method Used

1. Normalize decision matrix  
2. Multiply by weights  
3. Determine ideal best and worst  
4. Calculate distance from ideal solutions  
5. Compute performance score  
6. Rank alternatives  

---

## 📈 Result (Generated Output)

Below is the actual result generated in the output file:

| Fund Name | P1  | P2  | P3 | P4  | P5   | Topsis Score | Rank |
|------------|-----|-----|----|-----|------|---------------|------|
| M1 | 0.84 | 0.71 | 6.7 | 42.1 | 12.59 | 0.56369233  | 3 |
| M2 | 0.91 | 0.83 | 7   | 31.7 | 10.11 | 0.513032103 | 4 |
| M3 | 0.79 | 0.62 | 4.8 | 46.7 | 13.23 | 0.439177283 | 6 |
| M4 | 0.78 | 0.61 | 6.4 | 42.4 | 12.55 | 0.491956082 | 5 |
| M5 | 0.94 | 0.88 | 3.6 | 62.2 | 16.91 | 0.641885815 | 2 |
| M6 | 0.88 | 0.77 | 6.5 | 51.5 | 14.91 | 0.738148132 | 1 |
| M7 | 0.66 | 0.44 | 5.3 | 48.9 | 13.83 | 0.407389532 | 8 |
| M8 | 0.93 | 0.86 | 3.4 | 37.0 | 10.55 | 0.408498677 | 7 |

> 🏆 **Best Alternative:** M6 (Rank 1) with the highest TOPSIS score of **0.738148132**

---

## 📁 Project Structure

```
Topsis assignment/
│── topsis.py
│── README.md
```

---

## ✅ Output

After successful execution, the program displays:

```
Result saved successfully
```

The ranked result is stored in the specified output CSV file.

---

⭐ This project demonstrates practical implementation of Multi-Criteria Decision Making (MCDM) using the TOPSIS method in Python.
