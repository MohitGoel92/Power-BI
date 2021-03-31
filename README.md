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

The Data Source Settings button in the Home tab allows us to manage data connections and permissions.

**Note:** Connections to local files reference the exact path. If the file name or location changes, you will need to change the source and browse to the current version.

### Refreshing Queries

By default, all queries in the model will refresh when you use the "Refresh" button from the Home tab. If we do not require a table to refresh as it may be a static data table (e.g. lookup table), in the Query Editor we uncheck "Include in report refresh" to exclude individual queries from the refresh.

**Note:** Exclude queries that don't change often, like lookups and static data tables. This will make the notebook computationally lighter.

### Defining Hierarchies

Hierarchies are groups of nested columns that reflect multiple levels of granularity. For example, a geographical hierarchy may include continent, country, state, city and town. Each hierarchy can be treated as a single item in tables and reports, allowing users to drill up and drill down through different levels of the hierarchy in a meaningful way.

### Importing Models From Excel

The snippet below demonstrates the menu where we import models into excel:

<p align="center"> <img width="400" src= "/Pics/b6.PNG"> </p>

If we have a fully-built model in excel, we can import files built with Power Query/Power Pivot directly into Power BI Desktop using Import>Excel Workbook Contents.

Imported models retrain the following:

- Data source connections and queries.
- Query editing procedures and applied steps.
- Table relationships, hierarchies, field settings ... etc.
- All calculated columns and DAX measures.

**Note:** Power Pivot includes some features that Power BI does not (filtering options, DAX functions help, ... etc); if you are more comfortable in the Excel environment, build your models there and then import to Power BI.

### Things To Remember

- Perform data preprocessing and data cleaning before loading the data into Power BI.
  - Define clear and intuitive table names (avoid spaces) at the beginning as updating them later can be a headache, especially is you have referenced them in various places.
  - Establish a logical data/folder structure beforehand to avoid modifying data source settings if file names or locations change.
- Disable report refresh for all static sources. There is no need to refresh sources that are not updated regularly (or not at all), like lookups or static data tables. It is best to enable refresh for tables that will be changing, for example, live sales data, but the products list may not change frequently or not at all.
- When working with large tables, only load the data that is required. For instance, do not include hourly data if you only require the daily totals, or product-level transactions when you only care about store-level performance. This is due to extra data only slowing us down.

# Creating Table Relationships & Data Models in Power BI

### What Is A Data Model?

Let's examine the situation below:

<p align="center"> <img width="400" src= "/Pics/b7.PNG"> </p>

The above is not a data model. It is a collection of independent tables that share no connections or relationships.

Let's examine the situation below:

<p align="center"> <img width="400" src= "/Pics/b8.PNG"> </p>

The above is a data model. The tables are connected via relationships based on a common key.

### Database Normalisation

Normalisation is the process of organising the tables and columns in a relational database to reduce redundancy and preserve data integrity. It's commonly used to:

- Eliminate redundant data to decrease table sizes and improve processing speed and efficiency.
- Minimise errors and anomalies from data modifications (inserting, updating or deleting records).
- Simplify queries and structure the database for meaningful analysis.

**In laymens terms:** In a normalised database, each table should serve a distinct and specific purpose (i.e. product information, dates, transaction records, customer attributes ... etc).

Without normalisation, we end up with duplicate information that could have been avoided with a lookup table such as a product index table. Minor inefficiencies like this can be highly business impacting as the database scales in size.

### Data Tables Vs Lookup Tables

Models generally contain two types of tables: Data tables (fact tables) and Lookup tables (dimension tables).

- Data Tables contain values, typically at a granular level with ID's or "key" columns that can be used to create table relationships.
- Lookup Tables provide descriptive, often text-based attributes about each dimension in a table.

### Primary Vs Foreign Keys

- Primary keys uniquely identify each row of a table and match foreign keys in related data tables.
- Foreign keys may contain multiple instances of each value and are used to match the primary keys in related lookup tables.

### Relationships Vs Merged Tables

Merged tables create redundant data and utilises significantly more memory and processing power than creating relationships between multiple small tables.

### Creating Table Relationships

We have two options to create table relationships, they are:

**Option 1:** Click and drag to connect the primary and foreign keys within the Relationships pane. This is demonstrated by the picture below.

<p align="center"> <img width="400" src= "/Pics/b9.PNG"> </p>

**Option 2:** Add or detect relationships using the Manage Relationships dialog box. This is demonstrated by the picture below.

<p align="center"> <img width="400" src= "/Pics/b10.PNG"> </p>

### Creating "Snowflake" Schemas

Let's observe the below tables.

<p align="center"> <img width="400" src= "/Pics/b11.PNG"> </p>

From observation, we notice that the tables do not contain a primary key that is common to all. In this case, we can attempt to create relationships using primary keys common to only two tables at a time. In our case, the Sales_Data table can connect to Products using the ProductKey field, but cannot connect directly to the Subcategories or Categories table. 

By creating relationships from Products to Subcategories (using ProductSubcategoryKey) and Subcategories to Categories (using ProductCategoryKey), we have essentially connected Sales_Data to each lookup table. Filter context will now flow all the way down the chain.

**Note:** Models with chains of dimension tables are often called snowflake schemas, whereas star schemas usually have individual lookup tables surrounding a central data table.

### Relationship Cardinality

Cardinality refers to the uniqueness of values in a column. For our purposes, all relationships in the data model should follow a "one-to-many" cardinality; one instance of each primary key, but potentially many instances of each foreign key. In the case given below, there is one instance of each ProductKey in the Products table (noted by 1), and there are many instances of each product key in the Sales_Data table (noted by the asterisk \*). This is due to there being multiple sales associated with each product.

<p align="center"> <img width="400" src= "/Pics/b12.PNG"> </p>

### Filter Flow

The filter directions that are shown as arrows in the relationships view will, by default, point from the "one" side of the relationship (lookups) to the "many" side (data).

- When we filter a table, that filter context is passed along to all related "downstream" tables (following the direction of the arrow).
- Filters cannot flow "upstream" (against the direction of the arrow).
- If we filter using the primary key from a data table, it will give incorrect data to the other data tables.

**Note:** It is common practice to arrange the loookup tables above the data tables in the model as a visual reminder that filters flow "downstream".

When editing relationships between tables, we can also set the filter direction from single to both which allows the filter context to flow both ways. We will now get the correct data if we use the primary key for a data table and not the lookup table. However, it is advised to only use two-way filters carefully and only when necessary.

If we use multiple two-way filters in a more complex model, we run the risk of creating "ambiguous relationships" by introducing multiple filter paths between tables. Let's examine the below tables.

<p align="center"> <img width="400" src= "/Pics/b13.PNG"> </p>

We can't create a direct active relationship between the Sales_Data and Product_Lookup because that would introduce ambiguity between the tables Product_Lookup and Territory_lookup. To make this relationship active, we must deactivate or delete one of the relationships between Product_Lookup and Territory_Lookup first.

In the model above, filter context from the Product_Lookup table can be passed down to Returns_Data and up to Territory_Lookup, which would filter accordingly based on the TerritoryKey values passed from the Returns table. If we are able to activate the relationship between Product_Lookup and Sales_data as well, filters could pass from the Product_Lookup table through either the Sales or Returns table to reach the Territory_Lookup, which could yield conflicting filter context.

