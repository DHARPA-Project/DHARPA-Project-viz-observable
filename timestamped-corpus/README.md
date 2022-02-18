# Timestamped corpus visualization prototype
## Creating a data sample for the visualization
Data sample creation available in the 'timestamped-corpus/data_sample_timestamped_corpus.ipynb' Jupyter notebook file.</br>
Colab version: https://colab.research.google.com/drive/1XpFiZJG6xxwcbK8ya7rJNu9jh-SgeXwt?usp=sharing

## Observable notebook 
https://observablehq.com/@dharpa-project/timestamped-corpus
## Data flow

### UI inputs

|Name|Description|Possible value|Type|
|---|---|---|---|
|Scale|How the count of publication is scaled on graph|“color”</br>“height”|string|
|Axis labels|Select the proper interval for the axis (could also probably be partly guessed from data, but manual setting may be necessary if at some point we let users choose font size, the image size will also have an impact - more space if image bigger) | “5-year”</br>“year”</br>“month”</br>“day”</br> |

### Data

|   Name  	|   Description	|   Possible value	|  Type 	|
|---	|---	|---	|---	|
|   Time span	|   This has an impact on ticks display, and date display format on the axis. It could probably be guessed via data, as it is connected with how data is grouped (by day/month or year)	|   “day”</br>“month”</br>“year”	|   	string|
|  Publication data	|   A table containing aggregated data about publications. The aggregation was done using the value of the “Time span” input	|   n/a	|   	table|

### Publication data table schema

|   Column name 	|   Description	|  Type 	|
|---	|---	|---	|
|  Date |   As this is aggregated data, the date will be either first day of year or of a month if the grouping isn’t on day	|   date	|
|  Publication name |   	|   string	|
|  Count |  The number of documents for a given day or month or year 	|   number	|


### Viz output

|Variable name in Obs.|Description|Type|
|---|---|---|
|dateInfo|Outputs the date selected when a user click on the date that appears at the top of the interactive time navigation bar|array ([yyyy,m or mm,d or dd])|

