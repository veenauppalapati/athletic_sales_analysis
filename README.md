# athletic_sales_analysis
This project is part of my Week 5 - Module 5 Challenge for the Rutgers AI Bootcamp. The objective is to combine data from two CSV files, `athletic_sales_2020.csv` and `athletic_sales_2021.csv`, and perform data grouping, slicing, and analysis using pandas to extract insights from the combined dataset.


## Table of Contents
- [Project Structure](#project-structure)
- [Project Breakdown](#project-breakdown)
- [Pandas Commands](#pandas-commands)
- [Installation](#installation)

---

## Project Structure

```bash
athletic_sales_analysis
|__ Resources
|   |__ athletic_sales_2020.csv
|   |__ athletic_sales_2021.csv
|__ README.md
|__ athletic_sales_analysis.ipynb
```
---

## Project Breakdown: 

- **Part 1**: Combine and Clean the Data

- **Part 2**: Determine which region sold the most products

- **Part 3**: Determine which `region` had the most sales

- **Part 4**: Determine which `retailer` had the most sales

- **Part 5**: Determine which **retailer** sold the most Women’s Athletic Footwear

- **Part 6**: Determine the day with the most women’s athletic footwear sales

- **Part 7**: Determine the week with the most women’s athletic footwear sales


---

## Pandas Commands

The following Pandas commands were explored during this challenge:

**Analyzing**
```py
df.sort_values(by='column_name', ascending=True)
```

**Reading**
```py
df = pd.read_csv('data.csv')
```

**Transforming**
```py
df.rename(columns={'old_name': 'new_name'})
```

```py
df['date_column'] = pd.to_datetime(df['date_column'])
```

**Combining**
```py
combined_df = pd.concat([df1, df2]).reset_index(drop=True)
```

**Grouping**

```py
grouped_df = df.groupby('category').sum()
```

```py
pivot_table = pd.pivot_table(
                                df, 
                                values='sales', 
                                index='product', 
                                columns='region', 
                                aggfunc='sum'
                            )
```


**Filtering**
```py
filtered_df = df.loc[df['column'] == 'value']
```

```py
resampled_df = df.resample('D').sum()
```

**Other commands explored:**

- `.loc[]` – Access a group of rows and columns by labels or a boolean array.

- `.info()` – Print a concise summary of the DataFrame.

- `.head()` – Return the first few rows of the DataFrame.

- `pd.read_csv()` – Read a CSV file into a DataFrame.

- `pd.DataFrame()` – Create a DataFrame from an array, dictionary, or series.

- `.columns` – Access or set the column labels of the DataFrame.

- `.sort_values()` – Sort the DataFrame by one or more columns, either in ascending or descending order.

---

## Installation

To run this project, ensure you have python installed (version 3.8 or higher).  Follow these steps:

1.  Clone the repository:

```bash
    git clone https://github.com/veenauppalapati/athletic_sales_analysis
```

2.  Navigate to the project directory: 

```bash
    cd athletic_sales_analysis
```

3. Open the project folder in visual studio code

```bash
    code .
```
4. Run the code in the `athletic_sales_analysis.ipynb` notebook to explore and analyze the dataset.