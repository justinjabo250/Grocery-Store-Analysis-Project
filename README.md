# Grocery-Store-Analysis-Project

This is a Grocery Store Analysis Project, and in order to do our analysis on behalf of The Grocery Store. 

These are the tools we will be utilizing: Excel, Excel-spreadsheet, Excel Power Pivot to complete all tasks that must be completed:

The Dataset has been provided.

Key skill that we shall use:

    . Basics of Working with Excel
    . Excel Functions
    . advanced excel functions
    . Pivot Tables and Power Pivot
    . Descriptive Statistics with MS Excel
    . Measures of Dispersion
    . Comparing Data Distributions


The following are the essential stages we followed to develop our final project.

1. Add Power Pivot to your Menu bar
2. Click on Manage 
![g1](https://user-images.githubusercontent.com/115732734/227537033-083567dd-6a38-4516-be79-a46f63c38edc.jpg)



    3. Create a data model and establish a relationship with the three files.

    4. A new window opens. On the Home Click on Get Data from other sources.

    5. Scroll down and click Excel File.
    
 ![g2](https://user-images.githubusercontent.com/115732734/227543566-5f495b96-9c01-4b06-89d4-f5e404eead4c.jpg)



    6. On the next page, click on browse to choose you file.

![g3](https://user-images.githubusercontent.com/115732734/227543632-a5347816-ebba-4bbe-a419-931aba70c3be.jpg)


   7. Get the Customer file data and check Use first row as column headers. Click on Finish.



   8. To bring the two other files, repeat the steps above to bring in both the Order and Cookie Type files.





Now we want to create relationship between the three files

Click on Diagram View

![g4](https://user-images.githubusercontent.com/115732734/227543647-9c722dcf-8d94-4894-8065-3cbec57e418c.jpg)



   2. Click, drag, and drop the Customer ID in the Orders table on the Customer ID in the Customer table.



   3.  Repeat the step no. 10 for Product in Orders table on Cookie Type in Cookies Type table.
   
   ![g5](https://user-images.githubusercontent.com/115732734/227543704-327bce58-1824-4257-bc8c-11dbd529e3e8.jpg)
   


   4. Click on Data View beside Diagram View to return to your data.



Calculate the revenue made per order.

1. In the Order tab, add three new columns called Revenue, Cost and Profit.
2. To calculate the Revenue, click the first cell under Revenue, go to the formula bar and type **=RELATED(‘Cookie Type’[Revenue Per Cookie]) * Orders[Units Sold]**. Hit Enter.
3. To calculate the Cost, click the first cell under Cost, go to the formula bar and type **=RELATED(‘Cookie Type’[Cost Per Cookie]) * Orders[Units Sold]**
4. To calculate Profit, click the first cell under Profit, go to the formular bar and type **Orders[Revenue] – Orders[Cost]**


**Calculate Total Number of Customers**

Click on Measure
![g6](https://user-images.githubusercontent.com/115732734/227543706-93784572-a57e-4b9e-b783-be1ef2ee3dbc.jpg)


**2. Choose Customer Table, name the measure as Total Number of Customers**
  
![g7](https://user-images.githubusercontent.com/115732734/227543710-684300d8-3077-4d7e-b603-9d796cc87d4d.jpg)

  3. In the formula space, type **=DISTINCTCOUNT([Customer ID])** and click OK.

  4. Click on Manage and navigate to the Customers tab. Below the table, you will see Total Number of Customers = 5
  
![g8](https://user-images.githubusercontent.com/115732734/227543712-e32f7dc2-a758-4ddc-8d01-7adc8a3a9f3c.jpg)



**Calculate Total Profit using a Measure**

1. Click under the previous measure and type in the formular bar **=SUM(Orders[Profit])** and hit Enter.
2. Rename the measure to **Total Profit** and format it to currency.

![g10](https://user-images.githubusercontent.com/115732734/227543717-bff12f89-bcd1-4c6b-8d18-4787a626ae73.jpg)


**Calculate Average Profit per Customer**

Click under the Total Profit and type in the formular bar **=[Total Profit]/[Total number of customers]** and hit Enter.
Rename it to **Average Profit per Customer** and format it to currency.




**Calculate number of Orders each Customer has placed**

Close Power Pivot
Go to **Insert tab** and click on **Pivot Tables.** Choose **New Worksheet.**
Expand the **Customer table** on the far right under **PivotTable fields** and drag the **name** column into **Rows.** Do same for the **Order table** and drag **Order ID** into **Values.** 
Click the drop-down arrow on **Order ID** and go to **Value Field settings.** Change the **Sum** to **Count.**

![g11](https://user-images.githubusercontent.com/115732734/227543721-08e2207c-d88c-4e69-9dfe-a59564801ea0.jpg)



**Calculate Profit made on each Customer**

1. Click on **Customer table** and drag our **Total Profit** measure into the Values field.
2. Click on **Power Pivot** and select **KPIs** just beside Measures. Click on New **KPI**
3. Choose **Total Profit** as KPI base field (value)
4. Make the **Absolute value** 600000 and click **OK**

![g12](https://user-images.githubusercontent.com/115732734/227543723-117b99df-efc8-4bc2-9fe6-abdb1a0ce323.jpg)



   5. A new column named **Total Profit Status** should be added.

   6. Go to the **Customers table** under **PivotTable fields** and scroll down until you see a new icon with traffic symbol  named **Total Profit.**

   7. Uncheck **fx Value (Total Profit), Goal** and **Status** and recheck only Status. You should see the values under **Total Profit Status** changed into color scale.

![g13](https://user-images.githubusercontent.com/115732734/227543728-20b1e362-7f8c-4b3e-a447-7cb77e78b1b9.jpg)



  8. Check both the Goal and fx Value (Total Profit)

**Visualize our Results**

1. Go to PivotChart Analyze and click on Pivot Chart
2. Select Pie Chart and click OK

![g14](https://user-images.githubusercontent.com/115732734/227543731-ba432da6-6ef5-4f25-814c-267661e42690.jpg)

    3. Add a slicer by clicking Insert Slicer under the PivotTable Analyze

    4. The Slicers should be Cookie Type and Date.


![g15](https://user-images.githubusercontent.com/115732734/227543732-00d0e21f-9e25-4b1a-916f-bf899e589ff4.jpg)


**Please find Dataset Below**

[GroceryStoreAwesomeChocolateAnalysis.xlsx](https://github.com/justinjabo250/Grocery-Store-Analysis-Project/files/11063731/Grocery_Store_Awesome_Chocolate_Analysis.xlsx)

<h3>Final Project Grocery Store Analysis</h3>
<p>This Final Study and the recommendations we offer, after Examining and conducting a more thouroghly Analysis of Grocery Stores.</p>

[GroceyStoreAnalysis.xlsx](https://github.com/justinjabo250/Grocery-Store-Analysis-Project/files/11064485/GroceyStoreAnalysis.xlsx)
