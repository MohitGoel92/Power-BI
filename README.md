# Power-BI

This repository is used to deliver a complete course on Power BI that will take a complete Power BI novice to a level of business proficiency. Power BI is not only highly user friendly, insightful and beautifully designed, it is absolutely essential for analytics and business intelligence. Whether you are trying to get your first role in data analytics, business intelligence or wish to simply brush up on your skills, this course will be a highly practical way to make you perform like a pro. Learning a skill like Power BI will open up career doors that you thought were not applicable to you.

In this course we have Power BI files where we explore a wide variety of different techniques to analyse the data. This knowledge is then put into pracice using real-world business tasks. The main aim of this course is to guide an individual to produce **dashboards** and acquaint them with Power BI functionalities such as **DAX** (data analysis expressions).

Regardless of your current level of knowledge, I am sure this repository will be of use. Please see below the list of topics that will be covered and the order in which they should be approached. This makes the course easier to navigate incase you only need to learn a specific topic. I hope you enjoy the course as much as I have enjoyed making it and teaching students and colleagues just like you.

## Sections

- **Introducing Power BI Desktop:** What Power BI is and installation.
- **Connecting and Shaping Data:** Connecting to source data, shaping and transforming tables, editing, merging and appending queries.
- **Creating a Data Model:** Building relational models, creating table relationships, understanding cardinality, exploring filter flow.
- **Adding Calculated Fields with DAX:** Understanding DAX syntax, adding calculated columns and measures, writing common formulas and functions.
- **Visualising Data with Reports:** Inserting charts and visuals, customising formats, editing interactions, applying filters and bookmarks.
- **Project:** Building a pro quality B.I. report from a new dataset.

# Introducing Power BI Desktop

Power BI Desktop is a free, self-service data analysis and report authoring tool that you install on a Windows computer. It can connect to more than 70 on-premises and cloud data sources to turn information into interactive visuals. Data scientists and developers work with Power BI Desktop to produce reports and make them available to the Power BI service [1]. 

In Power BI Desktop, users can:

- Connect to data
- Transform and model the data
- Create charts and graphs
- Create reports and dashboards that are collections of visuals
- Share reports with others using the Power BI service

Below is an example report which shows a dashboard of the Covid-19 pandemic. [2]

<p align="center"> <img width="1000" src= "/Pics/Intro_1.png"> </p>

The example dashboard above gives us detailed information that can be understood simply by inspection. In addition to all the charts and diagrams, we also notice drop down menus at the top of the dashboard. This means users can extract the specific information that's required and drill down to their chosen level of granularity. The fascinating thing about a dashboard like the above is, although it is highly detailed and almost like a work of art, it is relatively quick to create and once created, it will update itself with new data.

### Advantages of using Power BI

- Power BI is quick to setup and is intuitive to use like Excel. 
- Powerful insights can be produced with little to no training. This includes charts, graphs, reports, dashboards, a collection of visuals, data cleaning and connecting to data sources. The platform also integrates with other popular business management tools like SharePoint, Office 365, and Dynamics 365, as well as other non-Microsoft products like Spark, Hadoop, Google Analytics, SAP, Salesforce, and MailChimp.
- Visualisations can be uploaded to the Power BI service, with the data refreshing whenever the underlying dataset is updated.
- Power BI reports provide real time information which is beneficial to an organisation as time-sensitive data can be collected or transmitted. Alerts can also be set up on KPIs to keep users informed on important metrics and measurements.
- Good security features as you are able to give specific privileges to each user so they only have access to the information they are supposed to.
- Users can verbally ask questions in natural language (Cortana) to access charts and graphs. This makes getting data highly user friendly, especially for mobile devices or non-technical users.
- Businesses can input huge quantities of data into Power BI that many other platforms would struggle to process.
- Built-in machine learning features can analyse data and help users spot valuable trends and make educated predictions.
- Powerful personalisation capabilities allow users to create dashboards so they can access the data they need quickly. [3]

