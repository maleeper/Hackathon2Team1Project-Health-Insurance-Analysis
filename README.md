# Healthcare Insurance Charge Analysis

Healthcare Insurance Charge Analysis is a comprehensive data analysis tool designed to streamline data exploration, analysis, and visualisation. The tool supports multiple data formats and provides an intuitive interface for both novice and expert data scientists.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
* This dataset captures details on personal attributes such as age, gender, BMI, family size and smoking habits as well as geographic factors and their influence on medical insurance charges. 
It can be used to analyze how these attributes impact medical insurance costs and to build predictive models to estimate healthcare expenses.


## Business Requirements
The business requires a predictive model to estimate insurance charges based on customer demographics (age, sex, region) and lifestyle factors (smoker). Since categorical variables cannot be directly used by most models, they must be transformed into a numerical format using one-hot encoding. Additionally, visualizations of the encoded features are required to understand category distributions and their impact on charges, enabling data-driven decisions in pricing strategy, risk assessment, and market targeting.

* Customer Segmentation

    * The distribution plot shows how customers are spread across sex, smoker, and region.

    * Helps insurers identify under-/over-represented groups.

* Risk Assessment

    * Average charges per category plot shows which groups drive higher costs (e.g., smokers have higher charges).

    * Insurers can adjust premiums accordingly.

* Market Strategy

    * Regional distribution can reveal where most insured clients are located.

    * Helps allocate sales and marketing resources effectively.

* Fairness & Compliance

    * By examining how categorical groups differ in charges, insurers can ensure pricing models comply with regulations (avoid discrimination while adjusting for risk).


## Hypothesis and how to validate?


* With Statistical tests (T-Test and ANOVA) in Data Visualization Jupyter Notebook, we justified our findings with the p-value as below. 

**Hypothesis 1 (Smoker Status):** We hypothesize that individuals who smoke will have significantly higher insurance charges compared to those who do not smoke. This will be tested as we keep other attributes constant while we compare relationship between smoker status and medical insurance cost.

    * Answer: Modest significant
    * p-value: 0.0000 (very near to 0)

**Hypothesis 2 (BMI):** We hypothesize that there is a positive correlation between an individual's Body Mass Index (BMI) and their insurance charges. This will be tested as we keep other attributes constant while we compare relationship between BMI and medical insurance cost.

    * Answer: Highly significant
    * p-value: 0.0000 (very near to 0, t-tested with obese and non-obese category)

**Hypothesis 3 (Age):** We hypothesize that older individuals will have higher average insurance charges than younger individuals. This will be tested as we keep other attributes constant while we compare relationship between Age and medical insurance cost.

    * Answer: Highly significant
    * Slope / Age coefficient: 257.72 (Linear Regression) 

**Hypothesis 4 (Region):** We hypothesize that geographic region will have less impact than personal attributes (Smoker status, BMI and Age) on medical insurance cost. This will be tested as we keep other attributes constant while we compare relationship between Age and medical insurance cost.

    * Answer: Modest significant
    * p-value: 0.0309 (ANOVA)

**Hypothesis 5 (Children):** We hypothesize that the number of children an individual has will have an impact on medical insurance cost but will be less than the impact of personal attributes (Smoker status, BMI and Age). This will be tested/validated as we keep other attributes constant while we compare relationship between number of children and medical insurance cost.

    * Answer: Small but statistically significant
    * p-value: 0.0177 (T-Test)


## Project Plan
Kanban board at: https://github.com/users/ka-kwok/projects/7/views/1

* How was the data managed throughout the collection, processing, analysis and interpretation steps?

    * **Collection
    Dataset sourced from Kaggle, containing demographic, lifestyle, and health variables with medical charges as the target. 

    * **Processing
    Data Processing Cleaned missing/inconsistent values, standardized data types, and engineered features such as one-hot encoding, log charges, BMI categories and comorbidity flags. 

    * **Analysis
    Analysis EDA with descriptive statistics and visualizations to explore distributions, trends, and outliers. Statistical Tests: Independent t tests for two-group comparisons (e.g., smoker vs. non-smoker) and one-way ANOVA for multi-group comparisons (e.g., BMI categories, regions). Predictive Modeling: Multiple linear regression to estimate charges based on demographic and lifestyle factors. 

    * **Interpretation
    Interpretation Identified significant factors influencing charges, validated hypotheses with p values, and evaluated model performance using R² and RMSE.



