# Grocery-Store-Analysis-Project
This is a Grocery Store Analysis Project, 

Week 1 Project: Grocery Store Analysis

Add Power Pivot to your Menu bar
Click on Manage 
Graphical user interface, application, table  Description automatically generated



    3. Create a data model and establish a relationship with the three files.

    4. A new window opens. On the Home Click on Get Data from other sources.

    5. Scroll down and click Excel File.
    
<h2>HTML Image
<img src="g1.jpg" alt="Trulli" width="500" height="333"></h2>

Graphical user interface, application  Description automatically generated



    6. On the next page, click on browse to choose you file.

Graphical user interface, text, application  Description automatically generated

   7. Get the Customer file data and check Use first row as column headers. Click on Finish.



   8. To bring the two other files, repeat the steps above to bring in both the Order and Cookie Type files.





Now we want to create relationship between the three files

Click on Diagram View
Application, table  Description automatically generated



   2. Click, drag, and drop the Customer ID in the Orders table on the Customer ID in the Customer table.



   3.  Repeat the step no. 10 for Product in Orders table on Cookie Type in Cookies Type table.

Graphical user interface, Excel  Description automatically generated



   4. Click on Data View beside Diagram View to return to your data.



Calculate the revenue made per order.

In the Order tab, add three new columns called Revenue, Cost and Profit.
To calculate the Revenue, click the first cell under Revenue, go to the formula bar and type =RELATED(‘Cookie Type’[Revenue Per Cookie]) * Orders[Units Sold]. Hit Enter.
To calculate the Cost, click the first cell under Cost, go to the formula bar and type =RELATED(‘Cookie Type’[Cost Per Cookie]) * Orders[Units Sold]
To calculate Profit, click the first cell under Profit, go to the formular bar and type Orders[Revenue] – Orders[Cost]


Calculate Total Number of Customers

Click on Measure
Table  Description automatically generated



  2. Choose Customer Table, name the measure as Total Number of Customers

Graphical user interface, application  Description automatically generated

  3. In the formula space, type =DISTINCTCOUNT([Customer ID]) and click OK.

  4. Click on Manage and navigate to the Customers tab. Below the table, you will see Total Number of Customers = 5

Graphical user interface, application, table, Excel  Description automatically generated





Calculate Total Profit using a Measure

Click under the previous measure and type in the formular bar =SUM(Orders[Profit]) and hit Enter.
Rename the measure to Total Profit and format it to currency.
Graphical user interface, application, table, Excel  Description automatically generated



Calculate Average Profit per Customer

Click under the Total Profit and type in the formular bar =[Total Profit]/[Total number of customers] and hit Enter.
Rename it to Average Profit per Customer and format it to currency.




Calculate number of Orders each Customer has placed

Close Power Pivot
Go to Insert tab and click on Pivot Tables. Choose New Worksheet.
Expand the Customer table on the far right under PivotTable fields and drag the name column into Rows. Do same for the Order table and drag Order ID into Values. 
Click the drop-down arrow on Order ID and go to Value Field settings. Change the Sum to Count.
Graphical user interface, application, table, Excel  Description automatically generated



Calculate Profit made on each Customer

Click on Customer table and drag our Total Profit measure into the Values field.
Click on Power Pivot and select KPIs just beside Measures. Click on New KPI
Choose Total Profit as KPI base field (value)
Make the Absolute value 600000 and click OK
Graphical user interface  Description automatically generated



   5. A new column named Total Profit Status should be added.

   6. Go to the Customers table under PivotTable fields and scroll down until you see a new icon with traffic symbol  named Total Profit.

   7. Uncheck fx Value (Total Profit), Goal and Status and recheck only Status. You should see the values under Total Profit Status changed into color scale.

Graphical user interface, application, table, Excel  Description automatically generated



  8. Check both the Goal and fx Value (Total Profit)

Visualize our Results

Go to PivotChart Analyze and click on Pivot Chart
Select Pie Chart and click OK
Graphical user interface, application, table, Excel  Description automatically generated

    3. Add a slicer by clicking Insert Slicer under the PivotTable Analyze

    4. The Slicers should be Cookie Type and Date.

Graphical user interface, application, table, Excel  Description automatically generated

Please find Dataset Below
