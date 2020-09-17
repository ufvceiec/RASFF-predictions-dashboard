# RASFF-predictions-dashboard
Analysis of the scraped data from the RASFF portal and development of a prediction model in several stages and of several characteristics of possible future alerts. Likewise, some figures are implemented for the development of an interactive dashboard with the statistical information of the alerts and the predictions themselves.

## File organization:
The project contains the following folders:
- Independence_test
- Models
- Preprocessing

All files are designed to run linearly. 
(Except those containing figures developed with the **Bokeh** library).

### Independence_test
**Chi-squared_test.ipynb**:  Use of the **chi-squared** test indicated for categorical variables, to analyze the interdependence of the dataset variables.

### Models
**Categorical_embedding.ipynb**: Main classification models. They make use of embedding layers to re-encode each of the categorical variables and then classify them using dense or 1d convolutional layers (depending on the stage).

**Baselines**: Folder with all baseline models: classic machine learning algorithms, neural networks without embedding and models with different data encodings.

### Preprocessing
Folder with all the notebooks that must be run to preprocess the raw data obtained from the scraper. **The number at the beginning of each file indicates the order of execution**. The raw data (.csv files) obtained from the scraper will be entered in file 0, the csv obtained by executing this file will be entered in file 1, and so on.

**Data_to_string.ipynb**: Notebook designed to convert each alert into a unique text string, this might be useful in the near future when dealing with the problem as an NLP problem.

**Opcional_preprocess.ipynb**: Optional preprocessing to try to improve the performance of the models. (**not completed**).

## Datasets:
All necessary datasets for running the notebooks are located in the Nas (Volume 1) / folder **RASFF_predictions**.

## Contact:
Responsible: Alberto Nogales (alberto.nogales@ceiec.es)\
Supervisors : Alberto Nogales\
Main developers: Rodrigo Díaz (rodrigo.diaz@ceiec.es)
