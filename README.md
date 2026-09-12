# Netflix Data Exploration and Visualisation

## 📌 Project Overview

Netflix is one of the world's leading streaming platforms, with a large catalogue of movies and TV shows across multiple countries and genres.

This project performs **Exploratory Data Analysis (EDA), Data Cleaning, and Data Visualisation** on the Netflix titles dataset to identify patterns in Netflix's content library and generate business insights that can support content-production and international-growth decisions.

The analysis focuses on answering:

* What type of content does Netflix offer?
* Which countries contribute the most content?
* Which genres are most common?
* How has Netflix's content catalogue changed over time?
* When does Netflix add the most content?
* Which markets could offer opportunities for growth?
* What content strategy could Netflix consider based on the available data?

---

# 🎯 Business Problem

Netflix wants to use its existing content data to make better decisions about:

1. **Which types of movies and TV shows should be produced?**
2. **Which countries and markets should receive greater content investment?**

The objective is to explore the data, identify meaningful patterns, and convert those patterns into **simple, actionable business recommendations**.

---

# 📂 Dataset
<a href="https://github.com/rajakulathilak/Netflix_Data_Analysis/blob/main/Netflix%20%281%29.csv">Netflix Dataset</a>
The dataset contains information about movies and TV shows available on Netflix.

### Important Features

| Feature        | Description                                 |
| -------------- | ------------------------------------------- |
| `show_id`      | Unique identifier for each title            |
| `type`         | Movie or TV Show                            |
| `title`        | Name of the movie or TV show                |
| `director`     | Director of the title                       |
| `cast`         | Cast members                                |
| `country`      | Country/countries associated with the title |
| `date_added`   | Date the title was added to Netflix         |
| `release_year` | Original release year                       |
| `rating`       | Content rating                              |
| `duration`     | Movie duration or number of seasons         |
| `listed_in`    | Genres/categories                           |
| `description`  | Description of the title                    |

---

# 🛠️ Tools & Technologies

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Google Colab**

---

# 🔍 Analysis Workflow

## 1. Data Exploration

The dataset was initially explored to understand its overall structure and quality.

The analysis included:

* Dataset shape
* Number of rows and columns
* Data types
* Duplicate records
* Numerical and categorical variables
* Summary statistics
* Unique values
* Value counts
* Potential outliers
* Missing values

This provided an initial understanding of the dataset before performing detailed analysis.

---

## 2. Summary Statistics & Feature Analysis

Numerical and categorical columns were separated and analysed independently.

### Numerical Analysis

Descriptive statistics were used to understand numerical variables such as:

* Release year
* Movie duration
* Other numerical features

### Categorical Analysis

Categorical variables were analysed using:

* Number of unique values
* Frequency distributions
* Value counts

This helped identify dominant categories and unusual values.

---

# 🧹 Data Cleaning & Preparation

## 3. Missing Value Analysis

Missing values were analysed across the dataset to determine:

* Which columns contain missing information
* The extent of missing data
* Which missing values could be reasonably filled
* Which records should be removed

Appropriate treatment was applied based on the importance and nature of each column.

---

## 4. Date Transformation

The `date_added` column was converted into a proper datetime format.

Additional features were extracted:

* `year_added`
* `month_added`

These features were then used to analyse Netflix's content-addition patterns over time.

---

## 5. Handling Missing Values

Missing values were handled based on the characteristics of individual columns.

* Text-based columns were filled where appropriate.
* Records missing critical information were removed where necessary.
* The cleaned dataset was then used for further analysis.

---

# 🔄 Data Transformation

## 6. Unnesting Multi-Value Columns

Several columns contain multiple values within a single record, including:

* `country`
* `cast`
* `listed_in` / genres

These columns were transformed by:

1. Splitting multiple values using `, `
2. Applying `explode()`
3. Creating separate rows for individual countries, actors and genres

This made it possible to perform more accurate frequency and country/genre-level analysis.

---

# 📊 Exploratory Data Analysis

## 7. Top 10 Countries

The unnested `country` data was analysed using value counts to identify the countries contributing the most titles to Netflix's catalogue.

**Business purpose:** Understand Netflix's strongest content-producing markets and identify potential geographic opportunities.

