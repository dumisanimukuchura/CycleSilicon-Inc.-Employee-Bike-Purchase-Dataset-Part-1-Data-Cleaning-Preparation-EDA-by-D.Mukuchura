# CycleSilicon Inc. Employee Bike Purchase Dataset – Part 1

## Project Overview
This project creates a synthetic employee dataset for CycleSilicon Inc., a fictional tech-bike company inspired by the cycling cultures of Silicon Valley. It will be utilized to practice Excel skills in:
- Data cleaning (removing duplicates, standardizing text, parsing dates, handling blanks)
- Exploratory Data Analysis (EDA)
- Preparing the groundwork for Part 2 (PivotTables, formulas, dashboards)

## Dataset Information
- **Source**: Synthetic dataset created in-house by AI
- **Records**: 85 employees after cleaning (originally 100)
- **Author**: Dumisani Maxwell Mukuchura
- **Contact**: 
  - Email: [dumisanimukuchura@gmail.com](mailto:dumisanimukuchura@gmail.com)
  - LinkedIn: [Dumisani Maxwell Mukuchura](https://www.linkedin.com/in/dumisani-maxwell-mukuchura-4859b7170/)
  - GitHub: [dumisanimukuchura](https://github.com/dumisanimukuchura)

## Data Dictionary
| Column Name         | Description                              |
|---------------------|----------------------------------------- |
| Employee ID         | Unique numeric identifier                |
| First Name          | Employee's given name                    |
| Last Name           | Employee's family name                   |
| Personal Email      | Employee personal email address          |
| Age                 | Employee age in years                    |
| Gender              | Male/Female                              |
| Marital Status      | Single, Married, Divorced, Widowed       |
| Job Title           | Employee's role/occupation               |
| Annual Salary       | Annual salary in USD                     |
| Education Level     | Highest education completed              |
| Home Owner          | Y/N home ownership indicator             |
| Car Owner           | Y/N car ownership indicator              |
| Commute Distance    | Home-to-work distance categories         |
| Start Date          | Date employee joined company             |
| End Date            | Date left or "Present" if still employed |
| Region              | Geographic region                        |
| Bike Purchase       | Y/N purchased company bike               |
| Bike Satisfaction   | Satisfaction score (1-5 scale)           |

## Project Structure

## 🧹 Steps in Data Cleaning

1. Created a copy of the original dataset.
2. Removed 15 duplicate entries → 85 unique rows remained.
3. Fixed First & Last Names using `TRIM(PROPER(...))`.
4. Cleaned emails and whitespace.
5. Standardized Gender and Marital Status labels for readability.
6. Corrected misspellings in Job Titles.
7. Converted Salary column to Number.
8. Standardized Commute Distance naming.
9. Handled various date formats using Excel formulas.
10. Replaced blank cells in Bike Satisfaction with `N/A`.

### 1. Data Cleaning Phase
- Removed 15 duplicate records (85 remaining)
- Standardized text fields:
  - Proper case names with `=TRIM(PROPER())`
  - Cleaned email addresses with `=TRIM()`
  - Fixed job title misspellings ("Directr" → "Director")
- Converted data types:
  - Age to Number
  - Salary to Number
- Standardized date formats from multiple sources to mm/dd/yyyy
- Handled blank/missing values in Bike Satisfaction (marked as "N/A")

### 2. Lookup & Conditional Formatting
- **Top 10 Paid Employees**: Highlighted in GREEN
- **Youngest 10 Employees**: Highlighted in RED (including ties)
- **Employees hired 2015+**: 60 identified, highlighted in BLUE
- **Bike Satisfaction**: Visualized with ORANGE data bars
- **Lookup Operations**:
  - `XLOOKUP` for first email match
  - `FILTER` for all email matches
- Created age buckets (Adolescent-Young, Middle-Aged, Old)
- Implemented salary raise logic by occupation group

### 3. PivotTable Summaries
- Employee counts by:
  - Job Title (Directors most common: 21)
  - Home Owner status (51 homeowners)
  - Region (Americas largest: 24)
- Salary sums:
  - By Education (PhD highest: $1.83M)
  - By Region (Americas highest: $2.10M)
- Bike purchase rates by region (Europe highest non-purchase: 62.5%)
- Average bike satisfaction by marital status (Married highest: 2.31)

### 4. Formulas & Functions
**Statistical Analysis**:
- Max salary: $148,000
- Average age: 44.3 years
- Median satisfaction: 2.0

**Counting Operations**:
- 20 female bike purchasers
- 24 male non-car owners
- 27 homeowners with bikes

**Math & Aggregation**:
- Total salary pool: $7,918,000
- Female employees salary: $4,256,000
- Single male employees salary: $1,536,000

**Data Transformations**:
- Created Full Name column with `=CONCATENATE()`
- Generated work emails (first.last@cyclesillicon.com)
- Calculated tenure days with `NETWORKDAYS()`

## Key Findings
1. **Compensation**:
   - Top salary: $148,000
   - PhD holders earn the highest combined salary ($1.83M total)

2. **Demographics**:
   - Average age: 44.3 years
   - Majority are homeowners (51 vs 34 non-owners)

3. **Bike Program**:
   - Americas region has highest purchase rate (66.67%)
   - Married employees report highest satisfaction (2.31)

## ✅ Next Steps

Stay tuned for Part 2 of this project where we'll explore:
- **Advanced PivotTables**
- **Interactive Dashboards**
- **Forecasting & What-If Analysis** 
- **More on Data Visualizations**

## Technical Notes
- **Excel Version Compatibility**: Used nested `IF` for Excel 2019 compatibility where `IFS` wasn't available
- **Date Handling**: Complex formulas to standardize multiple date formats
- **Dynamic Arrays**: Used `FILTER()` where available (Excel 365)

---

*Last updated: {4/25/2025}*