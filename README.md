# project_3_nlp_wine_recommendation

# AI bootcamp project 3 : Wine Recommendation and Food Pairing App
### select the perfect wine, paired with a meal and a recipe based on your taste preferences and expert reviews


# Table of content
1. [Introduction](https://github.com/mr-cworld/project_3_nlp_wine_recommendation/tree/main?tab=readme-ov-file#introduction)
2. [Objective](https://github.com/mr-cworld/project_3_nlp_wine_recommendation/tree/main?tab=readme-ov-file#objective)
3. [Installation](https://github.com/mr-cworld/project_3_nlp_wine_recommendation/tree/main?tab=readme-ov-file#installation)
* [The requirements](https://github.com/mr-cworld/project_3_nlp_wine_recommendation/tree/main?tab=readme-ov-file#the-requirement)
* [Steps to run the program](https://github.com/mr-cworld/project_3_nlp_wine_recommendation/tree/main?tab=readme-ov-file#steps-to-run-the-program)
   
4. [Dataset](https://github.com/mr-cworld/project_3_nlp_wine_recommendation/tree/main?tab=readme-ov-file#dataset)
* [Portuguese Wine Reviews Dataset from "BlogOsVinhos"](https://github.com/mr-cworld/project_3_nlp_wine_recommendation/tree/main?tab=readme-ov-file#portuguese-wine-reviews-dataset-from-blogosvinhos)
* [Wine Aroma Chart](https://github.com/mr-cworld/project_3_nlp_wine_recommendation/tree/main?tab=readme-ov-file#wine-aroma-chart)
5. [Gardio Intuitive UI](https://github.com/mr-cworld/project_3_nlp_wine_recommendation/tree/main?tab=readme-ov-file#gardio-intuitive-ui)
6. [Evaluation](https://github.com/mr-cworld/project_3_nlp_wine_recommendation/tree/main?tab=readme-ov-file#evaluation)
7. [Results](https://github.com/mr-cworld/project_3_nlp_wine_recommendation/tree/main?tab=readme-ov-file#results)
8. [Obstacles and Future Work](https://github.com/mr-cworld/project_3_nlp_wine_recommendation/tree/main?tab=readme-ov-file#obstacles-and-future-work)


## Introduction

The art of wine and food pairing enhances the culinary experience, yet selecting the right combination can be challenging. This project uses a dataset of wine reviews and judge notes to create an intelligent application for recommending wines, pairing them with suitable meals, and providing recipes for the suggested meals.


## Objective 
This project aims to build a recommendation system that simplifies the wine and food pairing process while enhancing the dining experience. The primary objective is to create a Gradio-based Wine Recommendation App that delivers personalized wine recommendations tailored to user preferences, including color, flavor, sensation, price range, and alcohol content. Additionally, the app provides curated meal suggestions paired with the selected wine and displays recipes to guide users in meal preparation. The technical implementation involves several key steps: data preprocessing to clean and translate wine reviews while structuring the dataset to include properties like color, flavor, and alcohol content; building recommendation logic to filter the dataset based on user input and leveraging the Gemini API for detailed reviews and fallback suggestions; developing an intuitive Gradio interface for input and output interactions; and deploying the app for local or server-based usage.

## Installation
### The requirement:
To run this project you need to install python 3.8 or higher,also you need to instal the packages and libraries bellow:
```python
pip install pandas
```
```python
pip install spacy googletrans
```
```python
pip install gradio requests gemini-api
```
```python
pip install google-generativeai
```
```python
pip install langchain-google-genai
```
### Steps to run the program 
1. Clone the repository.
```python
git clone https://github.com/mr-cworld/project_3_nlp_wine_recommendation
```
3. Navigate to the project directory.
4. Run the jupyter notebook file (with VS Code or colab).

## Dataset
### Portuguese Wine Reviews Dataset from "BlogOsVinhos"
1. **Dataset description**:
Over 6 000 Wine Reviews extracted from  [Blog "OsVinhos"](https://osvinhos.blogspot.com)
* Some columns may have its content in Portuguese.
* Some wines are not from Portugal.
* Price is measured in Euros (€)
* Alcohol is measured in Percentage (%)
* Rating goes from 0 to 20
* Review Date is in the following format (Month/Year)

2. **Source** : [open the link here](https://data.world/loliveira1999/portuguese-wine-dataset-from-blogosvinhos)

3. **Features**: Some columns has Content in Portuguese
   * *Before cleaning* :['name', 'region', 'year', 'color', 'castes','alcohol_percentage','winery', 'min_price', 'max_price','oenologist','Jreviw_rating','review_date', 'review_notes','wine_bottle_label','url','winecritic_notes','winecritic_rating']

   * *After Cleaning* : 
   ['Name', 'Region', 'Year', 'Color', 'Castes', 'Alcohol_Percentage',
       'Winery', 'Min_Price', 'Max_Price', 'Judge', 'Judge_Rating',
       'Review_Date', 'Review_Notes', 'Wine_Bottle_Label', 'URL']


4. **Size**:
   * *Before the data cleaning and selection*: 6,672 rows, 17 columns
   * *After the data cleaning and selection*: 6348 rows × 15 columns 

5. **Data Cleaning**:
   * Content in Portuguese were translated to English using NLP.
   * Duplicates and missing data were handled.
   * Droping rows with NAN values and also droping unnecessary columns.
   * Wine color, Aroma and  Flavor  columns were extracted and well classified for better filtering using spacy library.

6. **License**: 
   * Public Domain
  ### Wine Aroma Chart
  1. **Source** : [open the link here](https://sl.bing.net/br4fRIfXsi)
  2. **Data Transforming** : the aroma chart was analysed and transformed to csv file DataFrame.

## Gardio Intuitive UI: 
The app uses Gradio for creating an intuitive interface:

* **Input**:
User selects preferences :Wine Color, Aroma Preference , Flavor Profile, Sweetness Level,Wine Body and price range.
* **Output**:
Recommended wine, Attributes, Wine Description, Recommended Producers, Food Pairing and Recipe.

* **Gemini API**:
Used to analyze review notes for deeper insights and fallback recommendations. Google search links for recommended wines.

## Evaluation


## Results:
* Successfully recommended personalized wines for a diverse range of user inputs.
* Paired meals complemented wine recommendations effectively.
* Recipes added significant value, allowing users to create a complete dining experience.

## Obstacles and Future Work:
* 
Conclusion
The Wine Recommendation and Food Pairing App bridges the gap between wine enthusiasts and culinary delights. By combining data science, AI, and an intuitive interface, this app enhances the dining experience for users worldwide. We look forward to future iterations that refine and expand its capabilities.
