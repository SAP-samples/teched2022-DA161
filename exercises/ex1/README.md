# Exercise 1 – Understanding the Basics of SAP Analytics Cloud Stories

**Objective:** You should develop a basic understanding on how to create visualizations within SAP Analytics Cloud. 

**Estimated Time:** 25 mins

**Exercise Description:** You and a colleague are building a dashboard for the upcoming board meeting. As a starting point, your colleague has incorporated some Financial Planning Data into the dashboard. You want to further enhance the dashboard to better represent some KPIs while including HR data to get a better understanding on the end-to-end business operations as TCS Technologies. 

**Key Features:**
- Create a set of visualizations (i.e. Chart, Geo, and Table) to illustrate key relationships within your data
- Understand the Builder Panel vs. Styling Panel 
- Learn how to create some calculations

⚠️**Disclaimer**
When completing exercises, some data values or sceenshots may not match what you see on your sceen. It is because the current exercise is based on a feature that is currently in BETA. 

----------------------------------------------------------------------------------------------------------------------------------------

🚩 Before we get started, refer to the Getting Started section to find the starting dashboard for this exercise and create a copy of the starting dashboard. 

🚩As a Business Analyst for TCS Technologies, we are interested in creating a dashboard that incorporates Business Intelligence, Planning, and Scripting. As a starting point, you want to enhance the dashboard that your colleague has started by incorporating HR data. 
 
Lets start by editing the dashboard!

1. Click **Edit**

