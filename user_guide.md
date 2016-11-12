# Atmospheric Analysis Suite User Guide
##### Brenna Manning  2016

______________________________________________________________________

## Setup
### First things first: Fork/Clone this repository.
Instructions on how to fork a github repository can be found [HERE.](https://help.github.com/articles/fork-a-repo/)
Instructions on how to clone a github repository can be found [HERE.](https://help.github.com/articles/cloning-a-repository/)
If you are knew to github, learn about the basics [HERE.](https://guides.github.com/activities/hello-world/)

### Using Jupyter notebooks.
The analysis suite here is in the form of a jupyter notebook. *analysis_suite.ipynb.*  
This format allows the analysis to be done in a workbook where all code for processing data, and generating visuals and statistics is right there for you to see, and modify if you wish.  You are not required to modify any code in order to use this workbook. This workbook is a mix of text and code, with widgets to input what you want to analyse (datasets, features, etc.) providing instructions throughout of how to use.

For an explanation of how to install and get started with these notebooks, check out the Jupyter notebook [Quickstart Guide.](https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/)

### Your data:
Save your data sets as .csv files in the 'data' folder of this repository. This will make them show up in the dropdown menu when you are selecting datasets to analyze/compare. 


![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/csv_dropdown.png?raw=true "")

### Data formatting requirements:
**Date/time column must be labeled 'Date' and must be in either the format yyyy-mm-dd HH:MM:SS or the format m/dd/yy HH:MM.**

**Temperature data must be included for temperature bracket range functunality. Temperature column header should be labeled 'Temperature_(degC)'.** 


## Let's get started!
In your terminal: navigate to the folder containing *analysis_suite.ipynb*.

![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/terminal_find_folder.png?raw=true "")

Type "jupyter notebook" into the command line. 

![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/terminal_run_jupyter.png?raw=true "")

Your terrminal will show a message that looks something like this:


![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/jupyter_running.png?raw=true "")

And the jupyter notebook window should open in your web browser. That will look something like this: 


![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/jupyter_home.png?raw=true "")

All the files in your folder will appear here. Select analysis_suite.ipynb in this browser window to open the workbook. 

## analysis_suite.ipynb
Let's walk through all the steps of analysis using this notebook!

You will see many blocks of code in this notebook. If you are familiar with python, great. Feel free to edit the code as you wish. If you are not familiar with python do not worry. Everything you need to do can be done without touching the actual code. It is largely there for transparency's sake so you can see our exact analysis methods.

### Running the jupyter notebook?
A brief overview of how to use/interact with the jupyter notebook in the browser.
Jupyter notebooks are made up of cells. Each cell contains either text or code. Some code cells can generate widgets for user inputs or visuals or text outputs. To get the best experience out of this workbook, you need to start at the very top cell, and run them sequentially, entering/selecting inputs throughout.

Click on the top title cell to select it. "**Atmospheric Data Analysis Suite**" Once selected, a box will appear around the cell. To run the cell you have selected, either press ctrl-enter or click the 'run cell, select below' button in the top bar.

![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/run_cell.png?raw=true "")

When you do this - if there is code in the cell, it will run that code, and then the cell below it will be selected. Then you can run that one, selecting the next cell below to proceed through the notebook.

Running the first couple cells of code will import tools we will need and set up a list of data sets available. After running the cells below that we will have the first opportunity to provide user input through ipython widgets. 

#### ipython Widgets

###### CSV Selection
We are using ipython widgets to allow for user inputs without code modifications. 
After you run these two cells:

![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/select_dataframes.png?raw=true "")

You should see a dropdown menu appear after each one. 
In the first dropdown, select a .csv file from the list to be dataframe1. In the second, do the same for dataframe2. 

### *This part can be confusing so be careful:* 
##### Do NOT run these cells again after making your selection. It will clear your inputs and reset to default values. This is true of all ipython widgets. Follow this procedure when providing inputs:
- Run the cell to make the widget appear
- Make your selection or type in your input.
- Select the cell below by clicking on it.
- Resume running sequentially using ctrl+enter.

This will set the value you selected to that feature until that cell is rerun and it is reset to its default. 

##### Dataframe Naming
After you select which .csv files you will be using as your two datasets, you can name each of them in the text boxes pre-filled with 'Dataframe1' and 'Dataframe2'. These text boxes are also ipython widgets, so be sure to follow the procedure outlined above. These names are what will appear in graphs, etc, generated by the notebook. 

##### Feature Selection
When you run the dataframe 1 feature selection cell, a series of checkboxes will appear below the cell, with a scroll bar to see more if they do not fit on the page. Check the box to the right of the feature column headers you would like to include in your analysis. Some may be pre-checked if they are in the list of feature names to select by default. (Temperature, for example.)
![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/checkboxes.png?raw=true "")

##### Dataframe Display
In the cells following feature selection, tables should appear showing the dataframe you have created. The headings of this column show what features of the dataset will be analyzed throughout. This is displayed as a way to confirm this was done as intended.

##### Plot Comparing Same Feature for Two Datasets
After some preprocessing and cleaning you will see the header "Comparing Two Datasets". 
Here, using the two datasets you uploaded at the top of the notebook, you will choose a common variable for the x axis, and another for the y axis for comparison. 
For example, the date or temperature could be represented along the x axis, and another feature would be chosen to see how it varies over that x-axis variable for both datasets. 

Here is an example of a visual this might generate:

![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/two_datasets_feature_dropdowns.png?raw=true "")

![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/two_dataset_comparison.png?raw=true "")


##### Diurnal Profile Showing Comparison of Same Feature for Two Datasets on Average Day

Next you will see a section of the notebook labeled "Compare Two Datasets: Diurnal Profiiles"
To make diurnal profiles, this takes the average value of a feature over the whole dataset at a certain time a day, and plots how this changes for each hour of the day. It is essentially showing how that feature changes from midnight to midnight on the average day. 
Again, this will be done for the two datasets originally uploaded.
You choose a feature and generate the plot for this the same way as above, except the x-axis will always represent hours. 

Here is an example of what this might generate:

![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/diurnal_feature_select.png?raw=true "")


![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/diurnal_graph.png?raw=true "")


##### Select Range of Days and Plot Diurnal Profile Feature Comparison for Those Days
After running these cells and selecting a feature, you will have the oppurtunity to input a start and end to a date range to generate a diurnal profile graph as well as to move these sliders to update the graph in real time. 

![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/diurnal_time_range.png?raw=true "")


##### Select Range of Hours and Make Plot of Daily Average Values within that Time Range

Similarly to the date range diurnal profile plot, here you can select a specific time of day you want to look at a comparison plot of. This will be done with either text inputs or interactive sliders the same way as done above. 


![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/time_range_interactive.png?raw=true "")


##### Separate Datasets into Temperature Brackets and Plot

This is done the same way for temperature ranges if temperature data was included with the proper header. 
These temperature ranges can be created either with cutoff temperatures or by percentiles.

###### Cutoffs

![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/temp_cutoffs_interactive.png?raw=true "")


###### Percentiles


![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/temp_percentiles_interactive.png?raw=true "")


##### Spearman's Rank Correlation Matirx
Spearman's rank correlation tracks how well each series' trends correlate with one another (this is done in a matrix representation). The pandas method dataframe.corr lets us pick spearman, ignores non-number values and constructs a useful dataframe of correlation coefficients to generate the matrix.

The output will look something like this:

![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/corr_matrix.png?raw=true "")

or this:


![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/corr_matrix_5.png?raw=true "")


You will select features to include in the correlation matrix the same way you selected features of the dataframe to analyze at the start of the notebook. Keep in mind that only the columns you select which contain numerical data will be included in the matrix. 

Choose the dataframe you wish to view a correlation matrix for in the dropdown menu.
Once again, check the boxes to the right of the features you wish to select.
As usual after making your selection, do not re-run this cell that generated the widget, but proceed to the cells below.

![alt text](https://github.com/BrennaManning/atmospheric-analysis/blob/master/images/checkboxes.png?raw=true "")




##### Kruskal Test
The last analysis portion of this notebook is the Kruskal Wallis Test. [You can learn more about this test here.](http://www.biostathandbook.com/kruskalwallis.html) It is commonly used to reach conclusions in biology research. You can use it to determine whether or not variation is likely to be due to chance.

You can run this test on a certain feature between two datasets by selecting them from the dropdown menus. The test result will be printed below that cell.  A p-value below 0.5 shows 95% confidence that the differences between some of the medians are statistically significant.  More info on how to interpret these results [can be found here.](http://support.minitab.com/en-us/minitab-express/1/help-and-how-to/modeling-statistics/anova/how-to/kruskal-wallis-test/interpret-the-results/key-results/)


##### Exporting dataframe to a new.CSV File

To export a dataframe you have created/worked with in this notebook, simply select a dataframe from the dropdown menu and in the text box widget below, replace 'test.csv' with whatever you wish to call your new .CSV file.


### Troubleshooting:

If widgets stop appearing, try restarting your computer. 


