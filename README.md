# nutrition_clustering

### Objective
Since 1917, the US Department of Agriculture (USDA) has publicized different groupings (4, 5, 6 and 7) of food.  Since 1993, six food groups ( 1. Bread, cereal, rice, and pasta, 2. Vegetables,  3. Fruits, 4. Milk, yogurt, and cheeses, 5. Meat, poultry, fish, dry beans, eggs, and nuts group and recommended sparing use of 6. Fats, oils, and sweets) have been publicized based on "nutritional objectives and to moderate intake of those components related to risk of chronic diseases" (Dietary
Recommendations and How They Have Changed Over Time, Davis & Saltos). 

I am looking to determine if the current number of six food groups will need to be updated based upon nutrient similarities.  The objective of the analysis is to determine an optimal model to cluster food groups based on nutritional data and verify that the same food products should remain grouped together. This clustering of over 8000 different food products can be used by nutritionists and dieticians to design a variety of patient menus based on nutritional nees and markers.

### Data
The United States Department of Agriculture Agricultural Research Service’s(https://fdc.nal.usda.gov/) Food composition database contains numerous food products and associated descriptions of their nutritions. This dataset is available on Kaggle(https://www.kaggle.com/datasets/maheshdadhich/us-healthcare-data/?select=Nutritions_US.csv) and is the result of web scraping the USDAA's website. The dataset had a size of 8,790 rows/observations and 51 columns with each row/observation representing a food product and the vast majority (47) of columns numerically representing the amount (per 100 grams) of the associated vitamin or minieral in the food product. Column names are self-explanatory names yet the descriptions can be found below. 

 We will be using this nutritional data to find an optimal clustering of food products based on nutritional similarities.
 Column Names
1. NDB_No - Nutrition database number
2. Shrt_Desc - Short description
3. Water_(g) - water in grams per 100 grams
4. Energy_Kcal - Energy in Kcal
5. Protein_(g) - Protein
6. Lipid_Tot_(g) - Total Lipid
7. Ash_(g) - Ash
8. Carbohydrt_(g) - Carbohydrate, by difference
9. Fiber_TD_(g) - Fiber, total dietary
10. Sugar_Tot_(g) - Total Sugars
11. Calcium_(mg) - Calcium
12. Iron_(mg) - Iron
13. Magnesium_(mg) - Magnesium
14. Phosphorus_(mg) - Phosphorus
15. Potassium_(mg) - Potassium
16. Zinc_(mg) - Zinc
17. Copper_(mg) - Copper
18. Manganese_(mg) - Manganese
19. Selenium_(æg) - Selenium
20. Vit_C_(mg) - Vitamin C, total ascorbic acid
21. Thiamin_(mg) - Thiamin
22. Riboflavin_(mg) - Riboflavin
23. Niacin_(mg) - Niacin
24. Panto_Acid_(mg) - Pantothenic acid
25. Vit_B6_(mg) - Vitamin B6
26. Folate_Tot_(æg) - Folate, total
27. Folic_Acid_(æg) - Folic acid
28. Food_Folate_(æg) - Folate, food
29. Folate_DFE_(æg) - Folate, DFE
30. Choline_Tot_ (mg) - Choline, total
31. Vit_B12_(æg) - Vitamin B-12
32. Vit_A_IU - Vitamin A, IU
33. Vit_A_RAE - Vitamin A, RAE
34. Retinol_(æg) - Retinol
35. Alpha_Carot_(æg) - Carotene, alpha
36. Beta_Carot_(æg) - Carotene, beta
37. Beta_Crypt_(æg) - Cryptoxanthin, beta
38. Lycopene_(æg) - Lycopene
39. Lut+Zea_ (æg) - Lutein + zeaxanthin
40. Vit_E_(mg) - Vitamin E (alpha-tocopherol)
41. Vit_D_æg - Vitamin D (D2 + D3)
42. Vit_D_IU - Vitamin D
43. Vit_K_(æg) - Vitamin K (phylloquinone)
44. FA_Sat_(g) - Fatty acids, total saturated
45. FA_Mono_(g) - Fatty acids, total monounsaturated
46. FA_Poly_(g) - Fatty acids, total polyunsaturated
47. Cholestrl_(mg) - Cholesterol
48. GmWt_1 - gram weight 1
49. GmWt_Desc1 gram weight 1 descriptions
50. GmWt_2 - gram weight 2
51. GmWt_Desc2 - gram weight 2 description

### Exploratory Data Analysis, Data Cleaning and Data Pre-Processing
I removed two columns (49. GmWt_Desc1 and 51. GmWt_Desc2) as they included text descriptions that would not be useful in identifying nutritional values of the foods. The individual identifier 1. NDB_No was also removed for the same reason, but the 2. Short_Desc was kept for identification purposes, but not used to determine the clustering. Over 44 of the remaining 47 columns had null/empty values, but is consistent since not all vitamins or nutrients are found in a food product. I elected to replace the emtpy values with 0 to accurately represent the quantity. Using a correlation matrix, we found very few (less than 5 pairings) of the 47 features were strongly correlated to each other. Most of the columns were strongly skewed, so a log transform was applied and then a feature scaling (normalization) was applied to prepare the data for the clustering models.


### Methods
We used multiple clustering methods (KMeans, Agglomerate, and Gaussian Mixture) to cluster the data. To obtain the ultimate number of clusters we used hyperparameters to tune the various parameters (n_clu, eps and min_clu, and n_components repsectively) needed for each model. The Silhoutee score was the metric used to determine the optimal parameters to use.

### Findings and Insights Summary

All of the clustering methods used identified six clusters as the optimal number to produce the highest silhouette score.  


### Next Steps
Using Dimensionality Reduction would be the next logical step in this analysis in order to reduce the amount of time needed to run the clustering methods.




A paragraph explaining which of your Unsupervised Learning models you recommend as a final model that best fits your needs in terms.

Summary Key Findings and Insights, which walks your reader through the main findings of your modeling exercise.

Suggestions for next steps in analyzing this data, which may include suggesting revisiting this model or adding specific data features to achieve a better model.
