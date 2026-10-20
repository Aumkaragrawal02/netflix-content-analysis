# Netflix Content Analytics & Insights

Exploratory Data Analysis and Visualization of the Netflix Titles Dataset

Student: Aumkar | Enrollment No.: IU2441230694
Team Mate(s): Kunjan - IU2441230662
Indus University (IITE) - B.Tech CSE | Faculty: Vatsal Shingala

---

## 1. Project Definition

This project cleans and analyses the Netflix titles dataset to understand how the
catalogue is composed, how it has grown over time, which countries and genres
dominate, and which audience the content targets.

Objectives:
- Clean the data (missing values, duplicates, data types, outliers)
- Compare Movies vs TV Shows
- Analyse catalogue growth by year added and release year
- Identify top countries, genres and ratings
- Study movie duration and number of TV seasons
- Present findings through clear visualizations and a short insights report

---

## 2. Dataset Use Case

| Attribute          | Details                                       |
|--------------------|-----------------------------------------------|
| File               | netflix_titles.csv                            |
| Records / Columns  | 8,807 rows x 12 columns                       |
| Content split      | 6,131 Movies (69.6%), 2,676 TV Shows (30.4%)  |
| Release years      | 1925 - 2021                                   |
| Source             | Public Netflix titles dataset (Kaggle)        |

Columns: show_id, type, title, director, cast, country, date_added,
release_year, rating, duration, listed_in, description

Use cases: content strategy, market analysis, audience targeting,
trend analysis, and a future content-based recommendation system.

### Data Cleaning Summary

| Step           | Finding                                              | Action                                              |
|----------------|------------------------------------------------------|-----------------------------------------------------|
| Missing values | director 2,634, country 831, cast 825, date_added 10 | Filled with "Unknown" / dropped rows without date   |
| Bad entries    | 3 rows had duration typed in the rating column       | Moved the value to the duration column              |
| Duplicates     | 0 duplicate rows or show_id values                   | Checked and removed if found                        |
| Data types     | date_added was text; duration mixed minutes/seasons  | Converted to datetime; split into duration_min and seasons |
| Outliers (IQR) | 450 long/short movies, 254 long-running shows        | Kept (real values) and flagged them                 |

Cleaned dataset: 8,797 rows x 18 columns (saved as netflix_cleaned.csv).

---

## 3. Visualizations and Outcomes

| No. | Visualization                      | Outcome                                                        |
|-----|------------------------------------|----------------------------------------------------------------|
| 1   | Pie chart - Movies vs TV Shows     | About 70% Movies and 30% TV Shows                              |
| 2   | Stacked bar - Titles added per year| Rapid growth from 2016, peak in 2019                           |
| 3   | Bar chart - Top 10 countries       | United States, India and United Kingdom lead                   |
| 4   | Bar chart - Top 10 genres          | International Movies, Dramas and Comedies dominate             |
| 5   | Bar chart - Rating distribution    | TV-MA and TV-14 cover about 61% (teen/adult audience)          |
| 6   | Histogram - Movie duration         | Median movie length is 98 minutes                              |
| 7   | Bar chart - TV seasons             | About 67% of TV shows have only 1 season                       |
| 8   | Heatmap - Year vs Month added      | Shows the busiest months for new additions                     |

(Add screenshots of the charts from the notebook in the images/ folder.)

---

## 4. Key Insights

- Netflix's catalogue is movie-heavy (about 70% Movies).
- Most titles were added in 2019, and about 70% were released in 2015 or later.
- The US, India and the UK are the top content producers.
- The content mainly targets teen and adult viewers.

---

## 5. Python Libraries and Tools

| Library / Tool            | Purpose                                         |
|---------------------------|-------------------------------------------------|
| Python 3.x                | Core language                                   |
| Pandas, NumPy             | Data loading, cleaning and numeric operations   |
| Matplotlib, Seaborn       | Static visualizations and heatmaps              |
| Google Colab / Jupyter    | Running and presenting the notebook             |
| Git & GitHub              | Version control and team collaboration          |

Install:
    pip install pandas numpy matplotlib seaborn jupyter

---

## 6. Repository Structure

netflix-content-analytics/
|-- data/
|   |-- netflix_titles.csv
|   |-- netflix_cleaned.csv
|-- notebooks/
|   |-- Netflix_Cleaning_Visualization_Colab.ipynb
|-- images/
|   |-- (exported charts)
|-- docs/
|   |-- Project_Proposal.docx
|-- README.md

---

## 7. How to Run

1. Clone the repository:
       git clone [paste GitHub repo link here]
2. Open notebooks/Netflix_Cleaning_Visualization_Colab.ipynb in Google Colab
   (or Jupyter Notebook).
3. Upload netflix_titles.csv when asked in the first cell.
4. Run all cells in order (Runtime > Run all).

---

## 8. Team Contribution

| Task                          | Member 1 (Aumkar) | Member 2 |
|-------------------------------|-------------------|----------|
| Data cleaning                 | Yes               | Review   |
| Visualizations 1-4            | Yes               | -        |
| Visualizations 5-8            | -                 | Yes      |
| README and documentation      | Yes               | Yes      |

---

## 9. Conclusion

The project turns the raw Netflix catalogue into clear visual insights. Netflix is
movie-heavy, grew fastest between 2016 and 2019, is led by US, Indian and UK
content, and is aimed mainly at teen and adult viewers. Future scope: build a
content-based recommendation system using genre, cast and description.
