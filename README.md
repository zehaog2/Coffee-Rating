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
| Rating  | float  | Overall rating of the coffee. [Detailed interpretation](https://www.coffeereview.com/interpret-coffee/)  | 5 |
| Roaster  | str  | Name of the roaster company  | 5 |
| Coffee Name  | str  | Name of the coffee  | 5 |
| Roaster Location  | str  | Location of the roaster  | 104 |
| Coffee Origin  | str  | Origin of the beans  | 572 |
| Roast Level  | str  | Type of the roast (Light, Medium-Light, Medium, Medium-Dark, Dark) | 103 |
| Agtron  | str  | This variable contains 2 values: the left one indicates the Agtron reading for Whole Bean and the right one indicates the Agtron reading for Ground. An Agtron machine reflects light on a sample of coffee in order to objectively and accurately assign a number to the beans’ roast color.  The smaller the number, the darker the roast. How to Interpret Agtron Values: Dark Roast: Agtron 0-35 (very dark brown to almost black); Medium Roast: Agtron 35-55 (medium brown); Light Roast: Agtron 55-100 (lighter shades of brown to cinnamon-like colors). | 103 |
| Est. Price  | str  | Price of the coffee  | 2015 |
| Review Date  | str  | Date of the coffee review | 0 |
| Aroma  | float  | This value assesses how intense and pleasurable is the aroma when the nose first descends over the cup and is enveloped by fragrance.  | 167 |
| Acidity  | float  | Acidity is evaluated on a 1 to 10 scale, reflecting both intensity and quality. A higher score (e.g., 8-10) indicates a lively, bright acidity, often associated with fruity or citrusy notes, while a lower score (e.g., 4-6) suggests a smoother, more subdued acidity, common in darker roasts or naturally low-acid coffees.  | 4679 | 
| Acidity/Structure  | float  | In some reviews, Acidity/Structure is used instead of just Acidity to emphasize how acidity contributes to the overall balance and harmony of the coffee, including its relationship with body, flavor, and aftertaste. This approach provides a more comprehensive evaluation of the coffee’s complexity and sensory experience. The choice between Acidity and Acidity/Structure as a scoring category may depend on the reviewer’s preference, the specific characteristics of the coffee being evaluated, or the goals of the review.   | 5117 |
| Body  | float  | Body refers to the sensation of heaviness, richness, or thickness and associated texture when one tastes coffee. It is rated on a 1-10 scale, where higher scores indicate a richer, fuller mouthfeel. Full-bodied coffee feels rich, creamy, and thick in texture. Often associated with dark roasts or coffees with high oil content, like Sumatran or Brazilian coffees. Medium-bodied coffee has a balanced texture, not too heavy or too light, common in many Central American coffees. Light-bodied coffee feels delicate, crisp, and tea-like, often found in high-altitude, washed coffees like Ethiopian Yirgacheffe. | 116 |
| Flavor  | float  | Flavor encompasses all sensory experiences not covered by acidity, aroma, and body, effectively serving as a synthesis of these elements.  | 120 |
| Aftertaste  | float  | In coffee tasting, aftertaste refers to the sensations that linger after the coffee has been swallowed (or spit out). | 974 |
| With Milk  | float  | "With Milk" refers to the evaluation of a coffee's flavor profile when combined with milk, assessing how well the coffee's characteristics harmonize with the addition of milk.  | 7242 |
| Blind Assessment  | str  | The Blind Assessment section provides an unbiased sensory evaluation of the coffee, describing its aroma, flavor, acidity, body, and finish without knowing its origin or brand. | 0 |
| Notes  | str  | The Notes section provides background information about the coffee, including its origin, variety, processing method, and roaster. | 0 |
| Who Should Drink It  | str  | The Who Should Drink It section provides recommendations for the ideal audience based on the coffee's characteristics and appeal.  | 4360 |
| Bottom Line  | str  | The Bottom Line section in Coffee Review provides a concise summary of the coffee's key characteristics and overall impression.  | 4181 |

**Referece for variable description**
1. https://www.coffeereview.com/coffee-reference/coffee-basics/tasting-vocabulary/
2. https://www.coffeereview.com/agtron-numbers-a-sweet-spot/ 
3. https://www.coffeereview.com/interpret-coffee/ 


**Some difference reviews which do not match the parsing pattern:**
- https://www.coffeereview.com/review/wilton-benitez-colombia-variety-p-01/ 
- https://www.coffeereview.com/review/wilton-benitez-colombia-caturra-p-03/ 
- https://www.coffeereview.com/review/wilton-benitez-colombia-geisha-p-06/ 
- https://www.coffeereview.com/review/wilton-benitez-colombia-orange-bourbon-p-17/ 


**Variables which need further preprocessing:**

1. Agtron: left one for whole bean and right one for ground coffee.
2. Est. Price: Need to standardize units.
3. Review Date: Need to be transformed into dates instead of strings.



