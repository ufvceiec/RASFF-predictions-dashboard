# RASFF-predictions-dashboard
Análisis de los datos escrapeados de RASFF portal y desarrollo de un modelo de predicción en varias etapas y de varias características de las posibles alertas futuras. Así mismo se implementan algunas figuras para el desarrollo de un dashboard interactivo con la información estadística de las alertas y de las propias predicciones.

## Organización de los archivos:
El proyecto cuenta con las siguientes carpetas:
- Dashboard
- Independence_test
- Models
- Preprocessing

Todos los archivos están pensados para ejecutarse linealmente, excepto los que contienen figuras desarrolladas con la librería **Bokeh**.
### Dashboard
Archivos con las figuras para la implementación del dashboard.

**Figuras desarrolladas con Bokeh**: Diagramas y figuras interactivas desarrolladas con la librería Bokeh. Para la visualización de todos las figuras realizadas con Bokeh es necesario llevar a cabo los siguientes pasos:

- Abrir Command Prompt 
- Acceder a la carpeta donde esta el notebook
- Introducir el siguiente comando ```bokeh serve --show myapp.py``` cambiando *myapp.py* por el nombre del archivo que contiene la figura.
- Se abrirá automáticamente en el navegador una pestaña con la siguiente dirección ```http://localhost:5006/myapp``` que contendrá la figura interactiva desarrollada.

**Bar_chart_anual.ipynb**: Diagramas de barras simples.

**Bokeh_login_screen.ipynb**: Posible pantalla de login muy simple pensada para mostrar resultados a clientes.

### Independence_test
**Chi-squared_test.ipynb**: Uso del test **chi-squared** indicado para variables categóricas, para analizar la interdependencia de las variables presentes en el dataset.

### Models
**Categorical_embedding.ipynb**: Modelos de clasificación principales. Hacen uso de capas de embedding para re-codificar cada una de las variables categóricas y despúes clasificarlas mediante capas dense o convolucionales 1d (en función de la etapa).

**Baselines**: Carpeta con todos los modelos baselines, ya sean algoritmos de machine learning clásicos, redes neuronales sin embedding o modelos con diferentes codificaciones de los datos.

### Preprocessing
Carpeta con todos los notebooks que hay que ejecutar para preprocesar los datos en bruto obtenidos con el scraper. **El número que hay al principio de cada archivo indica el orden de ejecución**. Los datos en bruto (archivos .csv) obtenidos del scraper serán intruducidos en el archivo 0, el csv obtenido al ejecutar este archivo sera introducido en el archivo 1, y así sucesivamente.

**Data_to_string.ipynb**: Notebook diseñado para convertir cada alerta en una cadena de texto única, posiblemente útil para afrontar el problema como un problema de NLP en un futuro.

**Opcional_preprocess.ipynb**: Preprocesamiento opcional no terminado para intentar mejorar el rendimien to de los modelos.

## Datasets:
Todos los datasets necesarios para a ejecución de los notebooks se encuentran en el Nas (Volumen 1)/carpeta **RASFF_predictions**.

## Contact:
Responsible: Alberto Nogales (alberto.nogales@ceiec.es)\
Supervisors : Alberto Nogales\
Main developers: Rodrigo Díaz (rodrigo.diaz@ceiec.es)
