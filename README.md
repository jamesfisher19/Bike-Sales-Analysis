# Bike-Sales-Analysis

## Dataset Information

 - **Dataset Name:** Bike Sales in Europe
 - **Source:** [Bike Sales in Europe](https://www.kaggle.com/datasets/sadiqshah/bike-sales-in-europe?resource=download)
 
## Data Cleaning

| Step # | Action                                                               | Columns Affected            | Formula/Tool Used                                                               | Notes                                                                                |
| ------ | -------------------------------------------------------------------- | --------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| 1.     | Removed Duplicates                                                   | All                         | **Data > Remove Duplicates**                                                    | Quick removal of duplicates.                                                         |
| 2.     | Change values ‘M’ & ‘S’ to ‘Married’ & ‘Single’                      | Marital Status              | **Find & Replace All**                                                          | Changed values for readability, as readers may not know what the abbreviations mean. |
| 3.     | Change values ‘M’ & ‘F’ to ‘Male’ & ‘Female’                         | Gender                      | **Find & Replace All**                                                          | Changed values for readability, as readers may not know what the abbreviations mean. |
| 4.     | Added ‘Age Range’ column to distinguish Adolescents from Middle Age. | N/A (New Column: Age Range) | `=IF(L2>54,"Old",IF(L2>=31,"Middle Age",IF(L2<31,"Adolescent","Invalid")))` | Given that there are too many different ages, they can be grouped into age ranges.   |

---

## Pivot Table Analysis

| Pivot Table # | Objective                                                             | Rows                                                            | Columns                                     | Values              | Filters |
| ------------- | --------------------------------------------------------------------- | --------------------------------------------------------------- | ------------------------------------------- | ------------------- | ------- |
| 1.            | Average income of someone who bought or did not buy a bike by gender. | Female, Male                                                    | No (bikes purchased), Yes (bikes purchased) | Average Income      | N/A     |
| 2.            | Who is buying bikes based on their commute distance?                  | 0-1 Miles, 1-2 Miles, 2-5 Miles, 5-10 Miles, More than 10 Miles | No (bikes purchased), Yes (bikes purchased) | Bike purchase count | N/A     |
| 3.            | Who is buying bikes based on their age group?                         | Adolescent, Middle Age, Old                                     | No (bikes purchased), Yes (bikes purchased) | Bike purchase count | N/A     |
## Insights
#### Average income of someone who bought or did not buy a bike by gender.
*Overall, both men and women who had lower incomes did not purchase bikes at all. Those who had higher incomes did purchase bikes.*
#### Who is buying bikes based on their commute distance?
*Those who purchased bikes largely lived at most a mile from their workplace. There is also a small spike in people who choose not to purchase a bike if they live 5-10 miles away. For distances over 10 miles, people stop purchasing bikes and may use other forms of transportation.*
#### Who is buying bikes based on their age group?
*Adolescents are less likely to purchase bikes. The largest customer group is middle-aged, as their salaries may have increased to be able to afford a bike. The elderly are least likely to purchase bikes due to their physical conditions.*