### Installation link for Power BI

https://powerbi.microsoft.com/en-us/downloads/

Once downloaded, perform the below three steps whilst taking this course:

- Preview Features: Options -> Preview features -> Deselect anything that is ticked. This is to ensure we are working with the same tools as, depending on when you take this course there is a high probability of developments to have taken place. 
- Data Load: Options -> Data Load -> Deselect "Update or delete relationships when refreshing data" and "Autodetect new relationships after data is loaded". This is so we manually do the work to understand what is going on for learning purposes.
- Regional Settings: Options -> Regional Settings -> English (United States). This is because the dates are in US formation (Month-Day-Year). If you select other regions, you may encounter errors.

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

### Hiding Fields From Report View (For End Users Convenience)

Hiding fields from the Report View makes them inaccessible from the Report Tab (although they can still be accessed within the Data and Relationships view). This is commonly used to prevent users from filtering using invalid fields, or to hide irrelevant metrics from view.

**Note:** Hide the foreign key columns in your data tables to force users to filter using the primary keys in the lookup tables.

### Things To Remember

- Focus on building a normalised model from the start.
  - Make sure each table in the model serves a single, distinct purpose.
  - Use relationships and not merged tables as long and narrow tables are better than short and wide.
- Organise lookup tables above data tables in the diagram view.
  - This serves as a visual reminder that filters flow downstream.
- Avoid complex cross-filtering unless absolutely necessary.
  - Don't use two-way filters when one-way filters will get the job done.
- Hide fields from the report view to prevent invalid filter context.
  - Recommend hiding foreign keys from the data tables so that users can only access valid fields. This will make their work easier and more accurate.

# Analysing Data with DAX Calculations

**DAX:** Data Analysis Exressions.

DAX is the formula language that drives Power BI. With DAX we can:

- Add calculated columns and measures to the model, using intuitive syntax.
- Go beyond the capabilities of traditional "grid-style" formulas, with powerful and flexible functions built specifically to work with relational data models.

### Calculated Columns

Calculated columns allow us to add new, formula-based columns to tables.

- There is no A1-style references; calculated columns refer to entire tables or columns. In excel, we are able to apply formulas on a cell by cell basis, but in Power BI they impact the whole table or column.
- Calculated columns generate values for each row, which are visible within tables in the data view.
- Calculated columns understand row context; they're great for defining properties based on information in each row, but generally useless for aggregation (SUM, COUNT, etc).

**Note:** As a rule of thumb, use calculated columns when we wish to stamp static, fixed values to each row in a table, or use the query editor. Do not use calculated columns for aggregation formulas, or to calculate fields for the "values" area of a visualisation; use measures instead.

Example, for categorising whether the order was for a single item or multiple items, we have used the below DAX calculation:

```
QuantityType = IF(AW_Sales[OrderQuantity]>1,"Multiple Items","Single Item")
```

This will correctly add a column stating whether the order was for single or multiple items. However, if we use the DAX below:

```
TotalQuantity = SUM(AW_Sales[OrderQuantity])
```

We will see each cell in the new column be the sum total repeating itself which is not useful at all. We would therefore better off using a DAX measure.

**Note:** Calculated columns are typically used for filtering data, rather than creating numerical values.

### Measures

Measures are DAX formulas used to generate new calculated values.

- Like calculated columns, measures reference entire tables or columns (no A1-style or grid references).
- Unlike calculated columns, measure values are not visible within tables; they can only seen within a visualisation like aa chart or matrix (similar to a calculated field in an excel pivot).
- Measures are evaluated based on filter context, which means they recalculate when the fields or filters around them change (like new row or column labels are pulled into a matrix or when new filters are applied to a report).

**Note:** We use measures instead of calculated columns when a single row cannot give you the answer. In other words, when we need to aggregate. We use measures to create numerical, calculated values that can be analysed in the "values" field of a report visual.

