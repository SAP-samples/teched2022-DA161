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
 
For this Chart, we want to use SAP_XPA_FINANCE as our data model, which is a New Model type. The Chart requires at least one Account and at least one Measure to be selected from the Builder Panel. 

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
26. Click and hold the border of the Chart to move the Chart to align it with the top of the Table

![image](https://user-images.githubusercontent.com/112718519/199610647-8bd43648-27e6-4df0-8c26-a02ca87a6cf2.png)

27. Click and hold the bottom right resize icon for the Chart. Resize the Chart to align it with the table and the edge of the shape header.

![image](https://user-images.githubusercontent.com/112718519/199610701-5adc12e5-a6b7-4a00-b8ba-67fa26a7ebf2.png)

⚠️**Quality Check!** Does your Table look like this?

![image](https://user-images.githubusercontent.com/112718519/199611034-2a0e24e6-acc4-492c-904f-909828d13b64.png)

🚩 Now, the Chart only shows actual Gross Profit. We want the Chart to show actual Gross Profit versus planned Gross Profit. We will add planned Gross Profit into the Chart by adding an additional Dimension. 

28. Scroll to the bottom of the Builder Panel
29. Click **+ Add Dimension/Account**

![image](https://user-images.githubusercontent.com/112718519/199611131-67425fa6-003d-46a3-bd88-2e2feb35ba21.png)

30. Click **Version** 

![image](https://user-images.githubusercontent.com/112718519/199611186-bf29c876-3372-478e-ba58-aa5d53d3fbb5.png)

ℹ️ International Business Communication Standards (IBCS)

The color of the Chart is now changed to black for actual Gross Profit. This is because SAP Analytics Cloud is following International Business Communication Standards (IBCS), so we are coloring the bars based on the color of the Version that is added to the Chart. Now that we have actual Gross Profit in our Chart, we want to add planned Gross Profit.

![image](https://user-images.githubusercontent.com/112718519/199611592-218dd603-191e-4e64-bd67-f84fb7920da2.png)

31. Click **+ Add Version**

![image](https://user-images.githubusercontent.com/112718519/199611769-3603796a-8c95-4f41-a52a-15a7cc9f3bbb.png)

32. Click **22 Plan**
33. Click on a spot outside the Version selection dropdown menu to collapse it

![image](https://user-images.githubusercontent.com/112718519/199611789-a6021b16-19f8-46c7-a289-3137e4ba6d70.png)

🚩 We can see the difference between our Plan 22 and Actuals. However, we want a better visual representation of this data. Hence, lets add a variance to show the difference between Actual and 22 Plan.

34. Click the **expand** icon for Chart Add-ons
35. Scroll to the bottom of the Builder Panel
36. Click **Variance**

![image](https://user-images.githubusercontent.com/112718519/199611830-72d07bdc-3f46-4640-ad7a-8d007dce9172.png)

37. Click **+ Add Version/Time** 

![image](https://user-images.githubusercontent.com/112718519/199611840-e89e3e4d-132b-40cf-b466-6a297795e7b6.png)

38. Click **Version** 

![image](https://user-images.githubusercontent.com/112718519/199611875-5bacc75b-bbd6-4ca9-9863-8d6f97f91d49.png)

39. For Compare (A), click the expand icon for Version
40. Click **Actual**

![image](https://user-images.githubusercontent.com/112718519/199611913-6f722657-7b05-46b5-8f4c-98be4b3e700c.png)

41. For To (B), click the expand icon for Version
42. Click **22 Plan**

![image](https://user-images.githubusercontent.com/112718519/199611942-1a3b4aef-23b8-4cfc-ba23-c306cd977115.png)

43. Click **Data Label**
44. Scroll to the bottom of the Variance Panel
45. Click **Both**
46. Click  the **expand** icon for Number
47. Click **1**

![image](https://user-images.githubusercontent.com/112718519/199611970-290172b3-b513-409f-8bea-193624b99567.png)

48.	Click the **expand** icon for Percentage
49.	Click **1**
50.	Click **Done**

![image](https://user-images.githubusercontent.com/112718519/199612015-08d7730e-df42-4c2b-b402-1395e3569de7.png)

⚠️**Quality Check!** Does your Chart look like this? 

![image](https://user-images.githubusercontent.com/112718519/199088140-54dbbf15-be27-4980-ac08-b66953909993.png)

🚩 Press CTRL + S to save your story. 

🚩 We now have a good representation of some key figures when it comes to our financial data. Now, let's incorporate some Headcount data into our dashboard to provide our management team a holistic view of the business. 

53. In the toolbar, click on the **Chart** icon

![image](https://user-images.githubusercontent.com/112718519/199088216-92c1c4dc-6a91-457a-bfb1-d151616702ba.png)

54. Click and hold the border of the chart to move the object and position it to align with the Reporting Currency Input Control.

![image](https://user-images.githubusercontent.com/112718519/199088296-ac1b3238-1395-43ff-9541-88156b5026eb.png)

55. Click and hold the bottom right resize icon of the Chart

![image](https://user-images.githubusercontent.com/112718519/199088328-3dc57736-5f86-461a-b67c-d2fbb076418d.png)

56. Resize the Chart so that its width is slightly smaller than the Table above

![image](https://user-images.githubusercontent.com/112718519/199088390-f2a4f523-8e3a-4d39-8c6c-d63368346329.png)

⚠️**Quality Check!** Does your Chart look like this?

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

89. Click **Hire_Location**

![image](https://user-images.githubusercontent.com/112718519/199098919-ced9425f-4a57-49b8-9710-bc58e97fe5f5.png)

ℹ️ Location Clustering in Geo Visualization! Adding a Location Dimension will determine whether or not Location Clustering in the Builder Panel will continue to be turned on or automatically turned off. It will be turned off if you have less than 5000 data points. In this example, Location Clustering is automatically turned off. 

![image](https://user-images.githubusercontent.com/112718519/199100086-05063724-aa3d-45e6-ad0e-fbcc8e0e708c.png)

🚩 We can now see data points for all our hire locations int the Geo Map. Let's add Headcount and Career Level as the size and color respectively to further drill down into our data.

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

🚩 We are now interested in adding another KPI to summarize the Average Salary that we are paying our employees. To make it easier, let's duplicate the existing KPI so that we don't need to worry much about the formatting of the object.

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

112. Click the **Expand** icon for Account
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

⚠️Quality Check! Does your KPI look like this?

![image](https://user-images.githubusercontent.com/112718519/199101773-d37726c5-89e2-4bed-8682-aea048839bc1.png)

🚩 Press CTRL + S to save your story. 



## Summary

**You have completed the entire Understanding the Basics of SAP Analytics Cloud Stories section!**

**You are now able to:**
- Create a set of visualizations (i.e. Chart, Geo, and Table) to illustrate key relationships within your data
- Understand the difference between the Builder Panel vs. Styling Panel 
- Create a set of basic calculations
- Include Chart Add-ons, such as a Variance

Continue to - [Exercise 2 - Integrating Planning into a Business Intelligence Story](../ex2/README.md)

