# Fixed Level of Detail Example

FIXED level of detail expressions compute a value using the specified dimensions, without reference to the dimensions in the view.

We are going to create a chart that shows the interval between a customer's first purchase date and any subsequent purchase

1. Open Tableau, connect to Sample Superstore and pull over Orders to canvas, create a new worksheet

2. Click on Analysis and go to Create 2 calculated fields: a FIXED level of detail expression and a date substraction
 - Copy and paste the equation for FIRST PURCHASE DATE:

        {FIXED[Customer Name]: MIN([Order Date])}

 - Copy and paste the equation for DAYS SINCE FIRST PURCHASE:
        DATETRUNC('day',[Order Date])-DATETRUNC('day',[FIRST PURCHASE DATE])

3. Drag Days Since First Purchase from Measures to Dimensions (it’s automatically a Measure because it contains a number)

4.  Drag Days Since First Purchase to Columns, click on it and choose Continuous

5.  Drag Sales to Rows and change aggregate to AVG

6.  Click on Sales and Choose a Running Total Quick Calculation

7.  Drag First Purchase Date to Color

8.  Click on it in Color field and change it to Quarter

9.  Click on the dots next to the Quarter field and click colors

        It’s interactive! Click on the different years in the legend

---

# Include Level of Detail Example

Compute values using the specified dimensions in addition to whatever dimensions are in the view.

Useful when you want to calculate at a fine level of detail in the database and then re-aggregate and show at a coarser level of detail in your view. Fields based on INCLUDE level of detail expressions will change as you add or remove dimensions from the view.

        Create a visual of total sales per customer per region

1.  Click on Analysis and Select Create Calculated Field
 - Copy and paste the equation for SalesPerCustomer

        {INCLUDE[Customer Name]: SUM([Sales])}

2.  Place SalesPerCustomer on ROWS and aggregate it as an AVG

3.  Put Region in Columns shelf

4.  Drag SALES over to Rows

        Shows the difference between the sum of sales (somewhere between $390k and 700k per region) AND the avg sales per customer (between 750 and 1100 per region) 

---

# Exclude Level of Detail Example

Prevent the calculation from using one or more of the dimensions present in the view.

Useful for ‘percent of total’ or ‘difference from overall average’ scenarios. They are comparable to such features as Totals and Reference Lines.

Cannot be used in row-level expressions (where there are no dimensions to omit), but can be used to modify either a view level calculation or anything in between (that is, you can use an EXCLUDE calculation to remove dimension from some other level of detail expression).

1.  Go to Analysis and Select “Create Calculated Field”
 - Copy and paste the equation for ExcludeRegion

        {EXCLUDE[Region]: SUM([Sales])}

2.  Move Region and Sales to Columns

3.  Order Date to Rows and make sure it’s by MONTH

        This breaks out the sum of sales by region and month

4.  Drag ExcludeRegion over to Color

        Shades the view to show total sales by month w/o regional component

---
## Vocabulary

### Table Calculations

- Allow transforming values at the detail level of visualization only.
- Executed based on a tabular format with fields in rows and columns.

### Ad-hoc Calculations

- Temporary calculations that are carried out only for current visualizations.

---

# Key performance indicator table

1.  Sub-Category to Rows, Region to Columns and Sales to Text

2.  Create a Calculated Field “KPI”

        IF SUM ([SALES]) > 25000 THEN “ABOVE BENCHMARK” ELSE “BELOW BENCHMARK” END

3.  Change Mark card to Shape from drop down

4.  KPI > Shape

5.  Click Shape and choose KPI: Above (green) and Below(red)

6.  Change Sums from Text to Detail

---

## Extras

Tooltips display when you put the mouse over one or more marks in view.

Utilize the Analytics tab for Modeling & Summarizing
Use trend lines in predicting of given data (linear, logarithmic, exponential and polynomial).

Forecasting depends on the number of historical data points available.

Clustering groups data points together and separating them from other dissimilar data objects.

---

# Your Dashboard

---

## The Interface

### Default 
- the device that the dashboard will be created

### Size 
- size of your presentation screen

### Sheets 
- shows the names of your Worksheets

### Objects 
- how to place sheets and add other helpful items

---

## Objects on Your Dashboard

### Horizontal/Vertical
- how to display your sheets and other objects

### Text
- creates a text box
### Image
- insert outside images (like a pic of a matplotlib plot!)

### Webpage
- creates a web page interface

### Blank
- creates blank box

### Navigation
- provides users with ability to build navigation buttons

### Download
- dashboard can be downloaded in PDF format

### Extensions
- third-party allowing customized visualizations

### Ask Data
- AI functionality from Tableau Server
