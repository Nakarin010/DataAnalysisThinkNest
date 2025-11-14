# ThinkNest Cinema Data Analysis ⚡

> This group project is part of the Special Topics in Databases class. I focused on cleaning and preparing cinema ticket sales data for visualization in PowerBI.

---

## 📋 Project Overview

This project analyzes cinema ticket sales data from Thailand's theatre industry, focusing on data quality improvement and preparation for business intelligence tools.

**Dataset Source:** [Cinema Ticket Sales on Kaggle](https://www.kaggle.com/datasets/arashnic/cinema-ticket)

**Data Coverage:**
- **Time Period:** 8 months in 2018 (February to November)
- **Records:** 142,524 rows
- **Variables:** 14 columns
- **Data Quality Issues:** ~125 missing values in occupancy percentage and capacity columns

---

## 🎯 Project Goals

1. **Data Cleaning:** Address missing values and data quality issues
2. **Data Modeling:** Restructure the data to align with Thailand theatre industry context
3. **Data Preparation:** Prepare clean datasets for PowerBI visualization

---

## 🔄 Data Transformation Approach

### Main Table Modifications

The original dataset contained highly correlated variables that could be calculated from each other:

- **occupancy_rate (occu_perc)** can be calculated from capacity fields
- **total_sales** can be derived from: `tickets_sold - tickets_out` (tickets sold minus cancelled tickets)

### Enhanced Data Model

I modified the main table and added **2 reference tables** to better align with realistic Thailand Theatre Industry operations:

<img width="623" height="491" alt="Data Model Diagram" src="https://github.com/user-attachments/assets/379a3751-eb27-4a0a-92f3-23373a30d483" />

This restructuring:
- Reduces redundancy and correlation between fields
- Provides better context for Thailand's cinema industry
- Improves data normalization for analysis

---

## 📂 Repository Structure

```
DataAnalysisThinkNest/
├── README.md                    # Project documentation
├── .gitignore                   # Git ignore rules
├── data/
│   ├── raw/                     # Original datasets (not tracked in git)
│   └── processed/               # Cleaned datasets (not tracked in git)
├── workflows/
│   └── ThinkNest_Alteryx.yxmd  # Alteryx data cleaning workflow
├── docs/
│   └── ThinkNest-AI Usage Statement.pdf  # AI usage disclosure
└── reports/
    └── ThinkNest_Report.pdf    # Final project report and analysis
```

---

## 🛠️ How to Use This Project

### Prerequisites

- **Alteryx Designer** (2025.1 or compatible version)
- **Dataset:** Download from [Kaggle](https://www.kaggle.com/datasets/arashnic/cinema-ticket)

### Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Nakarin010/DataAnalysisThinkNest.git
   cd DataAnalysisThinkNest
   ```

2. **Download the dataset:**
   - Visit the [Kaggle dataset page](https://www.kaggle.com/datasets/arashnic/cinema-ticket)
   - Download the CSV files
   - Place them in the `data/raw/` folder

3. **Open the Alteryx workflow:**
   - Open `workflows/ThinkNest_Alteryx.yxmd` in Alteryx Designer
   - Update the input file paths to point to your `data/raw/` folder
   - Run the workflow to clean and process the data

4. **Review the results:**
   - Check the processed data output
   - Review the cleaning steps and transformations applied

---

## 📊 Dataset Fields

The main dataset includes:

- `film_code` - Unique identifier for each film
- `cinema_code` - Cinema location identifier
- `total_sales` - Total revenue from ticket sales
- `tickets_sold` - Number of tickets sold
- `tickets_out` - Number of tickets cancelled/refunded
- `show_time` - Movie screening time
- `occu_perc` - Occupancy percentage
- `ticket_price` - Price per ticket
- `ticket_use` - Number of tickets used
- `capacity` - Theatre capacity
- `date` - Transaction date
- `month` - Month of transaction
- `quarter` - Quarter of the year
- `day` - Day of the week

---

## 📄 Documentation Files

- **`docs/ThinkNest-AI Usage Statement.pdf`** - Disclosure of AI tools used during the project
- **`reports/ThinkNest_Report.pdf`** - Comprehensive 8-page analysis report with findings and visualizations

---

## 💡 Key Learnings

> One of many things I learned from this project is that there are many ways to approach data cleaning and analysis. The best approach really depends on your research question and thesis idea! ⚡

The data transformation process taught me:
- How to identify and handle redundant calculated fields
- The importance of contextualizing data for specific industries
- Strategies for addressing missing values in key metrics
- Data modeling techniques for improved analysis

---

## 🙏 Acknowledgments

- Dataset provided by [Arash Nic on Kaggle](https://www.kaggle.com/datasets/arashnic/cinema-ticket)
- Created for Special Topics in Databases class
- Tools used: Alteryx Designer, PowerBI

---

## 📧 Contact

For questions or collaboration opportunities, please open an issue in this repository.