# Choice of Methodology

* **Exploratory Data Analysis (EDA):** Performed to identify patterns, trends, and correlations between personal attributes (such as age, gender, BMI, smoking status, number of children, and region) and the target variable (insurance charges). EDA helps to detect outliers, understand variable distributions, and inform the selection of features for further analysis.

* **Visualization (Boxplots, Scatterplots, Heatmaps):** Utilized to visually represent relationships between key attributes and insurance charges. These visual tools help to clarify the impact of factors like smoking status, BMI, and age on costs, making complex data more accessible for stakeholders.

* **Statistical Testing:** Applied to quantitatively assess the influence of attributes (e.g., smoker status, BMI, age, region, number of children) on insurance charges. Techniques such as T-tests, ANOVA, and regression analysis provide statistical evidence for observed differences and validate hypotheses, ensuring conclusions are robust and data-driven.


 
## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
        Since categorical variables cannot be directly used by most models, they must be transformed into numerical format using one-hot encoding. Additionally, visualizations of the encoded features are required to understand category distributions and their impact on charges, enabling data-driven decisions in pricing strategy, risk assessment, and market targeting.

* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

## Ethical considerations
* During analysis, we identified that gender influenced insurance cost predictions, raising concerns of bias and fairness. Using gender as a predictor could perpetuate discriminatory outcomes and was therefore considered ethically inappropriate. From a privacy perspective, we also introduced an ID column, which served only as a unique identifier without containing personal or sensitive information, ensuring compliance with data protection principles.

* The anonymised ID column allowed us to track records without risking disclosure of personal data. These measures aligned our work with ethical standards, promoted fairness in analysis, and ensured that no legal or societal harm was introduced through our approach.

## Dashboard Design
* We mocked up a Tableau wireframe with Balsamiq showing where each KPI card, chart, and filter sits on the page so the report has a visual representation of the dashboard layout.

### Wireframe
* Link: https://github.com/ka-kwok/Hackathon2Team1Project-Health-Insurance-Analysis/blob/main/Dashboard_wireframe.png

## Unfixed Bugs
* N/A.

## Development Roadmap
* A key challenge encountered was a merge conflict in GitHub, which arose when multiple contributors modified overlapping sections of the codebase. With guidance from our instructor, we reviewed the conflicting files, reconciled the differences manually, and validated the merged version through testing. This process enhanced our understanding of version control and conflict resolution.

* Building on this experience, We aim to develop stronger proficiency in advanced Git workflows, adopt structured branching and collaboration practices, and explore automation tools such as GitHub Actions to streamline integration and testing in future projects.

## Deployment


### Tableau Dashboards

Link: https://public.tableau.com/app/profile/mark.aamodt.leeper/viz/Hackathon2Team1-Health-Insurance/HealthInsuranceDataAnalysisDashboard?publish=yes


## Main Data Analysis Libraries
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Plotly
* Scipy
* scikit-learn
* Tableau


## Credits 

* We credit the Code Institute LMS platform for code references, as well as OpenAI's ChatGPT for references and error handling.

### Content 

- The text for the Home page was taken from the Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page were taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)

### Media

- The photos used on the home and sign-up page are from This Open-Source site
- The images used for the gallery page were taken from this other open-source site


## Acknowledgements (optional)
* We would like to thank the members of our team, Dennis Kwok, Mark Aamodt-Leeper, Jeff Ozule and Jena (who unfortunately had to leave due to other academic commitments). We will also like to thank the Code Institute team including Vasi, Mark and Niel, who have been of great help in our quest for knowledge in Data Analytics. 
