# nutrition_clustering

###Objective
The objective of the analysis is to determine an optimal clustering model to use to detect food groups based on nutritional data.

###Data
The United States Department of Agriculture Agricultural Research Service’s(https://fdc.nal.usda.gov/) Food composition database contains numerous food products and associated descriptions of their nutritions. This dataset is available on Kaggle(https://www.kaggle.com/datasets/maheshdadhich/us-healthcare-data/?select=Nutritions_US.csv) and is the result of web scraping the USDAA's website and converted into a csv file. Variables are self-explanatory names yet the descriptions can be found at this link - variables descriptions -( All values are per 100 grams). 
NDB_No - Nutrition database number
Shrt_Desc - Short description
Water_(g) - water in grams per 100 grams
Energ_Kcal - Energy in Kcal
Protein_(g) - Protein
Lipid_Tot_(g) - Total Lipid
Ash_(g) - Ash
Carbohydrt_(g) - Carbohydrate, by difference
Fiber_TD_(g) - Fiber, total dietary
Sugar_Tot_(g) - Total Sugars
Calcium_(mg) - Calcium
Iron_(mg) - Iron
Magnesium_(mg) - Magnesium
Phosphorus_(mg) - Phosphorus
Potassium_(mg) - Potassium
Zinc_(mg) - Zinc
Copper_(mg) - Copper
Manganese_(mg) - Manganese
Selenium_(æg) - Selenium
Vit_C_(mg) - Vitamin C, total ascorbic acid
Thiamin_(mg) - Thiamin
Riboflavin_(mg) - Riboflavin
Niacin_(mg) - Niacin
Panto_Acid_(mg) - Pantothenic acid
Vit_B6_(mg) - Vitamin B6
Folate_Tot_(æg) - Folate, total
Folic_Acid_(æg) - Folic acid
Food_Folate_(æg) - Folate, food
Folate_DFE_(æg) - Folate, DFE
Choline_Tot_ (mg) - Choline, total
Vit_B12_(æg) - Vitamin B-12
Vit_A_IU - Vitamin A, IU
Vit_A_RAE - Vitamin A, RAE
Retinol_(æg) - Retinol
Alpha_Carot_(æg) - Carotene, alpha
Beta_Carot_(æg) - Carotene, beta
Beta_Crypt_(æg) - Cryptoxanthin, beta
Lycopene_(æg) - Lycopene
Lut+Zea_ (æg) - Lutein + zeaxanthin
Vit_E_(mg) - Vitamin E (alpha-tocopherol)
Vit_D_æg - Vitamin D (D2 + D3)
Vit_D_IU - Vitamin D
Vit_K_(æg) - Vitamin K (phylloquinone)
FA_Sat_(g) - Fatty acids, total saturated
FA_Mono_(g) - Fatty acids, total monounsaturated
FA_Poly_(g) - Fatty acids, total polyunsaturated
Cholestrl_(mg) - Cholesterol
GmWt_1 - gram weight 1
GmWt_Desc1 gram weight 1 descriptions
GmWt_2 - gram weight 2
GmWt_Desc2 - gram weight 2 description

###Exploratory Data Analysis, Data Cleaning and Data Pre-Processing
The dataset had a size of

###Methods
We used multiple clustering methods that where trained on the same stratified train-test split (80%/20%) of the dataset. Each classification model was tuned using GridSearch to find the optimal hyperparameters to train, fit and test the model. Tmultiple metrics were used to compare the training and testing errors for the different models used.

Findings and Insights Summary


###Next Steps
