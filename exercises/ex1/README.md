# Exercise 1 – Understanding the Basics of SAP Analytics Cloud Stories

**Objective:** You should develop a basic understanding on how to create visualizations within SAP Analytics Coud. 

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
3. Cick and **hold** the bottom right resize icon of the Table

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

8. Click **+ At least 1 Account required**

![image](https://user-images.githubusercontent.com/112718519/197619103-c342ed13-49cc-43bb-90f6-02557aa1b7d3.png)

9. Click on the arrow beside Operating Income to expand the Account
10. Click on **Gross Profit**
11. Click anywhere outside the Account selection drop down menu to collapse it 

![image](https://user-images.githubusercontent.com/112718519/197619116-a90dd2fa-85c4-4f47-b949-f39ba9f4f363.png)

12. Click **+ At least 1 Measure required**

![image](https://user-images.githubusercontent.com/112718519/197619158-234a75bf-9157-418d-9203-5e62599d8856.png)

13. Click **Currency Selection**
14. Click anywhere outside the Measure selection drop down menu to collapse it 

![image](https://user-images.githubusercontent.com/112718519/197619167-2c62e4ad-a72e-45e3-8573-4f1425b87223.png)

🚩 We can now see data for our Gross Profit as we've successfully met the minimum conditions to view data for our Bar / Column Chart. Let's now add our Product dimension to see the breakdown per Product.

![image](https://user-images.githubusercontent.com/112718519/197633398-29c382fb-9e11-4234-9bdd-7ac5be668fc5.png)

15. Click **+ Add Dimension**

![image](https://user-images.githubusercontent.com/112718519/197619199-ecae15ce-6dd2-4bec-84e5-10f65ffd3513.png)

16. Click **SAP_XPA_PRODUCT**
17. Click anywhere outside the Dimension selection drop down menu to collapse it

![image](https://user-images.githubusercontent.com/112718519/197619234-0a8574d9-7a72-4df1-b19d-dd6c18a0d3aa.png)

🚩 We can now see data for our Gross Profit per Product. However, as Product is a hierarchial dimension, we want to drill down into the Product Dimension so that we can see a more detailed view of our Gross Profit. 

![image](https://user-images.githubusercontent.com/112718519/197633436-c1b80d44-7d2c-432a-97cb-493cc2b43c9b.png)

18. Within the Builder Panel click the **Drill** icon in the SAP_XPA_Product Dimension
19. Click on **Level 2**

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
26. Click **+ Add Dimension/Account**

![image](https://user-images.githubusercontent.com/112718519/197629674-bc76455f-095f-40db-a0b8-65e95fd16402.png)

27. Click **Version**

![image](https://user-images.githubusercontent.com/112718519/197629699-f4bc5c08-6377-4435-9e0b-c41b1fc77d5c.png)

ℹ️ International Business Communication Standards (IBCS)

The color of the Chart is now changed to black for actual Gross Profit. This is because SAP Analytics Cloud is following International Business Communication Standards (IBCS), so we are coloring the bars based on the color of the Version that is added to the Chart. Now that we have actual Gross Profit in your Chart, we want to add planned Gross Profit.

**IMAGE**

28. Click **+ Add Verion**

![image](https://user-images.githubusercontent.com/112718519/197629736-b2d67db7-cc95-4772-856c-00cc74fbc275.png)

29. Click **22 Plan**
30. Click on a spot outside the Version selection dropdown menu to collapse it

![image](https://user-images.githubusercontent.com/112718519/197629879-7aeae2a3-99d9-43fb-84aa-4a8c10f4258e.png)

🚩 We can see the difference between our Plan 22 and Actuals. However, we want a better visual representation of this data. Hence, lets add a variance to show the difference between Actual and 22 Plan.

31.	Click the **expand** icon for Chart Add-ons
32.	Scroll to the bottom of the Builder Panel
33.	Click **Variance**

![image](https://user-images.githubusercontent.com/112718519/197629918-621777df-166e-4a8c-8be4-dbc76093d960.png)

34. Click **+ Add Version/Time**

![image](https://user-images.githubusercontent.com/112718519/197629994-ec040816-36f2-4003-abf9-d6a6d46f49dd.png)

35. Click **Version**

![image](https://user-images.githubusercontent.com/112718519/197630189-ffbc8eab-f284-4c8b-b0a6-ac0c248a4634.png)

36.	For Compare (A), click the **expand** icon for Version
37.	Click **Actual**

![image](https://user-images.githubusercontent.com/112718519/197630227-733d1396-820f-4509-bb55-e42d26f146db.png)

38.	For To (B), click the **expand** icon for Version
39.	Click **22 Plan**

![image](https://user-images.githubusercontent.com/112718519/197630259-c97f3461-f460-4633-b95f-d1375b0da9f5.png)

40.	Click **Data Label**
41.	Scroll to the bottom of the Variance Panel
42.	Click **Both**
43.	Click  the **expand** icon for Number
44.	Click **1**

![image](https://user-images.githubusercontent.com/112718519/197630308-29086c92-50e8-4206-9ceb-4231de056880.png)

45.	Click **expand** for Percentage
46.	Click **1**
47.	Click **Done**

![image](https://user-images.githubusercontent.com/112718519/197630320-32c4fc63-9264-452f-b1c9-63d8ee4c8b77.png)

⚠️**Quality Check!**
Does you Chart look like this?

**IMAGE**

🚩 We now have a good representation of some key figures when it comes to our financial data. Now, lets incorporate some Headcount data into our dashboard to provide our management team a holistic view of the business. 

48.	In the toolbar, click on the **Chart** icon

![image](https://user-images.githubusercontent.com/112718519/197639226-f0f12495-5a0f-4316-9d0a-63cccf5da2e6.png)

49. Click and hold the border of the chart to move the object and position it to align with the Currecy Selection Input Control.

![image](https://user-images.githubusercontent.com/112718519/197639283-0b35c35f-5c21-48a2-81c6-f67733e4afab.png)

50.	Cick and hold the bottom right resize icon of the Chart

![image](https://user-images.githubusercontent.com/112718519/197639310-21d74e50-f4d3-4499-970e-1aa7bca67722.png)

51.	Resize the Chart so that its width is slightly smaller than the Table above

![image](https://user-images.githubusercontent.com/112718519/197639333-43038748-7669-4196-8ae3-c513d41b9942.png)

⚠️**Quality Check!**
Does you Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/197639350-858e6521-9fe8-4ecc-9749-6aa723c84ad6.png)

🚩 We can see that the current data model that is being used in the Chart is SAP_XPA_FINANCE. In order to incorporate Headcount data into the Chart, you will need to change the Data Model for this Chart. 

52. Click on the **Data Model** icon 
![image](https://user-images.githubusercontent.com/112718519/197639376-f57ee6c8-93ee-4cff-9f82-b875d7ea01fc.png)

53. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/197639527-b67ce87a-793d-48e0-ba58-352a25ff59a3.png)

54. Click **Select other model...**

![image](https://user-images.githubusercontent.com/112718519/197639594-3755f6f9-3550-4f5f-80a6-c18ae0692945.png)

55. In the Search field, type **SAP_XPA_HEADCOUNT**
56. Click **SAP_XPA_HEADCOUNT**
 
![image](https://user-images.githubusercontent.com/112718519/197639648-e992112a-a376-44c4-a085-e4df8cdfaacc.png)

🚩 After selecting the Headcount Data Model, the Builder Panel automatically updates the name of the Data Model. For the Headcount Data Model, it is a Classic Account Model instead of a New Model that we saw for the Finance Data Model. Therefore, the Builder Panel is updated to reflect how Account is the only requirement for the Classic Account Model. 

You are not too familiar with the Headcount Data Model and you want to see a list of Accounts and Dimensions that are available to insert into the Chart. In the top right of the Builder Panel, click Available Objects.

57.	Click **Available Objects**

![image](https://user-images.githubusercontent.com/112718519/197639673-5a8b5110-e372-4791-a6a5-2d7f2e026fad.png)

ℹ️ Welcome to the Available Objects!

It provides you a hollistic view of all the data related objects that are associated to the data model. It provides you an ability to quickly drag an drop objects into the Builder Panel or use any of the quick action menus to bind the data.

![image](https://user-images.githubusercontent.com/112718519/197639771-4ade8c48-bff3-42ca-a676-2e6c4135b01a.png)

🚩 Based on the data that is available within this data model, we are interested in building a trend over time that represents our headcount.

58. Click on the **more action** icon for Headcount
59. Click **Add to Accounts**

![image](https://user-images.githubusercontent.com/112718519/197640032-20084fbb-c2c9-474a-a135-18905f1b42c9.png)

60. Click on the search bar and type **Hire**
61. Click on the **more action** icon for SAP_XPA_HIRE_DATE
62. Click on **Add to Dimensions**

![image](https://user-images.githubusercontent.com/112718519/197640064-4bd24b89-408d-4735-9ed0-e3d125ec70cf.png)

⚠️**Quality Check!**
Does you Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/197640088-d38d455f-4f66-4ff1-a528-af20b713ecef.png)

🚩 Based on the data type that you added into the Chart, SAP Analytics Cloud will automatically change the Chart Orientation to best represent the data. Since you added a time-based Dimension into the Chart, the Chart orientation is automatically vertical.

Let's drill into the visualization to see the data context per quarter.

63.	Click on the bar that represents (all)
64.	Click on the **Drill Down** icon

![image](https://user-images.githubusercontent.com/112718519/197640284-b7a10a12-5f3c-4168-b576-58ec8daf4dc2.png)

65.	Within the Builder Panel click on the **Drill** icon for SAP_XPA_HIRE_DATE
66.	Click **Level 3**

⚠️**Quality Check!**
Does you Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/197640353-d4d87796-5bca-4780-8a64-28bd64644a5a.png)

🚩 Now, you are interested in adding a variance to see the difference in Headcount between the current quarter and the previous quarter.

67.	Scroll to the bottom of the Builder Panel
68.	Click **expand** for the Chart Add-ons
69.	Click **Variance**

![image](https://user-images.githubusercontent.com/112718519/197640425-1205215c-7cec-4304-8b20-2ff79927d47c.png)

70.	Click **+ Add Version/Time**

![image](https://user-images.githubusercontent.com/112718519/197640436-0361fbd4-6390-4d49-a8a6-4a0f5075ad58.png)

71.	Click **SAP_XPA_HIRE_DATE**

![image](https://user-images.githubusercontent.com/112718519/197640458-4c33d15a-e2fe-4d6e-8f12-5c5dc19f7df3.png)

72.	Click **Integrated**
73.	Click **Done**

![image](https://user-images.githubusercontent.com/112718519/197640476-17c437de-f92e-41df-944d-b8fb9a5ce2df.png)

74.	Click **X** to close the Available Objects List

![image](https://user-images.githubusercontent.com/112718519/197640498-0b1a71f7-5fa0-40dd-98dd-7498e0a82cbd.png)

⚠️**Quality Check!**
Does you Chart look like this?

**IMAGE**

🚩 We now want to add a Geographical representation of where are hires are per location. It would also be a good idea for us to better understanding the various career levels that we have by headcount per location.

Let's add a new Geo Visualization. 

75.	Click the **Add** icon
76.	Click **Geo Map** in the Others section

![image](https://user-images.githubusercontent.com/112718519/197651430-681ae30e-6ef5-4b69-b5e7-35f3a6c0c55c.png)

77.	Click and hold the border of the Geo Widget to move the object
 
![image](https://user-images.githubusercontent.com/112718519/197651444-1bb5fba9-37b1-445a-a400-b7b93158fb3a.png)

78.	Move the Geo Widget to align it with the top of the Chart
 
![image](https://user-images.githubusercontent.com/112718519/197651455-c4a25dfb-ca01-4fa2-9200-b6499266e9c7.png)

79.	Resize the Geo to align it with the Chart above and the edge of the shape header
 
![image](https://user-images.githubusercontent.com/112718519/197651478-ea1b89ab-bc35-4933-9609-89e71280872c.png)

⚠️**Quality Check!**
Does you Geo Visualization look like this?

![image](https://user-images.githubusercontent.com/112718519/197651509-2c6132aa-6ff8-4d42-be0b-d4cdad03c3c2.png)

🚩 We want to change the Base Layer Style to better match the theme of the rest of the dashboard. 

80.	Click Light Gray to open the dropdown menu to see other Base Layer Styles.
81.	Click **Transparent Dark Gray**
 
![image](https://user-images.githubusercontent.com/112718519/197651540-26b1e3c6-d184-4d83-a1af-14f0bb0c22d7.png)

82.	Click **+ Add Layer**

![image](https://user-images.githubusercontent.com/112718519/197651622-6dacd766-ee45-480f-89c9-244eced27500.png)

83.	Click **+ Location Dimension required**

![image](https://user-images.githubusercontent.com/112718519/197651643-81a3b138-39bc-4c45-a02e-27d9cd7f3176.png)

ℹ️ Location Clustering in Geo Visualization!
Adding a Location Dimension will determine whether or not Location Clustering in the Builder Panel will continue to be turned on or automatically turned off. It will be turned off if you have less than 5000 data points. 

84.	Click **Hire_Location**

![image](https://user-images.githubusercontent.com/112718519/197651670-401b1d7a-0b4b-4855-b570-d0c99b99da30.png)

🚩 We can now see data points for all our hire locations. Let's add Headcount and Career Level as the size and color respectively to further drill down into our data. 

85.	Under Bubble Size click **Add Account**

![image](https://user-images.githubusercontent.com/112718519/197651685-9a6cea5e-9e8e-4727-b951-985fc00ca607.png)

86.	Click **Headcount**

![image](https://user-images.githubusercontent.com/112718519/197651717-65de588f-1211-4303-a50e-5974d189e88c.png)

87.	Under Bubble Color click **Add Dimension/Account**

![image](https://user-images.githubusercontent.com/112718519/197651734-d92cbc4b-715d-47a0-8163-7f9e01b9314d.png)

88.	Click **SAP_XPA_CAREER_LEVEL**

![image](https://user-images.githubusercontent.com/112718519/197651746-3cdb2fcd-3905-4924-a6f4-78e36d137319.png)

89.	Rename the Layer Name to **Headcount by Career Level**
90.	Click **Done**

![image](https://user-images.githubusercontent.com/112718519/197651752-03cf8ae8-f78e-4835-864c-f9dd7d2d1338.png)

⚠️**Quality Check!**
Does you Geo Visualization look like this?

![image](https://user-images.githubusercontent.com/112718519/197651790-fddf611c-7149-4a0a-8b15-7d208bb4bd1a.png)

## Summary

**You have completed the entire Understanding the Basics of SAP Analytics Cloud Stories section!**

**You are now able to:**
- Create a set of visualizations (i.e. Chart, Geo, and Table) to illustrate key relationships within your data
- Understand the difference between the Builder Panel vs. Styling Panel 
- Create a set of basic calculations
- Include Chart Add-ons, such as a Variance

Continue to - [Exercise 2 - Integrating Planning into a Business Intelligence Story](../ex2/README.md)

