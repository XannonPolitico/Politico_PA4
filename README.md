# Politico_PA4
## Intended Learning Outcomes
1. filter tabular data using several categorical and numerical conditions;
2. construct focused DataFrames by selecting relevant features;
3. summarize the relationship between categorical features and a numerical variable; and
4. communicate a data comparison using clear and correctly labeled plots.

## A. VISAYAS COMMUNICATION DATAFRAME
We are required to create a dataframe labeled as `VisComm` consisting of students whose Hometown is Visayas and whose track is Communication. Displaying only the columns labeled as Name, Gender, Math, Electronics, Average and also its number of rows.
* `board["Average"]` - Assigns the name for the new column
*  `= board[["Math", "Electronics", "GEAS", "Communication"]].mean` - Calculates the average of the students grades on all of their subjects.
*  `(axis=1)` - Assigns the new line into a column. 
* `VisComm = board.loc[(board["Hometown"] == "Visayas") & (board["Track"] == "Communication")` - Assigns the dataframe and filters the dataframe to display students whose hometown is Visayas and that their track is Communication.
* `,["Name", "Gender","Math","Electronics","Average"]]` - Filters the dataframe further to only display the Name, Gender, Math, Electronics, and Average.
* `VisComm.shape[0]` - Displays the number of rows of the dataframe.

## B. VISAYAS FEMALE DATAFRAME
We are required to created a dataframe labeled as `VisFemale` consisting of students whose Hometown is Visayas and whose Gender are Female. Displaying only the columns labeled as Name, Track, GEAS, Electronics, Average. After that, we also display the students whose average is at least 60.
* `VisFemale = board.loc[(board['Hometown'] == 'Visayas') & (board['Gender'] == 'Female')` - Assigns the dataframe and Filters the dataframe to show students whose hometown is Visayas and that their Gender is Female.
* `,['Name','Track','GEAS','Electronics','Average']]` - Filters the dataframe further to only display the Name, Track, GEAS, Electronics, and Average.
* `VF = VisFemale[VisFemale['Average'] >= 60]` - This lets us display the students whose average is at least 60.

## C. CATEGORY-AVERAGE VISUALIZATION
We are required to compute the mean average of three categories labeled as Track, Gender, and Hometown. After which, we display the calculated average means and also create a figure containing bar charts of each categories. Lastly, we write three concise statements where we identify each categories highes average mean.
* `trackmean = board.groupby('Track')['Average'].mean().round(2)` - Calculates the average mean of the category labeled Track.
* `gendermean = board.groupby('Gender')['Average'].mean().round(2)` - Calculates the average mean of the category labeled Gender.
* `hometownmean = board.groupby('Hometown')['Average'].mean().round(2)` - Calculates the average mean of the category labeled Hometown.
* `plt.subplots(1,3, figsize=(16, 5))` - Creates and layouts a figure consisting of three charts.
* `plt.bar` - Creates a bar chart.
* `.index` - Displays the labels for each bar
* `.values` - Displays the calculated average mean in a form of a bar
* `plt.ylim` - Extends or shortens the Y limit of the chart depending on the value entered.
* `plt.title` - Function that helps us assign the title for the chart.
* `plt.subplot(1,3,~)` - Positions the charts to the left, right, or middle.

To view the main python program for Programming Assignment 2, click this link https://github.com/XannonPolitico/Politico_PA4/blob/main/Politico_PA4.ipynb and download. Open in Jupyter Notebook, then run all cells.