### Calculated Columns Vs Measures Summary

<p align="center"> <img width="600" src= "/Pics/b14.PNG"> </p>

### DAX Syntax

Let's observe the below DAX Syntax:

```
Total Quantity:= SUM(Transactions[quantity])
```

- Total Quantity: This is the measure name. It is always surrounded in brackets (i.e. [Total Quantity]) when referenced in formulas, so spaces are okay.
- SUM: This is the function name. Calculated columns don't always use functions but measures do:
  - In a calculated column, =Transactions[quantity] returns the value from the quantity column in each row, since it evaluates one row at a time.
  - In a measure, =Transactions[quantity] will return an error since Power BI doesn't know how to translate that as a single value, therefore requiring some sort of aggregation.
- Transactions[quantity]: Transactions is the referenced table name and quantity is the referenced column name.
  - This is a fully qualified column, since it is preceeded by the table name, table names with spaces must be surrounded by single quotes.
    - e.g Without a space: Transactions[quantity]
    - e.g. With a space: 'Transactions Table'[quantity]

**Note:** For column references, use the fully qualified name (i.e. Table[Column]). For measure references, just use the measure name (i.e. [Measure]).

### DAX Operators

For some examples of DAX Operators, the tables below summarise a few.

<p align="center"> <img width="800" src= "/Pics/b15.PNG"> </p>
<p align="center"> <img width="800" src= "/Pics/b16.PNG"> </p>

### Common Function Categories

**Math and Statistics Functions:** Basic *aggregation* functions as well as *iterations* evaluated at the row-level.

- Common Examples:
  - SUM
  - AVERAGE
  - MAX/MIN
  - DIVIDE
  - COUNT/COUNTA
  - COUNTROWS
  - DISTINCTCOUNT

- Iterator Functions:
  - SUMX
  - AVERAGEX
  - MAXX/MINX
  - RANKX
  - COUNTX

**Logical Functions:** Functions for returning information about values in a given *conditional expressions*.

- Common Examples:
  - IF
  - IFERROR
  - AND
  - OR
  - NOT
  - SWITCH
  - TRUE
  - FALSE

**Text Functions:** Functions to manipulate *text strings* or *control formats* for dates, times or numbers.

- Common Examples:
  - CONCATENATE
  - FORMAT
  - LEFT/MID/RIGHT
  - UPPER/LOWER
  - PROPER
  - LEN
  - SEARCH/FIND
  - REPLACE
  - REPT
  - SUBSTITUTE
  - TRIM
  - UNICHAR

**Filter Functions:** *Lookup* functions based on related tables and *filtering* functions for dynamic calculations.

- Common Examples:
  - CALCULATE
  - FILTER
  - ALL
  - ALLEXCEPT
  - RELATED
  - RELATEDTABLE
  - DICTINCT
  - VALUES
  - EARLIER/EARLIEST
  - HASONEVALUE
  - HASONEFILTER
  - ISFILTERED
  - USERELATIONSHIP

**Date & Time Functions:** Basic *date* and *time* functions as well as advanced *time intelligence* operations.

- Common Examples:
  - DATEDIFF
  - YEARFRAC
  - YEAR/MONTH/DAY
  - HOUR/MINUTE/SECOND
  - TODAY/NOW
  - WEEKDAY/WEEKNUM

- Time Intelligence Functions:
  - DATESYTD
  - DATESQTD
  - DATESMTD
  - DATEADD
  - DATESINPERIOD

### Basic Date & Time Functions

- DAY/MONTH/YEAR(): Returns the day of the month (1-31), month of the year (1-12), or year of a given date = DAY/MONTH/YEAR(Date)
- HOUR/MINUTE/SECOND(): Returns the hour (0-23), minute (0-59), or second (0-59) of a given datetime value = HOUR/MINUTE/SECOND(Datetime)
- TODAY/NOW(): Returns the current date or exact time = TODAY/NOW()
- WEEKDAY/WEEKNUM(): Returns a weekday number from 1 (Sunday) to 7 (Saturday), or the week number of the year = WEEKDAY/WEEKNUM(Date, [ReturnType])
- EOMONTH(): Returns the date of the last day of the month, +/- a specified number of months = EOMONTH(StartDate, Months)
- DATEDIFF(): Returns the difference between two dates, based on a selected interval = DATEDIFF(Date1, Date2, Interval)

