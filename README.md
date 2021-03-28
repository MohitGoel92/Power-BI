# Power-BI

In this repository we have Power BI files where we explore a wide variety of different techniques to analyse the data for different business tasks. This knowledge is then tested and concretised by exercises which are great for learning and practice. A novice learning Power BI, or an experienced individual who is coming back to Power BI after some time of not using it will also benefit from going through the material.

## Sections:

- **Introducing Power BI Desktop:** Installing Power BI, exploring Power BI workflow, comparing Power BI vs Excel ... etc.
- **Connecting and Shaping Data:** Connecting to source data, shaping and transforming tables, editing, merging and appending queries .. etc.
- **Creating a Data Model:** Building relational models, creating table relationships, understanding cardinality, exploring filter flow ... etc.
- **Adding Calculated Fields with DAX:** Understanding DAX syntax, adding calculated columns and measures, writing common formulas and functions ... etc.
- **Visualising Data with Reports:** Inserting charts and visuals, customising formats, editing interactions, applying filters and bookmarks ... etc.
- **Project:** Building a pro quality B.I. report from a new dataset.

# Connecting and Shaping Data with Power BI Desktop

Power BI can connect to virtually any type of source data, some of which include:

- Flat files and folders (csv, text, xls)
- Databases (SQL, Access, Oracle, IBM, Azure)
- Online Services (Sharepoint, GitHub, Dynamics 365, Google Analytics, Salesforce, Power BI Service)
- Others (Web feeds, R scripts, Spark, Hadoop)

The diagram below shows us these options.


<p align="center"> <img width="800" src= "/Pics/b1.PNG"> </p>

### Query Editor

The diagram below shows the query editor (transform data):

<p align="center"> <img width="800" src= "/Pics/b2.PNG"> </p>

- The top bar contains query editing tools. Functionalities such as table transformations, calculated columns, statistical operations and extraction can all be performed using this.
- The Home tab includes general settings and common table transformations tools.
- The Transform tab includes tools to modify existing columns (e.g. splitting/grouping, transposing, extracting text).
- The Add Column tools create new columns (e.g. based on conditional rules, text operations, calculations, dates).
- The formula at the top contains M code.
- The query list below it on the left shows us the docs that we have loaded into the notebook.
- On the right we have the name of the sheet we have just loaded.
- Underneath that are all the applied steps we have taken. If we wish to remove the previous step or any step while working on this sheet, we simply press x and the step will undue. It is better to use the least amount of steps as loading the notebook will be quicker if we have a lower number of steps performed.

**The Home Tab:**

An example of the home tab is given below:

<p align="center"> <img width="1200" src= "/Pics/b3.PNG"> </p>

From the above, we observe that in the home tab we can:

- Choose or remove columns.
- Keep or remove rows.
- Sort values.
- Change data type (date, currency, percentage, text).
- Promote header row.
- Duplicate, move & rename columns.
- Promote header rows (using the first row as column headers)

