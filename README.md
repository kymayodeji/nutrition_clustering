# nutrition_clustering

### Objective
The objective of the analysis is to determine an optimal clustering model to use to detect food groups based on nutritional data.

### Data
The United States Department of Agriculture Agricultural Research Service’s(https://fdc.nal.usda.gov/) Food composition database contains numerous food products and associated descriptions of their nutritions. This dataset is available on Kaggle(https://www.kaggle.com/datasets/maheshdadhich/us-healthcare-data/?select=Nutritions_US.csv) and is the result of web scraping the USDAA's website and converted into a csv file. Variables are self-explanatory names yet the descriptions can be found at this link - variables descriptions -( All values are per 100 grams). 
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
22. Niacin_(mg) - Niacin
23. Panto_Acid_(mg) - Pantothenic acid
24. Vit_B6_(mg) - Vitamin B6
25. Folate_Tot_(æg) - Folate, total
26. Folic_Acid_(æg) - Folic acid
27. Food_Folate_(æg) - Folate, food
28. Folate_DFE_(æg) - Folate, DFE
29. Choline_Tot_ (mg) - Choline, total
30. Vit_B12_(æg) - Vitamin B-12
31. Vit_A_IU - Vitamin A, IU
32. Vit_A_RAE - Vitamin A, RAE
33. Retinol_(æg) - Retinol
34. Alpha_Carot_(æg) - Carotene, alpha
35. Beta_Carot_(æg) - Carotene, beta
36. Beta_Crypt_(æg) - Cryptoxanthin, beta
37. Lycopene_(æg) - Lycopene
38. Lut+Zea_ (æg) - Lutein + zeaxanthin
39. Vit_E_(mg) - Vitamin E (alpha-tocopherol)
40. Vit_D_æg - Vitamin D (D2 + D3)
41. Vit_D_IU - Vitamin D
42. Vit_K_(æg) - Vitamin K (phylloquinone)
43. FA_Sat_(g) - Fatty acids, total saturated
44. FA_Mono_(g) - Fatty acids, total monounsaturated
45. FA_Poly_(g) - Fatty acids, total polyunsaturated
46. Cholestrl_(mg) - Cholesterol
47. GmWt_1 - gram weight 1
48. GmWt_Desc1 gram weight 1 descriptions
49. GmWt_2 - gram weight 2
50. GmWt_Desc2 - gram weight 2 description

###Exploratory Data Analysis, Data Cleaning and Data Pre-Processing
The dataset had a size of 8, 790 rows/observations and 50 columns. 

###Methods
We used multiple clustering methods that where trained on the same stratified train-test split (80%/20%) of the dataset. Each classification model was tuned using GridSearch to find the optimal hyperparameters to train, fit and test the model. Tmultiple metrics were used to compare the training and testing errors for the different models used.

Findings and Insights Summary


###Next Steps
