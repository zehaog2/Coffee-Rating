# DS5110-Final-Project
Analyze datasets related to coffee/chocolate, cocoa

## Completed tasks:
1. (03/03-Xin) Web scrapping reviews from https://www.coffeereview.com/review/. 8387 reviews were scrapped with review date ranging from Feb. 1997 to Mar. 2025 (data updated until 03/03/2025). [Visit Web Scrapping Codes](Web_Scrapping.ipynb)

2. (03/10-Xin) Parsed the raw text data and saved into dataframe. [Visit Text Parsing Codes](Coffee_Review_Text_Extraction.ipynb)

**Variables Description:**

| Variable Name | Data type | Description | Number of missing values |
|:-------:|:----------:|----------|:----------:|
| URL  | str  | The unique link to the coffee review webpage, which is the primary key for this dataframe  | 0 |
| all_text| str | The original text before parsing | 0 |
| Rating  | float  | Rating of the coffee  | 5 |
| Roaster  | str  | Name of the roaster company  | 5 |
| Coffee Name  | str  | Name of the coffee  | 5 |
| Roaster Location  | str  | Location of the roaster  | 104 |
| Coffee Origin  | str  | Origin of the beans  | 572 |
| Roast Level  | str  | Type of the roast (Light, Medium-Light, Medium, Medium-Dark, Dark) | 103 |
| Agtron  | str  | Value 6  | 103 |
| Est. Price  | str  | Price of the coffee  | 2015 |
| Review Date  | str  | Date of the coffee review | 0 |
| Aroma  | float  | Value 6  | 167 |
| Acidity  | float  | Value 6  | 4679 | 
| Acidity/Structure  | float  | Value 6  | 5117 |
| Body  | float  | Value 6  | 116 |
| Flavor  | float  | Value 6  | 120 |
| Aftertaste  | float  | Value 6  | 974 |
| With Milk  | float  | Value 6  | 7242 |
| Blind Assessment  | str  | Value 6  | 0 |
| Notes  | str  | Value 6  | 0 |
| Who Should Drink It  | str  | Value 6  | 4360 |
| Bottom Line  | str  | Value 6  | 4181 |



**Some difference reviews which do not match the parsing pattern:**

- https://www.coffeereview.com/review/wilton-benitez-colombia-variety-p-01/ 
- https://www.coffeereview.com/review/wilton-benitez-colombia-caturra-p-03/ 
- https://www.coffeereview.com/review/wilton-benitez-colombia-geisha-p-06/ 
- https://www.coffeereview.com/review/wilton-benitez-colombia-orange-bourbon-p-17/ 