### Basic Logical Functions (IF/AND/OR)

- IF(): Checks if a given condition is met, and returns one value if the condition is *TRUE*, and another if the condition is *FALSE* = IF(LogicalTest, ResultIfTrue, [ResultIfFalse])
- IFERROR(): Evaluates an expression and returns a specified value if the expression returns an error, otherwise returns the expression itself = IFERROR(Value, ValueIfError)
- AND(): Checks whether both arguments are *TRUE*, and returns *TRUE* if both arguments are *TRUE*, otherwise returns *FALSE* = AND(Logical1, Logical2)
- OR(): Checks whether one of the arguments is *TRUE* to return *TRUE*, and returns *FALSE* if both arguments are *FALSE* = OR(Logical1, Logical2)

**Note:** For the AND() and OR() functions, we are restricted to only two conditions. However, if we use the && and || operators we can include more than two conditions.

### Text Functions

- LEN(): Returns the number of characters in a string = LEN(Text)
- CONCATENATE(): Joins two text strings into one = CONCATENATE(Text1, Text2)
  - **Note:** We can use the & operator as a shortcut, or to combine more than two strings.
- LEFT/MID/RIGHT(): Returns a number of characters from the start/middle/end of a text string = LEFT/RIGHT(Text, [NumChars]), MID(Text, StartPosition, NumChars)
- UPPER/LOWER/PROPER(): Converts letters in a string to upper/lower/proper case = UPPER/LOWER/PROPER(Text)
- SUBSTITUTE(): REPLACES an instance of existing text with new text in a string = SUBSTITUTE(Text, OldText, NewText, [InstanceNumber])
- SEARCH(): Returns the position where a specified string or character is found, reading left to right = SEARCH(FindText, WithinText, [StartPosition],[NotFoundValue])

### Related

- RELATED(): Returns related values in each row of a table based on relationships with other tables = RELATED(ColumnName)

The columnName is the column that contains the values we wish to retrieve.

*RELATED* works almost exactly like a VLOOKUP function - it uses the relationship between tables (defined by primary and foreign keys) to pull values from one table into a new column of another. Since this function requires row context, it can be used as a calculated column or as part of an iterator function that cycles through all the rows in a table (FILTER, SUMX, MAXX, etc).

**Note:** Avoid using RELATED to create redundant calculated columns unless you absolutely need them, since those extra columns increase file size; instead, use RELATED within a measure like FILTER or SUMX.

### Basic Maths & Stats Functions

- SUM(): Evaluates the sum of a column = SUM(ColumnName)
- AVERAGE(): Returns the average (arithmetic mean) of all the numbers in a column = AVERAGE(ColumnName)
- MAX(): Returns the largest value in a column or between two scalar expressions = MAX(ColumnName), MAX(Scalar1, [Scalar2])
- MIN(): Returns the smallest value in a column or between two scalar expressions = MIN(ColumnName), MIN(Scaral1, [Scalar2])
- DIVIDE(): Performs division and returns the alternate result (or blannk) if div/0 = DIVIDE(Numerator, Denominator, [AlternateResult])

### COUNT, COUNTA, DISTINCTCOUNT and COUNTROWS

- COUNT(): Counts the number of cells in a column that contains numbers = COUNT(ColumnName)
- COUNTA(): Counts the number of non-empty cells in a column (numerical and non-numerical) = COUNTA(ColumnName)
- DISTINCTCOUNT(): Counts the number of distinct or unique values in a column = DISTINCTCOUNT(ColumnName)
- COUNTROWS(): Counts the number of rows in the specified table, or a table defined by an expression = COUNTROWS(Table)

