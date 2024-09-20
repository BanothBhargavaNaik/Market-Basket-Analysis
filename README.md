# Market Basket Analysis with Association Rules

## Project Overview

This project implements Market Basket Analysis (MBA) using association rules to discover relationships between items purchased together in retail transactions. The goal is to identify patterns that can inform marketing strategies, inventory management, and product placement.


## Introduction

Market Basket Analysis is a data mining technique used by retailers to understand the purchase behavior of customers. By analyzing transaction data, we can uncover association rules that suggest how likely it is that the purchase of one item will lead to the purchase of another.

## Data Description

The dataset used in this project consists of transaction records from a retail store. Each transaction includes a list of items purchased together. Key columns include:

- **Items**: List of items purchased in the transaction.

## Methodology

1. **Data Preprocessing**: 
   - Load and clean the dataset.
   - Transform the data into a suitable format for analysis.

2. **Applying Association Rule Mining**: 
   - Use the Apriori algorithm to identify frequent itemsets.
   - Generate association rules from these itemsets.

. **Evaluating Rules**: 
   - Calculate key metrics: support, confidence, lift, leverage, conviction, and Zhang's metrics.
   - Filter and sort rules based on these metrics to identify the most significant associations.

## Results

- The project identified 78 association rules, with key findings including:
  - A typical rule has a lift of 1.76.
  - Rules involving popular items, such as whole milk, should be interpreted cautiously.

### Key Metrics

- **Lift**: Indicates the strength of the association.
- **Leverage**: A normalized measure of lift.
- **Conviction**: Measures the dependence of the consequent on the antecedent.
- **Zhang's Metrics**: Additional metrics that can help in understanding the significance of the rules, such as:
  - **Improvement**: Measures how much the probability of the consequent increases when the antecedent is known.
  - **Confidence**: Reflects the likelihood of the consequent occurring given the antecedent.

## Zhang's Metrics

Zhang's metrics provide a deeper insight into the quality of the association rules. Key metrics include:

- **Improvement**: 
  \[
  \text{Improvement}(A \rightarrow B) = \text{Confidence}(A \rightarrow B) - \text{Support}(B)
  \]
  This metric shows how much more likely the consequent is when the antecedent is present compared to its overall occurrence.

- **Zhang's Lift**:
  \[
  \text{Zhang's Lift}(A \rightarrow B) = \text{Lift}(A \rightarrow B) - 1
  \]
  This metric helps understand the effectiveness of the rule by comparing it to a baseline of independence.

## Conclusion

The analysis successfully uncovered meaningful associations between products, providing insights that can be leveraged for marketing and inventory management. Future work could explore more advanced techniques or larger datasets to enhance the findings.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib / Seaborn (for visualization)
- Jupyter Notebook

## How to Run the Project

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/market-basket-analysis.git

2. Navigate to the project directory:
   cd market-basket-analysis

3. Install the required libraries:
    pip install -r requirements.txt
    
4. Run the Jupyter Notebook: