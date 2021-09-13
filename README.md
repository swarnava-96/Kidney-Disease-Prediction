# Kidney-Disease-Prediction

#### Goal: To develop a POC using Flask, HTML and CSS for predicting whether a person is suffering from Kidney Disease or not, implementing Machine Learning algorithm.

### About the Data set: 
This is a machine learning project where we will predict whether a person is suffering from a Kidney Disease or not. The dataset was downloaded from Kaggle. The data was taken over a 2-month period in India with 25 features ( eg, red blood cell count, white blood cell count, etc). The target is the 'classification', which is either 'ckd' or 'notckd' - ckd=chronic kidney disease. There are 400 rows. A binary classification problem statement.

### Project Description: 
After loading the dataset("kidney_disease.csv") the first step was to perform an extensive Exploratory Data Analysis(EDA). Initially,the features were renamed for better understanding. Then the dataset was divided into numerical and categorical features. All the vaues of the categorical features were analysed and data cleaning was performed. Then countplots were created for the categorical features to check the unique values. Count plos for the target was also made to check whether the dataset is balanced or not.
It was a balanced dataset. Then a correlation heatmap was plotted to check the correlation between all the features.

The second step was to perform Feature Engneering. Most of the work was already completed in EDA. Here Label Encoding was performed on selected categorical features. The dataset was divided into independent(X) and dependent(y) features. Nan values were dropped.

The third step was Feature Selection. Features were selected manually based on domain knowledge. 'blood_pressure', 'specific_gravity', 'albumin', 'sugar', 'red_blood_cells', 'pus_cell', 'pus_cell_clumps' were the features that got selected.

The Forth step was Model Building. The dataset was divided into indepenent and dependen features. Train test split was performed for getting the train and test datasets.
Support Vector Classifier(SVC) with "linear" kernel was applied on the training data after testing with other Machine Learning algorithmns.
Predicton and validaion was performed on the test dataset.

The fifth step was to perform Hyperparameter Optimization on our model. I have not done this step but I have mentioned the codes that are required. The reason why I have skipped this step was due to system issue and the score I was getting without Hyperparameter optimization was somewhere around 98%
The false positives and the false negatives were also handled amazingly by the base model. As the dataset is small, doing a optimizing the hyperparameters wont have much effect.

The final step was to save the model as a pickle file to reuse it again for the Deployment purpose. Joblib was used to dump the model at the desired location.

The "Kidney Disease Prediction.ipynb" file contains all these informations.

### Deployment Architecture: 
The model was deployed locally (port 5000). The backend part of the application was made using Flask and for the frotend part HTML and CSS was used.
I have not focussed much on the frontend as I am not that good at it. The file "app.py" contains the entire flask code and inside the templates folder, "kidney.html" contains the homepage and "result.html" contains the result page. 

### Installation:
The Code is written in Python 3.7.3 If you don't have Python installed you can find it [here](https://www.python.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. To install the required packages and libraries, run this command in the project directory after [cloning](https://www.howtogeek.com/451360/how-to-clone-a-github-repository/) the repository:

##### 1. First create a virtual environment by using this command:
```bash
conda create -n myenv python=3.7
```
##### 2. Activate the environment using the below command:
```bash
conda activate myenv
```
##### 3. Then install all the packages by using the following command
```bash
pip install -r requirements.txt
```
##### 4. Then, in cmd or Anaconda prompt write the following code:
```bash
python app.py
```
##### Make sure to change the directory to the root folder.  

### A Glimpse of the application

### Further Changes to be Done
- [ ] Including more features.
- [ ] Deploying the Web Application on Cloud.
     - [ ] Google Cloud 
     - [ ] Azure
     - [ ] Heroku
     - [ ] AWS

### Technology Stack

<img src="https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=darkgreen" /> <img src="https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white" /> <img src="https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white" /> ![Seaborn](https://img.shields.io/badge/Seaborn-%230C55A5.svg?style=for-the-badge&logo=seaborn&logoColor=%white)  <img src="https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" /> <img src="https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white" /> <img src="https://img.shields.io/badge/conda-342B029.svg?&style=for-the-badge&logo=anaconda&logoColor=white"/> <img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white" />  <img src="https://img.shields.io/badge/matplotlib-342B029.svg?&style=for-the-badge&logo=matplotlib&logoColor=white"/> <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" /> <img src="https://img.shields.io/badge/Spyder-838485?style=for-the-badge&logo=spyder%20ide&logoColor=maroon" />