### CALCULATE

The CALCULATE function is similar to the *where* clause in SQL.

- CALCULATE(): Evaluates a given expression or formula under a set of defined filters = CALCULATE(Expression, [Filter1], [Filter2], ...)
  - The *Expression* is the name of an existing measure or DAX formula for a valid measure. E.g. [Total Orders], SUM(Returns_Data[ReturnQuantity]).
  - [Filter1], [Filter2] ... represent a list of simple Boolean (True/False) filter expressions (**Note:** These require simple and fixed values; we cannot create filters based on measures.) E.g. Territory_Lookup[Country] = "USA", Calendar[Year] > 1998.

**Note:** CALCULATE works just like SUMIF or COUNTIF in Excel, except it can evaluate measures based on ANY sort of calculation (not just a sum, count ... etc); it may help to think of it like "CALCULATEIF".

### ALL

- ALL(): Returns all the rows in a table, or all values in a column, ignoring any filters that have been applied = ALL(Table or ColumnName, [ColumnName1], [ColumnName2], ...)
  - Table or ColumnName that we want to clear filters on. E.g. Transactions, Products[ProductCategory].
  - [ColumnName1], [ColumnName2], ... is the list of columns that we want to clear filters on (optional). If the first parameter is a table, we cannot specialise additional columns. All columns must include the table name, and come from the same table. E.g. Customer_Lookup[CustomerCity], Customer_Lookup[CustomerCountry], Products[ProductName].

**Note:** Instead of adding filter context, ALL removes it. This is often used when we need to unfilter values that will not react to changes in filter context (i.e. % of total, where the denominator needs to remain fixed).

### FILTER

- FILTER(): Returns a table that represents a subset of another table or expression = FILTER(Table, FilterExpression)
  - "Table" is the table that is to be filtered. E.g. Territory_Lookup, Customer_Lookup.
  - "FilterExpression" is a Boolean (True/False) filter expression to be evaluated for each row of the table. E.g. Territory_Lookup[Country] = "USA", Calendar[Year] = 1998, Products[Price] > [Overall Avg Price]. This goes through the table row-by-row (iterative) and keeps or discards the rows of the data depending on whether it satisfies the FilterExpression. This produces a new table which is a subset of the original table.

**Note:** FILTER is used to add new filter context, and can handle more complex filter expressions than CALCULATE (by referencing measure for example). Since FILTER returns an entire table, it's almost always used as an input to other functions, like CALCULATE or SUMX.

**Note:** Since FILTER iterates through each row in a table, it can be slow and processor-intensive. Therefore, it is better to avoid using FILTER if a CALCULATE function will accomplish the same thing.

### Iterator ("X") Functions

Iterator (or "X") functions allow us to loop through the same calculations or expression on each row of a table, and then apply some sort of aggregation to the results (SUM, MAX, etc).

- Iterator (X) function = SUMX(Table, Expression)
  - SUMX is the aggregation to apply  to calculated rows. E.g. SUMX, COUNTX, AVERAGEX, RANKX, MAXX/MINX.
  - "Table" is the table in which the expression will be evaluated. E.g. Sales, FILTER(Sales, RELATED(Products[Category]) = "Clothing")
  - "Expression" is the expression to be evaluated for each row of the given table. E.g. [Total Orders], Sales[RetailPrice] * Sales[Quantity]

**Note:** This function should be visualised as adding a temporary new column to the table, calculating the value in each row (based on the expression) and then applying the aggregation to that new column (like SUMPRODUCT).

### Time Intelligence Formulas

Time Intelligence functions allow you to easily calculate common time comparisons:

- Performance to-date = CALCULATE(Measure, DATESYTD(Calendar[Date]))
  - Use DATESQTD for quarters or DATESMTD for months.
