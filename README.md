# 🎬 Movie Data Analysis with R and Power BI

## 📖 Project Overview
This project demonstrates my proficiency in data cleaning and visualization by analyzing a dataset of Hollywood movies released between 2007 and 2012. The data includes information on movie titles, genres, studios, profitability, and ratings. Using R, I cleaned and preprocessed the dataset to prepare it for analysis. Then, I used Power BI to create an interactive dashboard, highlighting key insights such as ratings, profitability, and production trends.

## 🌐 Data Source
The dataset was sourced from:
[Hollywood's Most Profitable Stories](https://public.tableau.com/app/sample-data/HollywoodsMostProfitableStories.csv).

## 🎯 Objectives
1. 🧹 Utilize R for comprehensive data cleaning and preparation.
2. 📊 Leverage Power BI to create insightful visualizations.
3. 🌟 Showcase skills in transforming raw data into actionable insights.

## 📁 Files in This Repository
- **`assignment 3.R`**: R script for cleaning and initial analysis of the dataset.
- **`clean_df.csv`**: The cleaned dataset ready for analysis and visualization.
- **`Assignment 3.pbix`**: Power BI dashboard with interactive visualizations.

## 🔄 Workflow

### Step 1: Data Cleaning in R
Using R, I ensured the dataset was clean and free of missing values, enabling seamless analysis and visualization. Key steps include:

1. **📥 Loading the Data**:
   ```r
   df <- read.csv("https://public.tableau.com/app/sample-data/HollywoodsMostProfitableStories.csv")
   ```
2. **🗑️ Removing Missing Values**:
   ```r
   library(tidyverse)
   df <- df %>% drop_na()
   ```
3. **📊 Summary Statistics and Visualizations**:
   - Scatterplot to analyze Rotten Tomatoes ratings by studio.
   - Bar chart showing the number of movies produced per year.

4. **📤 Exporting Cleaned Data**:
   ```r
   write.csv(df, "clean_df.csv")
   ```

#### 📝 R Script Highlights:
```r
# Load and clean data
df <- read.csv("https://public.tableau.com/app/sample-data/HollywoodsMostProfitableStories.csv")
library(tidyverse)
df <- df %>% drop_na()

# Visualizations
ggplot(df, aes(x=Lead.Studio, y=Rotten.Tomatoes..)) +
    geom_point() +
    scale_y_continuous(labels = scales::comma) +
    coord_cartesian(ylim = c(0, 110)) +
    theme(axis.text.x = element_text(angle = 90))

write.csv(df, "clean_df.csv")
```

### Step 2: Visualization in Power BI

![image](https://github.com/user-attachments/assets/167cfe32-366b-4137-8f9b-66a27920cbed)


The cleaned dataset was imported into Power BI, where I designed an interactive dashboard. The dashboard includes the following visualizations:
1. **📈 Average Rotten Tomatoes Ratings by Genre**
2. **📆 Number of Movies Produced Per Year**
3. **⭐ Audience Scores for Each Film**
4. **🏢 Profitability Per Studio**
5. **🌍 Worldwide Gross by Genre**

These visualizations provide actionable insights into movie performance and production trends. Brand colors (blue, green, and brown) were used to create a professional and cohesive design.

## 🛠️ How to Use This Repository
1. Clone the repository:
   ```bash
   git clone <repository_url>
   ```
2. Open `assignment 3.R` in RStudio to review the data cleaning process.
3. Import `clean_df.csv` into Power BI to explore the dashboard in `Assignment 3.pbix`.

## 🚀 Skills Demonstrated
- **🧹 Data Cleaning**: Efficiently handled missing values and ensured the dataset was analysis-ready using R.
- **📊 Data Visualization**: Designed an interactive and insightful Power BI dashboard to communicate findings effectively.
- **🔍 Data Analysis**: Identified key trends and metrics in movie production and performance.

## 📦 Dependencies
- **R Packages**:
  - `tidyverse`
  - `ggplot2`
- **Power BI Desktop**

## ✅ Results
This project showcases my ability to clean raw data and transform it into meaningful visualizations, providing valuable insights into Hollywood movie trends. It highlights my expertise in both data preparation and storytelling through visualizations.

## 📜 License
This project is open source under the MIT License.

