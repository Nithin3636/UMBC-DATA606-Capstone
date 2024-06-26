## 1. FOREST FIRE PREDICTION SYSTEM

- **Project Title:** FOREST FIRE PREDICTION SYSTEM
- **Prepared for:** UMBC Data Science Master Degree Capstone by Dr Chaoji (Jay) Wang 
- **Author:** Nithin Kumar Allam
- **GitHub:** https://github.com/Nithin3636
- **Linkedin:** https://www.linkedin:in/nithin-allam
- **Powerpoint Presentation:** https://drive.google.com/drive/u/1/folders/1_XYns2LSJUQjaAY9mD2tYb4HePaEg--S
- **Youtube Video:** https://youtu.be/A-moASKun9U


## 2. BACKGROUND

Forest Fire Prediction System gives the most accurate predictions of when fire can take place using data-driven techniques and machine learning models.
Why does it matter ?
1. **Early Warning and Prevention:** By accurately predicting the likelihood of forest fires, these systems enable authorities to take proactive measures to prevent fires from occurring or to mitigate their impact. 
2. **Resource Allocation:** Forest fire prediction systems help in allocating firefighting resources effectively. By identifying areas at high risk of fire, authorities can strategically deploy firefighting crews, equipment, and aircraft to those locations, improving response times and minimizing damage.

**Research Questions:**
1. How can machine learning algorithms be optimized to improve the accuracy and reliability of forest fire prediction models?
2. How do different environmental factors, such as weather conditions, vegetation type, and topography, influence the spread and intensity of forest fires?
3. What role can remote sensing technologies, such as satellite imagery and unmanned aerial vehicles (UAVs), play in enhancing forest fire prediction and monitoring?

## 3. DATA

- **Data sources:** [Algerian Forest Fires from UCI](https://archive.ics.uci.edu/dataset/547/algerian+forest+fires+dataset)
- **Data size:** 12.9 KB
- **Data shape:** 
  - `Algerian_forest_fires_dataset_UPDATE.csv` - 244 rows, 12 columns
- **Time period:** The datasets cover a time span of (from 06/01/2012 to 09/30/2012).
- **What does each row represent?**
  - The dataset includes 244 instances that regroup a data of two regions of Algeria,namely the Bejaia region located in the northeast of Algeria and the Sidi Bel-abbes region located in the northwest of Algeria.

### Data Dictionary

| day | month | year | Temperature | RH | Ws | Rain | FFMC | DMC | DC | ISI | BUI | FWI | Classes | Region |
|-----|-------|------|-------------|----|----|------|------|-----|----|-----|-----|-----|---------|--------|
| 1   | 6     | 2012 | 29          | 57 | 18 | 0.0  | 65.7 | 3.4 | 7.6 | 1.3 | 3.4 | 0.5 | 0       | 1      |
| 2   | 6     | 2012 | 29          | 61 | 13 | 1.3  | 64.4 | 4.1 | 7.6 | 1.0 | 3.9 | 0.4 | 0       | 1      |
| 3   | 6     | 2012 | 26          | 82 | 22 | 13.1 | 47.1 | 2.5 | 7.1 | 0.3 | 2.7 | 0.1 | 0       | 1      |
| 4   | 6     | 2012 | 25          | 89 | 13 | 2.5  | 28.6 | 1.3 | 6.9 | 0.0 | 1.7 | 0.0 | 0       | 1      |
| 5   | 6     | 2012 | 27          | 77 | 16 | 0.0  | 64.8 | 3.0 | 14.2| 1.2 | 3.9 | 0.5 | 0       | 1      |
| ... | ...   | ...  | ...         | ...| ...| ...  | ...  | ... | ... | ... | ... | ... | ...     | ...    |


#### Target/Label
The primary target for the machine learning models in this project is the classes. 

#### Features/Predictors
- Temperature
- relative humidity (RH)
- wind speed (Ws)
- rainfall (Rain)
- Fire Weather Index (FWI)
- FFMC
- DMC
- DC
- ISI
- BUI
- Region

## 4. Exploratory Data Analysis (EDA)
| [Month wise Fire Analysis for Bejaia Region] | [Month wise Fire Analysis for Sidi-Bel Abbes Region] |
|------------------------------|-----------------------|
| This bar plot depicts the Month wise Fire Analysis for Bejaia Region . | This bar plot depicts the Month wise Fire Analysis for Sidi-Bel Abbes Region. |
| <img width="337" alt="image" src="https://github.com/Nithin3636/UMBC-DATA606-Capstone/assets/145934081/11f12b3c-7d86-4dfb-97ad-6e8f8785e07f"> | <img width="337" alt="image" src="https://github.com/Nithin3636/UMBC-DATA606-Capstone/assets/145934081/8d347a78-9a97-46a2-aee2-49a3f97e2008"> |

| [Class Distributions \n 0: No Fire 1: Fire] | [Pie Chart of Classes] |
|------------------------------|-----------------------|
| This bar plot depicts the Class Distributions  . |Pie Chart of Classes. |
| <img width="337" alt="image" src="https://github.com/Nithin3636/UMBC-DATA606-Capstone/assets/145934081/6656c471-01e4-4949-8390-f96229f6f48a"> | <img width="337" alt="image" src="https://github.com/Nithin3636/UMBC-DATA606-Capstone/assets/145934081/4a487fef-7c6e-4b4c-bfe8-f1117ffb89e8"> |



## 5. Model Training

### Models for Predictive Analytics:
- Random Forest: An ensemble method that uses multiple decision trees to make a prediction, providing robustness and reducing the risk of overfitting.
- XGBoost: A gradient boosting framework that uses decision trees and is highly efficient, scalable, and typically provides higher performance.

### Training Procedure:
We will use an 80/20 split for our training and testing data to ensure sufficient data for learning while also having a representative test set for model evaluation.

### Python Packages:
We will utilize scikit-learn for model building, training, and evaluation. This package provides extensive functionalities for data preprocessing, model selection, and evaluation metrics.

### Development Environments:
Google Colab will be used due to its accessibility and the availability of free GPUs for faster computation, which is beneficial for training complex models like XGBoost.
### How will you measure and compare the performance of the models?
- Metrics: We will evaluate our models using accuracy, precision, recall, and the F1 score to comprehensively assess performance across various aspects of classification.
- Comparison: The performance of Random Forest and XGBoost will be compared based on the mentioned metrics to determine which model performs better in the context of forest fire prediction.
  
## 6. Application of the Trained Models
The web app allows users to interact with our trained forest fire prediction models by inputting environmental parameters and receiving predictions on fire occurrences.
- Utilized Flask for model deployment. Offers flexibility in integrating machine learning models with web technologies
- Input: Users can enter data such as temperature, wind speed, and humidity.
- Output: The app displays the likelihood of a forest fire, assisting in proactive fire management and community safety.

## 7. Conclusion
Developed predictive models (Random Forest and XGBoost) to forecast forest fire occurrences based on environmental data from the Algerian Forest Fires dataset. Evaluated models based on accuracy, precision, recall, and F1 score, determining the most effective approach for real-world application
- **Applications:** Support for forest management agencies in fire risk assessment.Tool for community safety awareness and disaster preparedness
- **Limitations:** Limited data scope only two regions and a short time frame. Model performance dependent on data quality and feature selection.
- **Lessons learned:** Importance of feature engineering in enhancing model accuracy. Need for robust testing and validation to ensure model reliability
- **future research:** Expand data collection to include more regions and longer time frames. Explore the integration of satellite imagery and other remote sensing data for enhanced predictive capabilities.
