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

### The Home Tab

An example of the Home Tab is given below:

<p align="center"> <img width="1200" src= "/Pics/b3.PNG"> </p>

From the above, we observe that in the home tab we can:

- Choose or remove columns.
- Keep or remove rows.
- Sort values.
- Change data type (date, currency, percentage, text).
- Promote header row.
- Duplicate, move & rename columns.
- Promote header rows (using the first row as column headers)

### The Transform Tab

An example of the transform tab is given below:

<p align="center"> <img width="1200" src= "/Pics/b4.PNG"> </p>

From the above, we observe that in the Transform Tab we can:

- Split a text column based on either a specific delimiter or a number of characters.
- Format a text column to upper, lower or proper case, or add a prefix or suffix. Trim is used to eliminate leading and trailing spaces.
- Extract characters from a text column based on fixed lengths, first/last, ranges or delimeters. We can also select two or more columns to merge (or concatenate) fields.
- Perform statistics functions that allow us to evaluate basic statistics for the selected column (sum, min/max, average, count, countdistinct). These tools will return a single value and are commonly used to explore a table rather than prepare it for loading.
- Use standard, scientific and trigonometry tools which allow us to apply standard operations such as addition, multiplication and division. We are also able to apply more advanced calculations such as power logarithm, sine and tangent to each value in the column. Unlike the statistics options, these tools are applied to each individual row in the table.
- Define binary flags via the Information tools (TRUE/FALSE or 1/0) to mark each row in a column as even, off, positive or negative.
- Group By: This allows us to aggregate our data at a different level (e.g. transforming daily data into monthly). 

**Note:** We are able to access many of these tools in both the Transform and Add Column menus. The difference is whether we wish to add a new column or modify an existing one.

### The Add Column Tab

An example of the Add Column tab is given below:

<p align="center"> <img width="1200" src= "/Pics/b5.PNG"> </p>

From the above, we observe that in the Add Column Tab we can use the Date and Time tools that give us to following options:

- Age: Difference between the current time and the date in each row.
- Date only: Removes the time component of a date/time field.
- Year/Month/Quarter/Week/Day: Extracts individual components from a date field (Time-specific options include hour, minute, seconds ... etc).
- Earliest/Latest: Evaluates the earliest or latest date from a column as a single value (can only be accessed from the "Transform" menu).

**Note:** Most of the time we will be performing these operations from the Add Column menu to build out new fields, rather than transforming an individual date/time column.

**Note:** The Index Columns contain a list of sequential values that can be used to identify each unique row in a table (typically starting from 0 or 1). These columns are often used to create unique IDs that can be used to form relationships between tables.

**Note:** The Conditional Columns function creates a new conditional column with outputs we set according to a criteria. For instance, if we had sales data, we can label a quantity of 1 as "single", anything more than 1 as "multiple" and anything else as other (incase we have odd data).

### Pivoting and Unpivoting

Pivoting is the process where we turn distinct row values into columns, or turn columns into rows (unpivoting).

**Note:** Transpose is similar to this, except it doesn't recognise unique values. Instead, the entire table is transformed so that each row becomes a column and vise versa.

### Merging Queries

Merging queries allows you to join tables based on a common column (this is similar to a VLOOKUP in excel).

**Note:** Merging adds columns to an existing table. However, because we can merge tables does not mean we always should. As a general rule, it is better to keep tables seperate and define relationships between them.

### Appending Queries

Appending queries allows us to combine (or stack) tables that share the exact same column structure and data types.

**Note:** Appending adds rows to an existing table.

**Note:** We may use the folder option when loading data to append all the files within the folder automatically, assuming they share the same structure. As we add new files, we are only required to refresh the query and the data sheets will automatically append.

### Data Source Settings