- Previous period = CALCULATE(Measure, DATEADD(Calendar[Date], -1, MONTH))
  - -1, MONTH: Select an interval (DAY, MONTH, QUARTER, or YEAR) and the number of intervals to compare (i.e. previous month).
- Running total = CALCULATE(Measure, DATESINPERIOD(Calendar[Date], MAX(Calendar[Date]), -10, DAY).
  - -10, DAY: Select an interval (DAY, MONTH, QUARTER, or YEAR) and the number of intervals to compare (i.e. rolling 10-day)

**Note:** To calculate a moving average, use the running total calculation above and divide by the number of intervals.

### Things To Remember: Calculated Columns and Measures

- Don't use a calculated column when a measure will do the trick.
  - Only use calculated columns to stamp static, fixed values to each row in a table.
  - Use measures when aggregation is necessary, or to create dynamic values in a report.
- Write measures for even the simplest calculations (i.e. Sum of Sales)
  - Once you create a measure it can be used anywhere in a report and as an input to other, more complex calculations (no implicit measures).
- Break measures down into simple, component parts.
  - DAX is a difficult language to master; focus on assembling simple components into more advanced formulas.
- Referene columns with the table name, and measures alone.
  - Using fully qualified column references (preceeded by the table name) helps make formulas more readable and intuitive, and differentiates them from measure references.

### Things To Remember: Speed and Performance

- Eliminate redundant columns and keep data tables narrow.
  - Data tables should ideally only contain quantitative values and foreign keys; any extra descriptive columns can usually live in a related lookup table.
- Imported columns are better than calculated columns.
  - When possible, create calculated columns at the source (i.e. in the raw database) or within the Query Editor. This is more efficient than processing those calculations in the Data Model.
- Minimise iterator functions (FILTER, SUMX ... etc).
  - Functions that cycle through each row in a table are computationally expensive. This means they take time and consume processing power.

# Visualising Data with Power BI Report View

The key parts of the report view are given below:

- The View options include Layout, Gridlines, Snap to Grid, Bookmarks and Selection Pane. An image is given below:

<p align="center"> <img width="800" src= "/Pics/b17.PNG"> </p>

- The Visualisation options include Charts, Slicers, Maps and Matrices. An image is given below:

<p align="center"> <img width="200" src= "/Pics/b18.PNG"> </p>

- The Fields/Format/Analytics Pane is used for selecting the relevant data to display. An image is given below:

<p align="center"> <img width="200" src= "/Pics/b19.PNG"> </p>

- The Filters Pane includes Visual-Level, Page-Level, Report-Level and Drillthrough Filters. An image is given below:

<p align="center"> <img width="200" src= "/Pics/b20.PNG"> </p>

- The Field List includes Tables, Columns and Measures. An image is given below:

<p align="center"> <img width="200" src= "/Pics/b21.PNG"> </p>

- The Report Pages are similar to Excel Tabs as they all start as a blank reporting canvas. An image is given below:

<p align="center"> <img width="400" src= "/Pics/b22.PNG"> </p>

### Inserting Objects and Basic Charts

Click on a visualisation type or use the "New Visual" option in the Home tab to insert a blank chart template (usually a column chart by default). Alternatively we can drag a field or measure directly into the report canvas to automatically generate a new visual.

**Note:** We can also add New Pages, Buttons, Text Boxes, Images and Shapes from this menu.

### Formatting Options

A short summary of the formatting options is given below:

<p align="center"> <img width="1000" src= "/Pics/b23.png"> </p>

### Filtering Options

In Power BI reporting, we have four primary filter types, they are:

- 1.) **Visual Level:** Applies only to the specific visual in which it is defined.
- 2.) **Page Level:** Applies to all visuals on the specific page in which it is defined.
- 3.) **Report Level:** Applies to all visuals across all pages of the report.
- 4.) **Drillthrough:** Applies to specific pages, and dynamically changes based on user paths.

**Note:** Filter settings include basic, advanced and Top N options.

