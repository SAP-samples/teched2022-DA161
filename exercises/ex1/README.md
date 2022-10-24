# Exercise 1 – Understanding the Basics of SAP Analytics Cloud Stories

**Objective:** You should develop a basic understanding on how to create visualization within SAP Analytics Coud. 

**Estimated Time:** 25 mins

**Exercise Description:** You and a colleague are building a dashboard for the upcoming board meeting. As a starting point, your colleague has incorporated some Financial Planning Data into the dashboard. You want to further enhance the dashboard to better represent some KPIs while including HR data to get a better understanding on the end-to-end business operations as TCS Technologies. 

**Key Features:**
- Create a set of visualizations (i.e. Chart, Geo, and Table) to illustrate key relationships within your data
- Understand the Builder Panel vs. Styling Panel 
- Learn how to create some calculations

⚠️**Disclaimer**
When completing exercises, some data values or sceenshots may not match what you see on your sceen. It is because the current exercise is based on a feature that is currently in BETA. 

----------------------------------------------------------------------------------------------------------------------------------------

🚩As a Business Analyst for TCS Technologies, we are interested in creating a dashboard that incorporates Business Intelligence, Planning, and Scripting. As a starting point, you want to enhance the dashboard that your colleague has started by incorporating HR data.
 
Lets start by editing the dashboard!

1. Click **Edit**

![image](https://user-images.githubusercontent.com/112718519/197612969-de7df972-55e4-4b46-b451-6a7ba9d4a5a6.png)

🚩 We can see that based on the current design of the dashboard, the Table and Currency Selection (Measure Input Control) takes up the entire dashboard. Let's resize a few widgets to make room for some additional visualizations that we want to create.

2. Scroll to the **bottom of the dashboard**
3. Cick an **hold** the bottom right resize icon of the Table

![image](https://user-images.githubusercontent.com/112718519/197613120-73a3a262-2156-4de5-95bc-f647711a4dee.png)

4. Resize the Table until it just fits all the Accounts

![image](https://user-images.githubusercontent.com/112718519/197613204-25863f2d-b00a-4023-a98f-0bbeb61e629e.png)

5. Click and hold the bottom right resize icon for the Currency Selection Input Control

![image](https://user-images.githubusercontent.com/112718519/197613279-63702395-221e-4b38-b489-54e054348ea4.png)

6. Resize the Currency Selection Input Control so that it has the same height as the Table

![image](https://user-images.githubusercontent.com/112718519/197613366-39d4247d-ead0-4455-93c6-5797bae8d900.png)

⚠️**Quality Check!**
Does your Table and Currency Selection Input Control look like this?

![image](https://user-images.githubusercontent.com/112718519/197613451-4d50dab9-8979-43f7-b9e1-1ef7325952ad.png)

🚩 Now that we have room on our dashboards, let's create our first visualization. We want to provide our colleagues a better understanding of the Gross Profit per Product.
 
Let's insert a Chart to visualize this information.

7. In the toolbar click on the Chart icon

![image](https://user-images.githubusercontent.com/112718519/197613522-55b20a86-4082-41d6-b86c-c3876a537a2e.png)

ℹ️ Welcome to the Builder Panel!

The Builder Panel is a place where you can create your visualizations by specifying elements of a visualization such as accounts, measures, dimensions, filters and so on. The Builder Panel will dynamically update depending on the Data Model and the type of visualization that you are creating. 
 
For this Chart, we are using SAP_XPA_FINANCE, which is a New Model type. The Chart requires at least one Account and at least one Measure to be selected from the Builder Panel. 

![image 7]

8. Click + At least 1 Account required

![image 8]

9. Click on the arrow beside Operating Income to expand the Account
10. Click on Gross Profit
14. Click anywhere outside the Account selection drop down menu to collapse it 

![image 9]

12. Click + At least 1 Measure required

![image 10]

13. Click Currency Selection
14. Click anywhere outside the Measure selection drop down menu to collapse it 

![image 11]

🚩 We can now see data for our Gross Profit as we've successfully met the minimum conditions to view data for our Bar / Column Chart. Let's now add our Product dimension to see the breakdown per Product.

![image 12]

15. Click +Add Dimension

![image 13]

16. Click SAP_XPA_PRODUCT
17. Click anywhere outside the Dimension selection drop down menu to collapse it

![image 14]

🚩 We can now see data for our Gross Profit per Product. However, as Product is a hierarchial dimension, we want to drill down into the Product Dimension so that we can see a more detailed view of our Gross Profit. 

![image 15]

18. Within the Builder Panel click the drill icon in the SAP_XPA_Product Dimension
19. Click on Level 2

![image 16]

🚩 We can now see data for our Gross Profit per Product. Based on this breakdown we can see that Youth Bikes bring us the most Gross Profit in comparison to any other product that we offer.

Let's resize the visualization for better readability. 

20. Click and hold the bottom right resize icon for the Chart
21. Resize the Chart so that it has the same height as the other two widgets

## Summary

**You have completed the entire Understanding the Basics of SAP Analytics Cloud Stories section!**

**You are now able to:**
- Create a set of visualizations (i.e. Chart, Geo, and Table) to illustrate key relationships within your data
- Understand the difference between the Builder Panel vs. Styling Panel 
- Create a set of basic calculations
- Include Chart Add-ons, such as a Variance

Continue to - [Exercise 2 - Integrating Planning into a Business Intelligence Story](../ex2/README.md)