![image](https://user-images.githubusercontent.com/112718519/197618454-663a2604-6d6e-482c-b642-00b5db211192.png)

🚩 We can see that based on the current design of the dashboard, the Table and Currency Selection (Measure Input Control) takes up the entire dashboard. Let's resize a few widgets to make room for some additional visualizations that we want to create.

2. Scroll to the **bottom of the dashboard**
3. Click and **hold** the resize icon in the bottom right of the Table 

![image](https://user-images.githubusercontent.com/112718519/197618514-dd7755d3-cc25-4564-9327-8755ee61c661.png)

4. Resize the Table until it just fits all the Accounts

![image](https://user-images.githubusercontent.com/112718519/197618719-43f9b390-62a1-40bd-b398-b0d94fcc8ca7.png)

5. Click and hold the resize icon in the bottom right of the Currency Selection Input Control

![image](https://user-images.githubusercontent.com/112718519/197618589-7e4855fa-9bfb-40d6-bfff-255d3fceef3b.png)

6. Resize the Currency Selection Input Control so that it has the same height as the Table

![image](https://user-images.githubusercontent.com/112718519/197618626-1992e4a5-02f7-4368-81e8-dcacc83994f9.png)

⚠️**Quality Check!**
Does your Table and Currency Selection Input Control look like this?

![image](https://user-images.githubusercontent.com/112718519/197619011-916979d4-4ed4-413a-84b3-e025d8b47e10.png)

🚩 Now that we have room on our dashboards, let's create our first visualization. We want to provide our colleagues a better understanding of the Gross Profit per Product.
 
Let's insert a Chart to visualize this information.

7. In the toolbar, click on the **Chart** icon

![image](https://user-images.githubusercontent.com/112718519/197619063-09705a2c-7aad-4a19-8639-ff374c068cbc.png)

ℹ️ Welcome to the Builder Panel!

The Builder Panel is a place where you can create your visualizations by specifying elements of a visualization such as accounts, measures, dimensions, filters and so on. The Builder Panel will dynamically update depending on the Data Model and the type of visualization that you are creating. 
 
For this Chart, we are using SAP_XPA_FINANCE, which is a New Model type. The Chart requires at least one Account and at least one Measure to be selected from the Builder Panel. 

![image](https://user-images.githubusercontent.com/112718519/197619076-27a85402-48e5-4dc1-bc60-c2b06fca7387.png)

🚩 We can see that the current data model that is being used in the Chart is SAP_XPA_HEADCOUNT. In order to incorporate financial data into the Chart, you will need to change the Data Model for this Chart.

8. Click on the **Data Model** icon

![image](https://user-images.githubusercontent.com/112718519/199082435-196fb5e5-e9a1-401a-b0d4-b61e78d9be4b.png)

9. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199082639-86f8f983-4107-42cf-a3ad-34a40bd749e9.png)

10. Click **SAP_XPA_FINANCE**

![image](https://user-images.githubusercontent.com/112718519/199082690-5b325dbd-9107-4323-86ef-a39a0fae62a2.png)

11. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199082747-349edbdf-3949-43d1-b108-0826d238ae80.png)

🚩 After selecting the Finance Data Model, the Builder Panel automatically updates the name of the Data Model.

12. Click **+ At least 1 Account required**

![image](https://user-images.githubusercontent.com/112718519/199083035-638c0472-f146-4ad8-8ff3-4b39f12501f8.png)

13. Click on the arrow beside Finance to expand the Account
14. Click on the arrow beside Operating Income to expand the Account
15. Click on **Gross Profit**
16. Click anywhere outside the Account selection drop down menu to collapse it 

![image](https://user-images.githubusercontent.com/112718519/199083860-4b4fe42e-e30c-4d16-ba7a-89e54192ae0a.png)

17. Click **+ At least 1 Measure required**

![image](https://user-images.githubusercontent.com/112718519/199084027-73fb187b-2b7a-4c81-8bc3-b02479031688.png)

18. Click **Reporting Currency**
19. Click on a spot outside the Measures selection dropdown menu to collapse it

![image](https://user-images.githubusercontent.com/112718519/199084112-834e7f1f-84d8-4d26-9080-7501e08238c4.png)

🚩 We can now see data for our Gross Profit as we've successfully met the minimum conditions to view data for our Bar / Column Chart. Let's now add our Product dimension to see the breakdown per Product.

![image](https://user-images.githubusercontent.com/112718519/199090847-2086b1c8-d2ab-404e-af37-2d47fbb05e28.png)

20. Click **+ Add Dimension**

![image](https://user-images.githubusercontent.com/112718519/199084155-488f00af-059f-43d5-a316-77fccd115369.png)

21. Click **SAP_XPA_PRODUCT**
22. Click anywhere outside the Dimension selection drop down menu to collapse it

![image](https://user-images.githubusercontent.com/112718519/199084307-0511fa19-fbed-4aac-b785-436c935ab24c.png)

🚩 However, as Product is a hierarchial dimension, we want to drill down into the Product Dimension so that we can see a more detailed view of our Gross Profit.

23. Let's try drilling via the Builder Panel. Click the **Drill** icon in the SAP_XPA_Product Dimension. 
24. Click on **Level 2**
 
![image](https://user-images.githubusercontent.com/112718519/199084418-1e53b310-cb01-47b8-9475-d87c7cd71e27.png)

🚩 We can now see data for our Gross Profit per Product. Based on this breakdown we can see that Youth Bikes bring us the most Gross Profit in comparison to any other product that we offer.

Let's resize and reposition the visualization for better readability.

25. Scroll to the right of the dashboard
26. Click and hold the border of the chart to move the object

![image](https://user-images.githubusercontent.com/112718519/199084713-506adc3a-4458-4e3f-9487-493d55983bb6.png)

27. Move the Chart to align it with the top of the Table

![image](https://user-images.githubusercontent.com/112718519/199084747-7a15f9e2-a1af-4f7d-9653-d73312682b4f.png)

28. Click and hold the bottom right resize icon for the Chart

![image](https://user-images.githubusercontent.com/112718519/199084767-061f2ba3-a5fa-447b-92f5-eceadf738e94.png)

29. Resize the Chart to align it with the table and the edge of the shape header

![image](https://user-images.githubusercontent.com/112718519/199084801-f22a6f5c-7d09-47d8-812e-6c1e0d83ae98.png)

⚠️**Quality Check!** Does your Table look like this?

![image](https://user-images.githubusercontent.com/112718519/199084983-c2ec7456-1ee8-44ec-878b-3d25fd05d4a2.png)

🚩 Now, the Chart only shows actual Gross Profit. We want the Chart to show actual Gross Profit versus planned Gross Profit. We will add planned Gross Profit into the Chart by adding an additional Dimension. 

30. Scroll to the bottom of the Builder Panel
31. Click + Add Dimension/Account

![image](https://user-images.githubusercontent.com/112718519/199084871-dfcc50ca-d295-4eaf-b9ed-95155ea4e262.png)

32. Click **Version** 

![image](https://user-images.githubusercontent.com/112718519/199084907-7d0f20e1-ceb6-4e11-8a77-9ed447057f57.png)

ℹ️ International Business Communication Standards (IBCS)

The color of the Chart is now changed to black for actual Gross Profit. This is because SAP Analytics Cloud is following International Business Communication Standards (IBCS), so we are coloring the bars based on the color of the Version that is added to the Chart. Now that we have actual Gross Profit in our Chart, we want to add planned Gross Profit.

![image](https://user-images.githubusercontent.com/112718519/199085107-7f786f12-a921-4752-806d-5ec9805b46b7.png)

33. Click **+ Add Version**

![image](https://user-images.githubusercontent.com/112718519/199086100-c68c2318-a762-4d2f-a0b0-9555fc0907fa.png)

34. Click **22 Plan**
35. Click on a spot outside the Version selection dropdown menu to collapse it

![image](https://user-images.githubusercontent.com/112718519/199086671-ee8c4845-eedb-41eb-a61d-1b66b6d5d1fc.png)

🚩 We can see the difference between our Plan 22 and Actuals. However, we want a better visual representation of this data. Hence, lets add a variance to show the difference between Actual and 22 Plan.

36. Click the **expand** icon for Chart Add-ons
37. Scroll to the bottom of the Builder Panel
38. Click **Variance**

![image](https://user-images.githubusercontent.com/112718519/199086727-0ef856cb-60ca-4871-bbb0-ca5d7a400142.png)

39. Click **+ Add Version/Time** 

![image](https://user-images.githubusercontent.com/112718519/199086853-778cb3d0-a5c7-4b61-8a3a-db688396313c.png)

40. Click **Version** 

![image](https://user-images.githubusercontent.com/112718519/199086881-dd229e5f-0438-405b-8952-1a22fb779e11.png)

41. For Compare (A), click the expand icon for Version
42. Click **Actual**

![image](https://user-images.githubusercontent.com/112718519/199086932-c923b43c-5539-4303-8564-ef98cb552d9a.png)

43. For To (B), click the expand icon for Version
44. Click **22 Plan**

![image](https://user-images.githubusercontent.com/112718519/199086982-582c0678-4192-47a1-9a1d-61064161d074.png)

45. Click **Data Label**
46. Scroll to the bottom of the Variance Panel
47. Click **Both**
48. Click  the **expand** icon for Number
49. Click **1**

![image](https://user-images.githubusercontent.com/112718519/199087096-836747fa-bff2-4591-a473-2814cf3041e6.png)

50.	Click the **expand** icon for Percentage
51.	Click **1**
52.	Click **Done**

![image](https://user-images.githubusercontent.com/112718519/199087239-bc0323c1-ef44-4ab5-9c97-42ca038227ff.png)

⚠️**Quality Check!** Does your Chart look like this? 

![image](https://user-images.githubusercontent.com/112718519/199088140-54dbbf15-be27-4980-ac08-b66953909993.png)

🚩 Press CTRL + S to save your story. 

🚩 We now have a good representation of some key figures when it comes to our financial data. Now, let's incorporate some Headcount data into our dashboard to provide our management team a holistic view of the business. 

53. In the toolbar, click on the **Chart** icon

![image](https://user-images.githubusercontent.com/112718519/199088216-92c1c4dc-6a91-457a-bfb1-d151616702ba.png)

54. Click and hold the border of the chart to move the object and position it to align with the Current Selection Input Control.

![image](https://user-images.githubusercontent.com/112718519/199088296-ac1b3238-1395-43ff-9541-88156b5026eb.png)

55. Click and hold the bottom right resize icon of the Chart

![image](https://user-images.githubusercontent.com/112718519/199088328-3dc57736-5f86-461a-b67c-d2fbb076418d.png)

56. Resize the Chart so that its width is slightly smaller than the Table above

![image](https://user-images.githubusercontent.com/112718519/199088390-f2a4f523-8e3a-4d39-8c6c-d63368346329.png)

⚠️**Quality Check!** Does you Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/199088488-cda40c1a-49f0-4f6f-aa1c-542b66dd1b53.png)

🚩 We can see that the current data model that is being used in the Chart is SAP_XPA_FINANCE. In order to incorporate Headcount data into the Chart, you will need to change the Data Model for this Chart. 

57. Click the **Data Model** icon

![image](https://user-images.githubusercontent.com/112718519/199088539-02519191-aab8-4c05-81d2-7eb4530080ab.png)

58. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199088565-dc4877cb-a110-432e-9dcf-48fca619c8a3.png)

59. Click on the arrow

![image](https://user-images.githubusercontent.com/112718519/199088592-fbe3c085-17cb-4e76-894c-ffb31b8b3720.png)

60. Click **SAP_XPA_HEADCOUNT**

![image](https://user-images.githubusercontent.com/112718519/199088651-e0119529-873d-41c2-8d4b-07a64e52ff1a.png)

61. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199088836-cf4bc429-06d5-44c0-b447-4785daf2bcea.png)

🚩 After selecting the Headcount Data Model, the Builder Panel automatically updates the name of the Data Model. For the Headcount Data Model, it is a Classic Account Model instead of a New Model that we saw for the Finance Data Model. Therefore, the Builder Panel is updated to reflect how Account is the only requirement for the Classic Account Model. 

You are not too familiar with the Headcount Data Model and you want to see a list of Accounts and Dimensions that are available to insert into the Chart. In the top right of the Builder Panel, click Available Objects.

62. Click **Available Objects** in the Builder Panel

![image](https://user-images.githubusercontent.com/112718519/199089493-f73a1984-91aa-4c6e-8bc0-46b8150dc7cb.png)

ℹ️ Welcome to the Available Objects!

It provides you a holistic view of all the data related objects that are associated to the data model. It provides you an ability to quickly drag and drop objects into the Builder Panel or use any of the quick action menus to bind the data.

![image](https://user-images.githubusercontent.com/112718519/197639771-4ade8c48-bff3-42ca-a676-2e6c4135b01a.png)

🚩 Based on the data that is available within this data model, we are interested in building a trend over time that represents our headcount.

63. Click on the **More** action icon for **Headcount**
64. Click Add to Accounts

![image](https://user-images.githubusercontent.com/112718519/199089622-bd8daa3d-0cfe-4dec-b2dc-bfd466b2fc0c.png)

65. Click on the search bar and type **Hire**
66. Click on the **More** action icon for **SAP_XPA_HIRE_DATE**
67. Click on **Add to Dimensions**

![image](https://user-images.githubusercontent.com/112718519/199089702-047c08f8-92a6-45f6-916e-3e64e9722ec4.png)

⚠️ **Quality Check!** Does your Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/199096258-d04003f1-5482-42b0-9b50-b2e8a6fccafd.png)

68. Click on the bar that represents (all)
69. Click on the **Drill Down** icon

![image](https://user-images.githubusercontent.com/112718519/199096284-6dc5e2ba-f375-473b-a579-4ed4d307f50e.png)

70. Within the Builder Panel, click on the **Drill icon** for SAP_XPA_HIRE_DATE
71. Click Level 3
 
⚠️ **Quality Check!** Does your Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/199096773-41a63215-f733-414e-ba4b-7446d9360af7.png)

72. Scroll to the bottom of the Builder Panel
73. Click **expand** for the Chart Add-ons
74. Click **Variance**

![image](https://user-images.githubusercontent.com/112718519/199096959-5512c6bd-661b-4d20-879b-3e2ccaf2addd.png)

75. Click **+ Add Version/Time**

![image](https://user-images.githubusercontent.com/112718519/199096995-812fecbf-b9ff-45a1-9994-bfd1cc9487c6.png)

76. Click **SAP_XPA_HIRE_DATE** 

![image](https://user-images.githubusercontent.com/112718519/199097115-516683d7-78fa-4289-8f6c-c2af9e946c80.png)

77. Click **Integrated**
78. Click **Done**

![image](https://user-images.githubusercontent.com/112718519/199097345-a7765684-db8e-4525-ad63-3cca7cffe889.png)

79. Click **X** to close the Available Objects List

![image](https://user-images.githubusercontent.com/112718519/199097372-eed75136-9f22-44a4-b3d3-87c2e6988538.png)

⚠️Quality Check! Does you Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/199097243-8231bf88-96c1-47ac-bc2a-6470a4b14326.png)

🚩 We now want to add a Geographical representation of where the hires are per location. It would also be a good idea for us to better understand the various career levels that we have by headcount per location.

80. Click the **Add** icon
81. Click **Geo Map** in the Others section

![image](https://user-images.githubusercontent.com/112718519/199097768-f0e6d75d-0ab6-4fb3-ad53-89e672c0202b.png)

82. Click and hold the border of the Geo Widget to move the object

![image](https://user-images.githubusercontent.com/112718519/199097798-ca88e52c-112b-4d83-8b7a-ab1c05b00782.png)

83. Move the Geo Widget to align it with the top of the Chart

![image](https://user-images.githubusercontent.com/112718519/199097983-798e5bc3-ada5-4f01-8562-f817032e2276.png)

84. Resize the Geo to align it with the Chart above and the edge of the shape header

![image](https://user-images.githubusercontent.com/112718519/199098010-f3ff1bce-4a11-4b67-9f05-c2c45ff8efe7.png)

🚩 We want to change the Base Layer Style to better match the theme of the rest of the dashboard.

85. Click Light Gray to open the dropdown menu to see other Base Layer Styles
86. Click Transparent Dark Gray

![image](https://user-images.githubusercontent.com/112718519/199098096-a330d3ff-f21b-400b-bd20-be2b6fcab90f.png)

87. Click **+ Add Layer**

![image](https://user-images.githubusercontent.com/112718519/199098867-3b0d07eb-8147-4d87-aca1-d482b0372f5f.png)

88. Click **+ Location Dimension required** 

![image](https://user-images.githubusercontent.com/112718519/199098894-9471c6fe-2c5b-4c81-958e-89ead8013ae3.png)

ℹ️ Location Clustering in Geo Visualization! Adding a Location Dimension will determine whether or not Location Clustering in the Builder Panel will continue to be turned on or automatically turned off. It will be turned off if you have less than 5000 data points.

![image](https://user-images.githubusercontent.com/112718519/199100086-05063724-aa3d-45e6-ad0e-fbcc8e0e708c.png)

89. Click **Hire_Location**

![image](https://user-images.githubusercontent.com/112718519/199098919-ced9425f-4a57-49b8-9710-bc58e97fe5f5.png)

🚩 We can now see data points for all our hire locations. Let's add Headcount and Career Level as the size and color respectively to further drill down into our data.

90. Under Bubble Size click **+ Add Account**

![image](https://user-images.githubusercontent.com/112718519/199098943-630c2bdb-29c1-4568-9546-a63c74cc25c2.png)

91. Click **Headcount**

![image](https://user-images.githubusercontent.com/112718519/199098965-59985f43-3578-412b-b7c4-af34d7b6cc52.png)

92. Under Bubble Color click **+ Add Dimension/Account**

![image](https://user-images.githubusercontent.com/112718519/199099006-ad23dc22-2f28-4b9c-b19d-2c85b81bebb5.png)

93. Click **SAP_XPA_CAREER_LEVEL**

![image](https://user-images.githubusercontent.com/112718519/199099021-7f1e2630-df69-4ea1-97c8-95b6250fa5e7.png)

94. Rename the Layer Name to **Headcount by Career Level**
95. Click **Done**

![image](https://user-images.githubusercontent.com/112718519/199099049-21ed45fd-b740-4384-b10c-e99ae4b49697.png)

⚠️ **Quality Check!** Does your Geo Visualization look like this?

![image](https://user-images.githubusercontent.com/112718519/199100172-356e447d-7660-4e5f-a8d8-255e0b4da34c.png)

🚩 Press CTRL + S to save your story. 

🚩 We are now intersted in adding another KPI to summary the Average Salary that we are paying our employees. To make it easier, lets duplicate the existing KPI so that we don't need to worry much about the formatting of the object.

96. Click on the **Numeric Point Chart Operating Income for 2022**
97. Click the **More** Action icon
98. Hover over **Copy** and select **Duplicate**

![image](https://user-images.githubusercontent.com/112718519/199100309-a8cd0d33-597f-4567-960a-5c4118eb89d3.png)

99. Move the object besides Operating Income for 2022
100. Click on the **Data Model** icon

![image](https://user-images.githubusercontent.com/112718519/199100640-da1e0ea5-3763-479c-a80c-1fd9e28124e4.png)

101. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199100769-b726a392-e805-4470-94b9-ecd4de4a537a.png)

102. Click **SAP_XPA_HEADCOUNT**

![image](https://user-images.githubusercontent.com/112718519/199100795-ad69a5a8-bb34-4219-939a-a52162da1603.png)

103. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199100815-87518b95-001e-4e56-8e7a-00025429fc57.png)

104. Click **+ At least 1 Account required** 

![image](https://user-images.githubusercontent.com/112718519/199100846-9b238a35-afe7-46c8-830a-6f5bc37331c5.png)

105. Click **Salary** 

![image](https://user-images.githubusercontent.com/112718519/199100984-d654d31c-8af6-4c7e-ac07-a9e07314ad51.png)

🚩 After clicking Salary, we realize that the KPI shows the total salary that was ever paid to employees. This KPI doesn't show Average Salary per Employee, which is what you want to see in the KPI.

Hence, we will have to create a calculation to reflect this metric.

106. Deselect **Salary** 
107. Click **Add Calculation** 

![image](https://user-images.githubusercontent.com/112718519/199101194-c9348080-a310-47ad-a5b6-4a71f43ddde1.png)

108. Click **Aggregation**

![image](https://user-images.githubusercontent.com/112718519/199101212-da3bd7e1-a3e6-4139-9611-3a3f9f431bd8.png)

109. Click the **Expand** icon for Operation
110. Scroll down till you see **Average**
111. Click **Average**

![image](https://user-images.githubusercontent.com/112718519/199101322-5089ff4b-b204-4783-bfb5-dfcef46f5c26.png)

112. Click the **Expand(( icon for Account
113. Click **Salary** 

![image](https://user-images.githubusercontent.com/112718519/199101402-73cdc80f-f344-42e5-b93c-3991fee823fb.png)

114. Click the Expand icon for Aggregation Dimensions
115. Click SAP_XPA_EMPLOYEE

![image](https://user-images.githubusercontent.com/112718519/199101446-34287f54-d020-43df-8147-062a599b06dd.png)

116. Rename the calculation to **Average Salary**
117. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199101477-79aa88f6-761d-4c83-b904-c69f85a9c519.png)

118. Rename the Title to **Average Salary**

![image](https://user-images.githubusercontent.com/112718519/199101614-c670d8e0-5e94-4d57-87fa-4ca4ff2c07fa.png)

119. Click the **More** Action icon
120. Hover over Show / Hide and deselect **Primary Value Labels**

![image](https://user-images.githubusercontent.com/112718519/199101715-05656fae-dc8d-4415-b84a-491c3762ae9f.png)

⚠️Quality Check! Does your Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/199101773-d37726c5-89e2-4bed-8682-aea048839bc1.png)

🚩 Press CTRL + S to save your story. 





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

23. Click and hold the resize icon in the bottom right of the Chart

![image](https://user-images.githubusercontent.com/112718519/197629286-402df8f0-f0f4-4e5b-b1cd-208bb6619dd1.png)

24. Resize the Chart to align it with the table and the edge of the shape header

![image](https://user-images.githubusercontent.com/112718519/197629395-c6630f32-7857-47fe-9e94-13649fa31c87.png)

⚠️**Quality Check!**
Does your dashboard look like this?

**IMAGE**

🚩 Now, the Chart only shows actual Gross Profit. We want the Chart to show actual Gross Profit versus planned Gross Profit. We will add planned Gross Profit into the Chart by adding an additional Dimension. 

25. Scroll to the bottom of the Builder Panel
26. Under Color, click **+ Add Dimension/Account**

![image](https://user-images.githubusercontent.com/112718519/197629674-bc76455f-095f-40db-a0b8-65e95fd16402.png)

27. Click **Version**

![image](https://user-images.githubusercontent.com/112718519/197629699-f4bc5c08-6377-4435-9e0b-c41b1fc77d5c.png)

ℹ️ International Business Communication Standards (IBCS)

The color of the Chart is now changed to black for actual Gross Profit. This is because SAP Analytics Cloud is following International Business Communication Standards (IBCS), so we are coloring the bars based on the color of the Version that is added to the Chart. Now that we have actual Gross Profit in our Chart, we want to add planned Gross Profit.

**IMAGE**

28. Click **+ Add Version**

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

45.	Click the **expand** icon for Percentage
46.	Click **1**
47.	Click **Done**

![image](https://user-images.githubusercontent.com/112718519/197630320-32c4fc63-9264-452f-b1c9-63d8ee4c8b77.png)

⚠️**Quality Check!**
Does you Chart look like this?

**IMAGE**

🚩 Press CTRL + S to save your story. 

🚩 We now have a good representation of some key figures when it comes to our financial data. Now, let's incorporate some Headcount data into our dashboard to provide our management team a holistic view of the business. 

48.	In the toolbar, click on the **Chart** icon

![image](https://user-images.githubusercontent.com/112718519/197639226-f0f12495-5a0f-4316-9d0a-63cccf5da2e6.png)

49. Click and hold the border of the chart to move the object and position it to align with the Currecy Selection Input Control.

![image](https://user-images.githubusercontent.com/112718519/197639283-0b35c35f-5c21-48a2-81c6-f67733e4afab.png)

50.	Click and hold the bottom right resize icon of the Chart

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

🚩 For the Headcount Data Model, it is a Classic Account Model instead of a New Model that we saw for the Finance Data Model. Therefore, the Builder Panel is updated to reflect how Account is the only requirement for the Classic Account Model. 

You are not too familiar with the Headcount Data Model and you want to see a list of Accounts and Dimensions that are available to insert into the Chart. In the top right of the Builder Panel, click Available Objects.

57.	Click **Available Objects**

![image](https://user-images.githubusercontent.com/112718519/197639673-5a8b5110-e372-4791-a6a5-2d7f2e026fad.png)

ℹ️ Welcome to the Available Objects!

It provides you a holistic view of all the data related objects that are associated to the data model. It provides you an ability to quickly drag and drop objects into the Builder Panel or use any of the quick action menus to bind the data.

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

🚩 Press CTRL + S to save your story.

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

🚩 We now want to add a Geographical representation of where the hires are per location. It would also be a good idea for us to better understand the various career levels that we have by headcount per location.

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
Does your Geo Visualization look like this?

![image](https://user-images.githubusercontent.com/112718519/197651509-2c6132aa-6ff8-4d42-be0b-d4cdad03c3c2.png)

🚩 We want to change the Base Layer Style to better match the theme of the rest of the dashboard. 

80.	Click Light Gray to open the dropdown menu to see other Base Layer Styles
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

85.	Under Bubble Size click **+ Add Account**

![image](https://user-images.githubusercontent.com/112718519/197651685-9a6cea5e-9e8e-4727-b951-985fc00ca607.png)

86.	Click **Headcount**

![image](https://user-images.githubusercontent.com/112718519/197651717-65de588f-1211-4303-a50e-5974d189e88c.png)

87.	Under Bubble Color click **+ Add Dimension/Account**

![image](https://user-images.githubusercontent.com/112718519/197651734-d92cbc4b-715d-47a0-8163-7f9e01b9314d.png)

88.	Click **SAP_XPA_CAREER_LEVEL**

![image](https://user-images.githubusercontent.com/112718519/197651746-3cdb2fcd-3905-4924-a6f4-78e36d137319.png)

89.	Rename the Layer Name to **Headcount by Career Level**
90.	Click **Done**

![image](https://user-images.githubusercontent.com/112718519/197651752-03cf8ae8-f78e-4835-864c-f9dd7d2d1338.png)

⚠️**Quality Check!**
Does your Geo Visualization look like this?

![image](https://user-images.githubusercontent.com/112718519/197651790-fddf611c-7149-4a0a-8b15-7d208bb4bd1a.png)

🚩 We are now intersted in adding another KPI to summary the Average Salary that we are paying our employees. To make it easier, lets duplicate the existing KPI so that we don't need to worry much about the formatting of the object.

91.	Click on the Numeric Point Chart Operating Income for 2022
92.	Click the More Action icon
93.	Hover over Copy and select Duplicate

![image](https://user-images.githubusercontent.com/112718519/198134777-a8f24e4d-692c-41dc-9829-2fc75c94a00b.png)

94.	Move the object besides Operating Income for 2022
95.	Click on the Change Datasource icon

![image](https://user-images.githubusercontent.com/112718519/198134799-d7525162-c38d-44ce-a64d-ffc9035bf676.png)

96.	Click OK

![image](https://user-images.githubusercontent.com/112718519/198134828-1af1f319-1f1e-4dd1-90e6-893cec347e14.png)

97.	Click SAP_XPA_HEADCOUNT

![image](https://user-images.githubusercontent.com/112718519/198134862-3bcde83f-5c5e-44c3-aa19-5faf698303ea.png)

98.	Click OK

![image](https://user-images.githubusercontent.com/112718519/198134886-14c56cdd-8f9c-4ecf-9bbf-7763bfb506a6.png)

99.	Click + At least 1 Account required 

![image](https://user-images.githubusercontent.com/112718519/198134928-0c31a693-f5cd-4aa0-b314-6abe81ecc86a.png)

100.	Click Salary

![image](https://user-images.githubusercontent.com/112718519/198134949-db43d7c2-069b-4219-b214-339835101bfb.png)

🚩 After clicking Salary, we realize that the KPI shows the total salary that was ever paid to employees. This KPI doesn't show Average Salary per Employee, which is what you want to see in the KPI. 

Hence, we will have to create a calculation to reflect this metric.

101.	Deselect Salary
102.	Click Add Calculation

![image](https://user-images.githubusercontent.com/112718519/198135127-c816ff4a-3b82-4b6c-8986-bc247a312b92.png)

103.	Click Aggregation

![image](https://user-images.githubusercontent.com/112718519/198135154-890a712f-3297-4368-b52d-90da0f282b11.png)

104.	Click the Expand icon for Operation
105.	Scroll down till you see Average
106.	Click Average

![image](https://user-images.githubusercontent.com/112718519/198135183-4d4ef538-2522-46ed-9c33-69a4ee0deecc.png)

107.	Click the Expand icon for Account
108.	Click Salary

![image](https://user-images.githubusercontent.com/112718519/198135227-5a37f0f2-a6f9-4675-9fe5-f7f1f401c697.png)

109.	Click the Expand icon for Aggregation Dimensions
110.	Click SAP_XPA_EMPLOYEE

![image](https://user-images.githubusercontent.com/112718519/198135262-c4a0003e-4c13-4d9c-9eae-bb5d43d78afe.png)

111.	Rename the Calculation to Average Salary
112.	Click OK

![image](https://user-images.githubusercontent.com/112718519/198135293-0ef114d1-b54a-43a4-82f1-53fa51c26779.png)

113.	Rename the Title to Average Salary

![image](https://user-images.githubusercontent.com/112718519/198135323-17b8e075-20bf-4e63-9792-a92bbdfe29bd.png)

114.	Click the More Action icon
115.	Hover over Show / Hide and deselect Primary Value Labels

![image](https://user-images.githubusercontent.com/112718519/198135358-76e85b1f-7ea4-47a3-b3cc-8dac2fa485c3.png)

⚠️**Quality Check!**
Does your Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/198135375-2586380f-b368-41ff-9f38-b285db98accd.png)

116.	Save your story with CTRL + S

## Summary

**You have completed the entire Understanding the Basics of SAP Analytics Cloud Stories section!**

**You are now able to:**
- Create a set of visualizations (i.e. Chart, Geo, and Table) to illustrate key relationships within your data
- Understand the difference between the Builder Panel vs. Styling Panel 
- Create a set of basic calculations
- Include Chart Add-ons, such as a Variance

Continue to - [Exercise 2 - Integrating Planning into a Business Intelligence Story](../ex2/README.md)

