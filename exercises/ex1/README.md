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

![image](https://user-images.githubusercontent.com/112718519/197618454-663a2604-6d6e-482c-b642-00b5db211192.png)

🚩 We can see that based on the current design of the dashboard, the Table and Currency Selection (Measure Input Control) takes up the entire dashboard. Let's resize a few widgets to make room for some additional visualizations that we want to create.

2. Scroll to the **bottom of the dashboard**
3. Cick an **hold** the bottom right resize icon of the Table

![image](https://user-images.githubusercontent.com/112718519/197618514-dd7755d3-cc25-4564-9327-8755ee61c661.png)

4. Resize the Table until it just fits all the Accounts

![image](https://user-images.githubusercontent.com/112718519/197618719-43f9b390-62a1-40bd-b398-b0d94fcc8ca7.png)

5. Click and hold the bottom right resize icon for the Currency Selection Input Control

![image](https://user-images.githubusercontent.com/112718519/197618589-7e4855fa-9bfb-40d6-bfff-255d3fceef3b.png)

6. Resize the Currency Selection Input Control so that it has the same height as the Table

![image](https://user-images.githubusercontent.com/112718519/197618626-1992e4a5-02f7-4368-81e8-dcacc83994f9.png)

⚠️**Quality Check!**
Does your Table and Currency Selection Input Control look like this?

![image](https://user-images.githubusercontent.com/112718519/197619011-916979d4-4ed4-413a-84b3-e025d8b47e10.png)

🚩 Now that we have room on our dashboards, let's create our first visualization. We want to provide our colleagues a better understanding of the Gross Profit per Product.
 
Let's insert a Chart to visualize this information.

7. In the toolbar click on the Chart icon

![image](https://user-images.githubusercontent.com/112718519/197619063-09705a2c-7aad-4a19-8639-ff374c068cbc.png)

ℹ️ Welcome to the Builder Panel!

The Builder Panel is a place where you can create your visualizations by specifying elements of a visualization such as accounts, measures, dimensions, filters and so on. The Builder Panel will dynamically update depending on the Data Model and the type of visualization that you are creating. 
 
For this Chart, we are using SAP_XPA_FINANCE, which is a New Model type. The Chart requires at least one Account and at least one Measure to be selected from the Builder Panel. 

![image](https://user-images.githubusercontent.com/112718519/197619076-27a85402-48e5-4dc1-bc60-c2b06fca7387.png)

8. Click + At least 1 Account required

![image](https://user-images.githubusercontent.com/112718519/197619103-c342ed13-49cc-43bb-90f6-02557aa1b7d3.png)

9. Click on the arrow beside Operating Income to expand the Account
10. Click on Gross Profit
11. Click anywhere outside the Account selection drop down menu to collapse it 

![image](https://user-images.githubusercontent.com/112718519/197619116-a90dd2fa-85c4-4f47-b949-f39ba9f4f363.png)

12. Click + At least 1 Measure required

![image](https://user-images.githubusercontent.com/112718519/197619158-234a75bf-9157-418d-9203-5e62599d8856.png)

13. Click Currency Selection
14. Click anywhere outside the Measure selection drop down menu to collapse it 

![image](https://user-images.githubusercontent.com/112718519/197619167-2c62e4ad-a72e-45e3-8573-4f1425b87223.png)

🚩 We can now see data for our Gross Profit as we've successfully met the minimum conditions to view data for our Bar / Column Chart. Let's now add our Product dimension to see the breakdown per Product.

![image](https://user-images.githubusercontent.com/112718519/197633398-29c382fb-9e11-4234-9bdd-7ac5be668fc5.png)

15. Click +Add Dimension

![image](https://user-images.githubusercontent.com/112718519/197619199-ecae15ce-6dd2-4bec-84e5-10f65ffd3513.png)

16. Click SAP_XPA_PRODUCT
17. Click anywhere outside the Dimension selection drop down menu to collapse it

![image](https://user-images.githubusercontent.com/112718519/197619234-0a8574d9-7a72-4df1-b19d-dd6c18a0d3aa.png)

🚩 We can now see data for our Gross Profit per Product. However, as Product is a hierarchial dimension, we want to drill down into the Product Dimension so that we can see a more detailed view of our Gross Profit. 

![image](https://user-images.githubusercontent.com/112718519/197633436-c1b80d44-7d2c-432a-97cb-493cc2b43c9b.png)

18. Within the Builder Panel click the drill icon in the SAP_XPA_Product Dimension
19. Click on Level 2

![image](https://user-images.githubusercontent.com/112718519/197619292-a9c2159e-cb6f-43cb-8856-2cfdad9c0bde.png)

🚩 We can now see data for our Gross Profit per Product. Based on this breakdown we can see that Youth Bikes bring us the most Gross Profit in comparison to any other product that we offer.

Let's resize and reposition the visualization for better readability. 

20. Scroll to the right of the dashboard
21. Click and hold the border of the chart to move the object

![image](https://user-images.githubusercontent.com/112718519/197629130-8797e878-0285-4ce3-a46f-4d81c743b636.png)

22. Move the Chart to align it with the top of the Table

![image](https://user-images.githubusercontent.com/112718519/197629215-5058ecdb-822d-4487-a356-d291b136a39b.png)

23. Click and hold the bottom right resize icon for the Chart

![image](https://user-images.githubusercontent.com/112718519/197629286-402df8f0-f0f4-4e5b-b1cd-208bb6619dd1.png)

24. Resize the Chart to align it with the table and the edge of the shape header

![image](https://user-images.githubusercontent.com/112718519/197629395-c6630f32-7857-47fe-9e94-13649fa31c87.png)

⚠️**Quality Check!**
Does your dashboard look like this?

**IMAGE**

🚩 Now, the Chart only shows actual Gross Profit. We want the Chart to show actual Gross Profit versus planned Gross Profit. We will add planned Gross Profit into the Chart by adding an additional Dimension. 

25. Scroll to the bottom of the Builder Panel
26. Click + Add Dimension/Account

![image](https://user-images.githubusercontent.com/112718519/197629674-bc76455f-095f-40db-a0b8-65e95fd16402.png)

27. Click Version

![image](https://user-images.githubusercontent.com/112718519/197629699-f4bc5c08-6377-4435-9e0b-c41b1fc77d5c.png)

ℹ️ International Business Communication Standards (IBCS)

The color of the Chart is now changed to black for actual Gross Profit. This is because SAP Analytics Cloud is following International Business Communication Standards (IBCS), so we are coloring the bars based on the color of the Version that is added to the Chart. Now that we have actual Gross Profit in your Chart, we want to add planned Gross Profit.

**IMAGE**

28. Click + Add Verion

![image](https://user-images.githubusercontent.com/112718519/197629736-b2d67db7-cc95-4772-856c-00cc74fbc275.png)

29. Click 22 Plan
30. Click on a spot outside the Version selection dropdown menu to collapse it

![image](https://user-images.githubusercontent.com/112718519/197629879-7aeae2a3-99d9-43fb-84aa-4a8c10f4258e.png)

🚩 We can see the difference between our Plan 22 and Actuals. However, we want a better visual representation of this data. Hence, lets add a variance to show the difference between Actual and 22 Plan.

31.	Click the expand icon for Chart Add-ons
32.	Scroll to the bottom of the Builder Panel
33.	Click Variance

![image](https://user-images.githubusercontent.com/112718519/197629918-621777df-166e-4a8c-8be4-dbc76093d960.png)

34. Click + Add Version/Time

![image](https://user-images.githubusercontent.com/112718519/197629994-ec040816-36f2-4003-abf9-d6a6d46f49dd.png)

35. Click Version

![image](https://user-images.githubusercontent.com/112718519/197630189-ffbc8eab-f284-4c8b-b0a6-ac0c248a4634.png)

36.	For Compare (A), click the expand icon for Version
37.	Click Actual

![image](https://user-images.githubusercontent.com/112718519/197630227-733d1396-820f-4509-bb55-e42d26f146db.png)

38.	For To (B), click the expand icon for Version
39.	Click 22 Plan

![image](https://user-images.githubusercontent.com/112718519/197630259-c97f3461-f460-4633-b95f-d1375b0da9f5.png)

40.	Click Data Label
41.	Scroll to the bottom of the Variance Panel
42.	Click Both
43.	Click  the expand icon for Number
44.	Click 1

![image](https://user-images.githubusercontent.com/112718519/197630308-29086c92-50e8-4206-9ceb-4231de056880.png)

45.	Click expand for Percentage
46.	Click 1
47.	Click Done

![image](https://user-images.githubusercontent.com/112718519/197630320-32c4fc63-9264-452f-b1c9-63d8ee4c8b77.png)

⚠️**Quality Check!**
Does you Chart look like this?

**IMAGE**

## Summary

**You have completed the entire Understanding the Basics of SAP Analytics Cloud Stories section!**

**You are now able to:**
- Create a set of visualizations (i.e. Chart, Geo, and Table) to illustrate key relationships within your data
- Understand the difference between the Builder Panel vs. Styling Panel 
- Create a set of basic calculations
- Include Chart Add-ons, such as a Variance

Continue to - [Exercise 2 - Integrating Planning into a Business Intelligence Story](../ex2/README.md)

