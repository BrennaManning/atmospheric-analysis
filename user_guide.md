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

After you select which .csv files you will be using as your two datasets, you can name each of them in the text boxes pre-filled with 'Dataframe1' and 'Dataframe2'. These text boxes are also ipython widgets, so be sure to follow the procedure outlined above. These names are what will appear in graphs, etc, generated by the notebook. 







### Troubleshooting:

If widgets stop appearing, try restarting your computer. 


