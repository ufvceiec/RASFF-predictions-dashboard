# RASFF-predictions-dashboard
Analysis of the scraped data from the RASFF portal and development of a prediction model in several stages and of several characteristics of possible future alerts. Likewise, some figures are implemented for the development of an interactive dashboard with the statistical information of the alerts and the predictions themselves.

## Organización de los archivos:
The project contains the following folders:
- Dashboard
- Independence_test
- Models
- Preprocessing

All files are designed to run linearly, except those containing figures developed with the **Bokeh** library.

### Dashboard
Files with the figures for the implementation of the dashboard.

**Figures developed with Bokeh**: Diagrams and interactive figures developed with the Bokeh library. To view all the Bokeh figures, it is necessary to carry out the following steps:

- Open Command Prompt
- Access the folder where the notebook is
- Enter the following command ```bokeh serve --show myapp.py``` changing *myapp.py* for the name of the file that contains the figure.
- A tab with the following address ```http: // localhost: 5006 / myapp``` will automatically open in the browser, that will contain the interactive Bokeh figure.

**Bar_chart_anual.ipynb**: Simple bar charts.

**Bokeh_login_screen.ipynb**: Very simple login screen designed to show results to clients.

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