### Editing Report Interactions

Report interactions allow us to determine how filters applied to one visual impact others. For example, by selecting the Timeline visual and enabling "Edit interactions" from the Format tab, we can manually determine which visuals should "react" when the date range changes. The image below is used to illustrate this.

<p align="center"> <img width="1000" src= "/Pics/b24.PNG"> </p>

For certain types of visuals, a third option allows us to "highlight" sub-segments of the data, rather than simply filtering Vs not filtering. For instance, when the interaction mode is set to "filter", selecting a category will produce a filtered list of subcategories in the relevant/corresponding visual. However, when the interaction mode is set to "highlight", selecting a category will produce the same list as pre-selection but the relevant data will be highlighted in the relevant/corresponding visual.

### Adding & Linking Bookmarks

A practical use for a bookmark is to direct the viewer of the report to a new page where we can present key insights. We insert a button on the page and link it to a bookmark using the object "Action" property. We are now able to create a narrative from the data and really bring our insights to life.

### "WHAT-IF" Parameters

"What If" Parameters are essentially pre-set measures that produce values within a given range, based on user-inputs (data type, min/max, increment and default). These tools come in handy for forecasting or scenario testing. In our Power BI notebook we have created a "Price Adjustment %" parameter in order to compare Total Revenue (based on the actual price) against Adjusted Revenue (based on the parameter-adjusted price). To clarify this, a screenshot is given below.

<p align="center"> <img width="1000" src= "/Pics/b25.PNG"> </p>

**Note:** When you create a parameter, a new table is automatically added with DAX calculations for "Parameter" and "Parameter Value". This will look something like the below:

```
Parameter = GENERATESERIES(-1, 1, 0.1)
Parameter Value = SELECTEDVALUE(Parameter[Parameter], 0)
```

### Managing & Viewing As Roles

Roles allow you to define filtered views that can be tailored to specific audiences. For instance, if we have analysts in seperate regions like Europe, North America, and the Pacific, we can create seperate views based on simple DAX filter statements. This is beneficial if other regions are not allowed to view the data for other regions. The two screenshots below are used to illustrate what this will look like.

<p align="center"> <img width="1000" src= "/Pics/b261.jpg"> </p>
<p align="center"> <img width="1000" src= "/Pics/b271.jpg"> </p>

### Importing Custom Visuals

In the visualisations pane, click the three dots and add the desired visualisation.

### Desktop Vs Phone Layout

The Phone Layout view allows us to design on a canvas size optimised for mobile viewing (Vs desktop).

**Note:** You can't actually build content within the Phone Layout view; recommend building in Desktop Layout and assembling select visuals for mobile if we plan to share content via the Power BI app.

### Things To Remember: Data Visualisation Best Practices

- Strive for clarity & simplicity, above all else.
  - Aim to maximise impact and minimise noise; it's all about balancing design and function.
- Don't just build charts and graphs, rather, create a narrative.
  - Without context, data is meaningless. Therefore, using filters, bookmarks, and effective visualisations to translate raw data into powerful insights and implications.
- We must always ask ourselves these three key questions:
  - 1.) What type of data are you visualising? (Integer, categorical, time-series, geo-spatial ... etc)
  - 2.) What are you trying to communicate (Relationships, compositions, trending ... etc)
  - 3.) Who is the end user consuming this information? (Analyst, CEO, client, intern ... etc)

# References


[1](https://www.stitchdata.com/resources/7-reasons-power-bi/).  7 reasons to use Microsoft Power BI.

[2](https://community.powerbi.com/t5/COVID-19-Data-Stories-Gallery/COVID-19-Coronavirus-dashboard-Global-pandemic/td-p/978109).  COVID-19 Coronavirus dashboard - Global pandemic.

[3](https://www.nigelfrank.com/insights/everything-you-ever-wanted-to-know-about-microsoft-power-bi).  Everything you ever wanted to know about Microsoft Power BI