---

## 8. Top 10 Genres

The genre data was analysed to identify the most frequently represented genres on Netflix.

**Business purpose:** Understand the types of content that dominate Netflix's catalogue and identify potential areas for content investment.

---

## 9. Movies vs TV Shows

The distribution of Movies and TV Shows was analysed using count plots.

**Observation:** The analysis shows the relative importance of Movies and TV Shows within Netflix's overall catalogue.

---

## 10. Content Added Per Year

The `year_added` feature was analysed to understand how Netflix's content additions changed over time.

This helps identify periods of:

* Higher content additions
* Lower content additions
* Changes in Netflix's content strategy

---

## 11. Distribution Analysis

Different visualisation techniques were used to understand the distribution of important variables, including:

* Box plots
* Histograms
* Bar charts
* Pie charts
* Count plots

Each visualisation was accompanied by an observation highlighting the most important pattern.

---

# 📈 Key Analysis Areas

The project analyses:

### Content

* Movies vs TV Shows
* Popular genres
* Content ratings
* Movie duration
* TV-show seasons

### Geography

* Top countries
* Country-level content distribution
* Country and genre relationships

### Time

* Content additions by year
* Content additions by month
* Growth patterns in Netflix's catalogue

---

# 💡 Business Insights

The analysis was used to identify patterns that can support Netflix's content and expansion strategy.

### Insight 1 — Content Strategy

The distribution of Movies and TV Shows provides an indication of Netflix's overall content mix and can help guide future investment between the two formats.

### Insight 2 — Genre Strategy

The top genres reveal the categories that dominate Netflix's catalogue. This can help Netflix identify genres where it already has strong representation as well as potential gaps that could be explored.

### Insight 3 — Geographic Expansion

Country-level analysis highlights the markets that contribute significantly to Netflix's content catalogue. Comparing country representation can help identify markets where additional local content investment may provide growth opportunities.

> **The exact numerical findings are available in the project notebook and visualisations.**

---

# 🎯 Business Recommendations

Based on the analysis, Netflix can consider three simple strategies:

### 1. Invest in Strong and Emerging Genres

Continue investing in genres with strong representation while identifying underserved genres that could attract new audiences.

### 2. Increase Local Content

Use country-level data to identify markets where Netflix can increase investment in local-language movies and TV shows.

Local content can help Netflix attract subscribers, improve engagement and compete with regional streaming platforms.

### 3. Build Country-Specific Content Strategies

Instead of applying one global content strategy, Netflix can use country and genre-level data to determine which types of content should be prioritised in different markets.

---

# 📁 Project Structure

```text
Netflix-Data-Exploration-and-Visualisation/
│
├── notebook (1).ipynb
├── Netflix (1).csv
├── README.md
└── images/
    └── visualisations/
```

---

# 🚀 How to Run the Project

### Clone the repository

```bash
git clone <https://github.com/rajakulathilak/Netflix_Data_Analysis/tree/main>
```

### Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn
```

Open the notebook:


<a href="https://github.com/rajakulathilak/Netflix_Data_Analysis/blob/main/notebook%20(1).ipynb">Netflix_python_code</a>

Run the cells sequentially to reproduce the analysis.

---

# 📌 Skills Demonstrated

This project demonstrates practical experience in:

* Data Exploration
* Data Cleaning
* Data Wrangling
* Missing Value Treatment
* Duplicate Detection
* Outlier Analysis
* Datetime Transformation
* Feature Engineering
* Handling Multi-Value Columns
* `groupby()`
* `value_counts()`
* `explode()`
* Exploratory Data Analysis
* Data Visualisation
* Business Insight Generation
* Business Recommendations

### Python Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn

---

# 📊 Project Outcome

This project demonstrates how raw Netflix content data can be transformed into **business insights through Python-based exploratory data analysis and visualisation**.

The analysis helps understand Netflix's content mix, genre trends, geographic distribution and content-addition patterns, providing a foundation for making data-driven decisions around **content production and international market growth**.

---

## 👤 Author

**Raja Kula Thilak**

Aspiring Data Analyst | Python | SQL | Excel | Tableau | Data Analytics

---

⭐ If you found this project useful, feel free to explore the repository and the analysis notebook.
