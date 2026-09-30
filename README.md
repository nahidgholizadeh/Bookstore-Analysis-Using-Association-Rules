# Book Sales Market Basket Analysis (Association Rules)

## 📌 Project Overview
This project performs an in-depth **Market Basket Analysis** on a real-world book sales dataset using **JMP software**. The primary objective is to discover hidden patterns in customer purchasing behavior by generating **Association Rules**. 

By analyzing the relationships between different books and authors, this project provides valuable insights that can be leveraged to build a recommendation engine, optimize product placement, and create targeted marketing campaigns (e.g., "Customers who bought Book A also bought Book B").

## 🛠️ Tools & Technologies
- **JMP Software:** Used for data cleaning, joining tables, exploratory data analysis (EDA), and executing the Association Rules algorithms.
- **Data Mining Techniques:** Market Basket Analysis, Association Rules (Support, Confidence, Lift).

## 📂 Dataset
The project utilizes the `BX-Book` dataset, which was initially provided as three separate files and then merged for analysis:
- `BX-Book-Ratings.csv`: Contains user ratings for various books.
- `BX-Books.csv`: Contains metadata about the books (e.g., Title, Author, Year of Publication, Publisher).
- `BX-Users.csv`: Contains demographic information about the users (e.g., Location, Age).
- `joined.jmp`: The final, consolidated JMP data table used for the analysis (created by merging the three CSV files).

*Note: Due to their large size (e.g., the joined table is over 138 MB), the raw data files are not uploaded to this repository, but the analysis process and results are fully documented.*

## 🚀 Key Analysis & Business Insights

### 1. Exploratory Data Analysis (EDA)
Before generating association rules, a comprehensive EDA was conducted to understand the dataset's characteristics:
- **Top Entities:** Identified the top 20 authors (by books published and books sold), top 20 publishers (by books sold), and top 20 best-selling books (e.g., *Wild Animus*, *The Lovely Bones*).
- **Geographical Distribution:** The USA, Germany, and the UK are the top three countries with the highest number of book orders.
- **Publication Trends:** The majority of books in the dataset were published between 1999 and 2002.
- **Rating Distribution:** The average book rating is 7.63, with '8' being the most frequently given score.
- **Customer Demographics:** The primary customer base falls within the 23-29 age range, peaking significantly at age 21.

### 2. Association Rules (Market Basket Analysis)
Association rules were generated to find relationships between purchased items. The analysis was conducted under specific thresholds (Minimum Support = 0.001, Minimum Confidence = 0.04 for books; Confidence = 0.5 for authors) and explored two scenarios: **including** and **excluding** zero ratings.

**Key Findings (Books):**
- **High Lift:** Rules with the highest Lift indicate a very strong association between specific titles, often belonging to the same series (e.g., *Key of Knowledge* -> *Key of Light*, *Left Behind* series).
- **High Confidence:** High confidence rules confirm predictable purchasing patterns within series (e.g., buying Part 2 of *The Lord of the Rings* strongly predicts buying Part 3).
- **High LHS Support:** When filtering for High LHS (Left-Hand Side) Support, *Wild Animus* frequently acts as the antecedent, suggesting it is a common entry point for diverse subsequent purchases.
- **Impact of Ratings:** A comparative analysis showed that the top 10 books with the highest support (most frequently bought together) had a significantly higher average rating compared to the overall dataset average (excluding zero ratings). This confirms that highly-rated books are central to co-purchasing networks.

**Key Findings (Authors):**
- Strong associations exist between authors of similar genres. For example, buying books by *Jude Deveraux* or *Barbara Delinsky* strongly suggests a likelihood of buying books by *Nora Roberts*.
- The analysis effectively grouped authors into related clusters, providing a solid foundation for author-based recommendations.

## 📁 Repository Structure
- `Bookstore-Analysis-Using-Association-Rules.pdf`: The complete, detailed report containing all data visualizations, rule tables, and analytical conclusions generated in JMP.

```text
Bookstore-Analysis-Using-Association-Rules/
│
├── data/
│   └── BX-Book-Ratings.png
│
├── Report/
│   └── Bookstore-Analysis-Using-Association-Rules.pdf
│
└── README.md
```

## 💻 How to Use
1. Clone this repository.
2. Open the `Bookstore-Analysis-Using-Association-Rules.pdf` report to explore the detailed findings, charts, and top 20 association rules based on Lift, Confidence, and LHS Support.
3. The insights from this report can be used as the logic for a book recommendation system.