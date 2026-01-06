
# Workflow Management System - Corporate Workflow Management Solution
## Overview

This project simulates a real-life business process where clients submit files to an organization, which are processed through three key stages:  
Review, Production, and Quality Control. 

The Review team assigns an "estimated effort" for billing, while the Production team completes the task. The final output is then evaluated by the Quality Control team, who assigns an "error rating" (1 being excellent, 5 being poor).  
  
If rework is necessary, the task is sent back to Production or Review; however, reworks are not tracked in this example, and every project ends at the Quality Control stage. The client database is excluded to keep the project scope simple.

This data solution primarily benefits managers and upper management by offering a high-level view of the workflow process, enabling better decision-making, streamlining operations, and ultimately improving both employee and client satisfaction.

## Group and Contributions
#### **Srushti Borkar**
- Responsible for the MongoDB database solution and management. 
- Tasked with the example sample data for this project
- Did the project report
- Did quality check of Jupyter notebook
#### **Shayana Reddy**
- Came up with the ER diagram
- Helped with database schema solution
- Helped with the Documentation
- Took charge with creative solutions and ideas in brainstorming sessions
#### **Athul Rohan**
- Came up with the business case scenario idea from previous workplace experience
- Responsible for the entire Jupyter notebook
- Executed the Readme.md file and documentation
- Helped with production and did quality check of Project report

## How to Run the notebook
#### **Required Python Version and Libraries**

This project requires Python 3. The following libraries are used throughout the notebook for data manipulation, analysis, visualization, and graph-based modeling:

- **pymongo** (MongoClient, ServerApi): Provides the connection between Python and the MongoDB Atlas/Server cluster.

- **pandas** -> data loading, cleaning, and tabular data manipulation

- **numpy** -> numerical operations and array-based computations

- **matplotlib** -> core plotting and chart generation

- **seaborn** -> high-level statistical data visualizations

- **squarify** -> treemap visualizations

- **IPython** -> enhanced notebook display utilities (e.g., formatted tables)

- **datetime** (standard library) -> date and time handling

- **warnings** (standard library) -> suppression of non-critical runtime warnings

#### **Instructions**
- Once the dependencies are installed, you can launch Jupyter Notebook
- Inside the Jupyter interface, navigate to the directory where your notebook is stored and click on the notebook file (.ipynb) to open it.

- To run the notebook, click on the first cell and press Shift + Enter (or click the "Run" button at the top). Continue running the cells one by one to see the output (or click on "run all" to run all cells).
