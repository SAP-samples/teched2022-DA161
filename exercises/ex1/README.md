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
Does your Table and Reporting Currency Input Control look like this?

![image](https://user-images.githubusercontent.com/112718519/199618487-073b1a5f-fa3c-48de-ba9f-a3106ade61fe.png)

🚩 Now that we have room on our dashboards, let's create our first visualization. We want to provide our colleagues a better understanding of the Gross Profit per Product.
 
Let's insert a Chart to visualize this information.

7. In the toolbar, click on the **Chart** icon

![image](https://user-images.githubusercontent.com/112718519/197619063-09705a2c-7aad-4a19-8639-ff374c068cbc.png)

ℹ️ Welcome to the Builder Panel!

The Builder Panel is a place where you can create your visualizations by specifying elements of a visualization such as accounts, measures, dimensions, filters and so on. The Builder Panel will dynamically update depending on the Data Model and the type of visualization that you are creating. 
 
For this Chart, we want to use SAP_XPA_FINANCE as our data model, which is a New Model type. The Chart requires at least one Account and at least one Measure to be selected from the Builder Panel. 

![image](https://user-images.githubusercontent.com/112718519/197619076-27a85402-48e5-4dc1-bc60-c2b06fca7387.png)

🚩 In the Builder Panel, we can see that the current data model that is being used in the Chart is SAP_XPA_HEADCOUNT. In order to incorporate financial data into the Chart, you will need to change the Data Model for this Chart.

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

![image](https://user-images.githubusercontent.com/112718519/199619015-fe52f2f1-c50f-43c6-b5da-605a8291f900.png)

20. Click **+ Add Dimension**

![image](https://user-images.githubusercontent.com/112718519/199084155-488f00af-059f-43d5-a316-77fccd115369.png)

21. Click **SAP_XPA_PRODUCT**
22. Click anywhere outside the Dimension selection drop down menu to collapse it

![image](https://user-images.githubusercontent.com/112718519/199084307-0511fa19-fbed-4aac-b785-436c935ab24c.png)

🚩 However, as Product is a hierarchial dimension, we want to drill down into the Product Dimension so that we can see a more detailed view of our Gross Profit.

23. Let's try drilling via the Builder Panel. Click the **Drill** icon in the SAP_XPA_Product Dimension. 
24. Click on **Level 2**
 
![image](https://user-images.githubusercontent.com/112718519/199084418-1e53b310-cb01-47b8-9475-d87c7cd71e27.png)

🚩 We can now see data for our Gross Profit per Product. Based on this breakdown, we can see that Youth Bikes bring us the most Gross Profit in comparison to any other product that we offer.

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

![image](https://user-images.githubusercontent.com/112718519/199612802-bc96fc93-3d8c-4c0f-82ce-bd5ea9c15fe9.png)

🚩 Press CTRL + S to save your story. 

🚩 To ensure that we are comparing 22 Plan with 22 Actual instead of Actual financial data for all years, let's add a filter so that we are setting a date range for 2022 values only.

51. Click **+ Add Filters**

![image](https://user-images.githubusercontent.com/112718519/199613739-f4aa042a-37f7-4841-8192-d405b182ef80.png)

52. Click **Date (Range)**

![image](https://user-images.githubusercontent.com/112718519/199613815-1e779afb-46ac-4cde-b43b-449690b65bc2.png)

53. Click the **toggle** to enable the ability to include range up to the current period

![image](https://user-images.githubusercontent.com/112718519/199614034-f482b8f0-7303-4e8a-95d4-1e256375c425.png)

54. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199614073-9d2b0cd3-1cc0-4fc6-95cc-fcde0928564d.png)

55. For Actual, click the icon under **Show As**

![image](https://user-images.githubusercontent.com/112718519/199614129-ee29dbe9-d8a3-4c07-9cfc-2c3972c5c197.png)

56. In Layered Bars, ensure that **Front** is checked

![image](https://user-images.githubusercontent.com/112718519/199614167-8050f4d9-5060-488a-acdf-812d182e1d0b.png)

⚠️**Quality Check!** Does your Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/199614205-174b6132-a506-4b77-a4ff-8260d5710428.png)

🚩 We now have a good representation of some key figures when it comes to our financial data. Now, let's incorporate some Headcount data into our dashboard to provide our management team a holistic view of the business. 

57. In the toolbar, click on the **Chart** icon

![image](https://user-images.githubusercontent.com/112718519/199614384-e0f4ff42-2531-44f8-836c-fc8db412f5fa.png)

58. Click and hold the border of the chart to move the object and position it to align with the Reporting Currency Input Control.

![image](https://user-images.githubusercontent.com/112718519/199614421-8ed5e049-b6b2-4712-b36c-328ff146fb36.png)

59. Click and hold the bottom right resize icon of the Chart

![image](https://user-images.githubusercontent.com/112718519/199614440-814aa9fe-f013-47af-a2bc-3feae53c91e8.png)

60. Resize the Chart so that its width is slightly smaller than the Table above

![image](https://user-images.githubusercontent.com/112718519/199614452-ea197062-ed9f-4adc-a8e1-925dfe37989f.png)

⚠️**Quality Check!** Does your Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/199614656-30cdeb21-8db1-4f07-b5dd-2bb2af222dd7.png)

🚩 We can see that the current data model that is being used in the Chart is SAP_XPA_FINANCE. In order to incorporate Headcount data into the Chart, you will need to change the Data Model for this Chart. 

61. Click the **Data Model** icon

![image](https://user-images.githubusercontent.com/112718519/199614680-185c7392-cf32-4771-b2c0-03a4033c8548.png)

62. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199614707-dd34101c-270e-4e2d-a52f-fe4a2063ec01.png)

63. Click on the arrow

![image](https://user-images.githubusercontent.com/112718519/199614722-9be45fed-d9d8-41db-b341-e3921d2a3fb1.png)

64. Click **SAP_XPA_HEADCOUNT**

![image](https://user-images.githubusercontent.com/112718519/199614750-00a70e68-ffb1-4803-8b13-9b7cf395ea10.png)

65. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199614759-5d55219d-8c1d-44e9-ab75-d303ac3cb7e3.png)

🚩 After selecting the Headcount Data Model, the Builder Panel automatically updates the name of the Data Model. For the Headcount Data Model, it is a Classic Account Model instead of a New Model that we saw for the Finance Data Model. Therefore, the Builder Panel is updated to reflect how Account is the only requirement for the Classic Account Model. 

You are not too familiar with the Headcount Data Model and you want to see a list of Accounts and Dimensions that are available to insert into the Chart. In the top right of the Builder Panel, click Available Objects.

66. Click **Available Objects** in the Builder Panel

![image](https://user-images.githubusercontent.com/112718519/199614808-726e270b-e505-4cc3-bac5-4ea168d46370.png)

ℹ️ Welcome to the Available Objects!

It provides you a holistic view of all the data related objects that are associated to the data model. It provides you an ability to quickly drag and drop objects into the Builder Panel or use any of the quick action menus to bind the data.

![image](https://user-images.githubusercontent.com/112718519/199614821-90c0c534-1dcb-4ef4-91f6-a737fa4214d5.png)

🚩 Based on the data that is available within this data model, we are interested in building a trend over time that represents our headcount.

67. Click on the **More** action icon for **Headcount**
68. Click Add to Accounts

![image](https://user-images.githubusercontent.com/112718519/199614850-ef04bcda-b276-4f05-a404-bf829eefe0fb.png)

69. Click on the search bar and type **Hire**
70. Click on the **More** action icon for **SAP_XPA_HIRE_DATE**
71. Click on **Add to Dimensions**

![image](https://user-images.githubusercontent.com/112718519/199614876-7cc5eaf4-2f4a-499a-8fbf-41e72c8e0a70.png)

⚠️ **Quality Check!** Does your Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/199614927-5b725dba-846c-40f7-9347-b13e6b41c24b.png)

72. Click on the bar that represents (all)
73. Click on the **Drill Down** icon

![image](https://user-images.githubusercontent.com/112718519/199615079-53213222-d2fc-466c-ac77-4c306cc558b2.png)

74. Within the Builder Panel, click on the **Drill icon** for SAP_XPA_HIRE_DATE
75. Click Level 3

![image](https://user-images.githubusercontent.com/112718519/199615137-24d31957-a09b-497a-a229-297580ce89a8.png)
 
⚠️ **Quality Check!** Does your Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/199615304-31b90bd2-ebe0-41ad-bfb8-9e847413036d.png)

76. Scroll to the bottom of the Builder Panel
77. Click **expand** for the Chart Add-ons
78. Click **Variance**

![image](https://user-images.githubusercontent.com/112718519/199615321-a07afb49-0dc1-44d1-9e99-8af337b711af.png)

79. Click **+ Add Version/Time**

![image](https://user-images.githubusercontent.com/112718519/199615363-7be00bfb-c3f0-4ee2-aff5-501a82b37bce.png)

80. Click **SAP_XPA_HIRE_DATE** 

![image](https://user-images.githubusercontent.com/112718519/199615382-20f9a59f-e4b3-4f29-973b-d830722bcfc2.png)

81. Click **Integrated**
82. Click **Done**

![image](https://user-images.githubusercontent.com/112718519/199615441-94bf4697-dd97-400a-b84a-4942ec5b3c42.png)

83. Click **X** to close the Available Objects List

![image](https://user-images.githubusercontent.com/112718519/199615461-7ae950e2-393a-4cf7-9cca-b5300d7ce122.png)

⚠️Quality Check! Does you Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/199615859-3948d55b-c853-44f6-a4da-d1375c0da680.png)

🚩 We now want to add a Geographical representation of where the hires are per location. It would also be a good idea for us to better understand the various career levels that we have by headcount per location.

84. Click the **Add** icon
85. Click **Geo Map** in the Others section

![image](https://user-images.githubusercontent.com/112718519/199615919-eac54a69-a388-4737-a0eb-f015343a61fe.png)

86. Click and hold the border of the Geo Widget to move the object

![image](https://user-images.githubusercontent.com/112718519/199615961-ee6becd3-05d9-4ca2-93fb-94f5d2f4757b.png)

87. Move the Geo Widget to align it with the top of the Chart

![image](https://user-images.githubusercontent.com/112718519/199615995-9e08e298-529d-41f7-82ca-ec5787c638d3.png)

88. Resize the Geo to align it with the Chart above and the edge of the shape header

![image](https://user-images.githubusercontent.com/112718519/199616013-abff90f4-b84e-4ea0-b2ce-15e4002dcc73.png)

🚩 We want to change the Base Layer Style to better match the theme of the rest of the dashboard.

89. Click Light Gray to open the dropdown menu to see other Base Layer Styles
90. Click Transparent Dark Gray

![image](https://user-images.githubusercontent.com/112718519/199616077-80944b2b-ab56-43b2-afbb-d84d38c5ad8c.png)

91. Click **+ Add Layer**

![image](https://user-images.githubusercontent.com/112718519/199616094-37e75041-3392-4ab6-9455-5638e91eb8a7.png)

92. Click **+ Location Dimension required** 

![image](https://user-images.githubusercontent.com/112718519/199616134-5362cd8c-9a4a-4cbf-971d-1c93123f2f7c.png)

93. Click **Hire_Location**

![image](https://user-images.githubusercontent.com/112718519/199616156-f6966a84-f910-4540-ad26-65b65df54e27.png)

ℹ️ Location Clustering in Geo Visualization! Adding a Location Dimension will determine whether or not Location Clustering in the Builder Panel will continue to be turned on or automatically turned off. It will be turned off if you have less than 5000 data points. In this example, Location Clustering is automatically turned off. 

![image](https://user-images.githubusercontent.com/112718519/199616164-63424461-3b29-435d-a609-215330b2ea1d.png)

🚩 We can now see data points for all our hire locations int the Geo Map. Let's add Headcount and Career Level as the size and color respectively to further drill down into our data.

94. Under Bubble Size click **+ Add Account**

![image](https://user-images.githubusercontent.com/112718519/199616178-cea0143c-d512-46bb-805d-61374bf6d152.png)

95. Click **Headcount**

![image](https://user-images.githubusercontent.com/112718519/199616193-20e7ea28-94a3-41f0-a6d7-67dc15aa2f58.png)

96. Under Bubble Color click **+ Add Dimension/Account**

![image](https://user-images.githubusercontent.com/112718519/199616210-c7c3b02e-170c-464c-843f-e578db0dcfe1.png)

97. Click **SAP_XPA_CAREER_LEVEL**

![image](https://user-images.githubusercontent.com/112718519/199616226-2203fcd9-c514-4d7c-8573-28b63021a495.png)

98. Rename the Layer Name to **Headcount by Career Level**
99. Click **Done**

![image](https://user-images.githubusercontent.com/112718519/199616260-56114cd8-3c04-476d-866f-296aafc2517b.png)

⚠️ **Quality Check!** Does your Geo Visualization look like this?

![image](https://user-images.githubusercontent.com/112718519/199100172-356e447d-7660-4e5f-a8d8-255e0b4da34c.png)

🚩 Press CTRL + S to save your story. 

🚩 We are now interested in adding another KPI to summarize the Average Salary that we are paying our employees. To make it easier, let's duplicate the existing KPI so that we don't need to worry much about the formatting of the object.

100. Click on the **Numeric Point Chart Operating Income for 2022**
101. Click the **More** Action icon
102. Hover over **Copy** and select **Duplicate**

![image](https://user-images.githubusercontent.com/112718519/199616304-e0fea9e2-86d1-4115-887f-b60ec1d67c2f.png)

103. Move the object besides Operating Income for 2022
104. Click on the **Data Model** icon

![image](https://user-images.githubusercontent.com/112718519/199616336-765a0b26-8cc6-40a9-af6b-8377c685074a.png)

105. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199616357-3ceba66e-51e1-4eb7-b523-65ea2e5bf9a8.png)

106. Click **SAP_XPA_HEADCOUNT**

![image](https://user-images.githubusercontent.com/112718519/199616370-e709cfa7-2ff2-4428-ab41-4d505c34b251.png)

107. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199616382-b70570cd-62bf-469f-b233-583d7c5999e2.png)

108. Click **+ At least 1 Account required** 

![image](https://user-images.githubusercontent.com/112718519/199616406-bd93dc3b-4aba-40fe-b508-80c91b952add.png)

109. Click **Salary** 

![image](https://user-images.githubusercontent.com/112718519/199616418-f7626f08-9f83-4595-8962-ec9dc62fbae3.png)

🚩 After clicking Salary, we realize that the KPI shows the total salary that was ever paid to employees. This KPI doesn't show Average Salary per Employee, which is what you want to see in the KPI.

Hence, we will have to create a calculation to reflect this metric.

110. Deselect **Salary** 
111. Click **Add Calculation** 

![image](https://user-images.githubusercontent.com/112718519/199616462-749ed36a-bf99-4b55-abef-cba4ade09cb0.png)

112. Click **Aggregation**

![image](https://user-images.githubusercontent.com/112718519/199616481-31a823d4-0e6a-4464-a60d-00fab25b0a84.png)

113. Click the **Expand** icon for Operation
114. Scroll down till you see **Average**
115. Click **Average**

![image](https://user-images.githubusercontent.com/112718519/199616516-329b39e5-6899-4056-ac00-9200334e1501.png)

116. Click the **Expand** icon for Account
117. Click **Salary** 

![image](https://user-images.githubusercontent.com/112718519/199616532-e044cc22-dfa0-4f4b-8495-a156c78132b2.png)

118. Click the Expand icon for Aggregation Dimensions
119. Click SAP_XPA_EMPLOYEE

![image](https://user-images.githubusercontent.com/112718519/199616545-46e3da5b-e227-48ff-be5e-be6570b57629.png)

120. Rename the calculation to **Average Salary**
121. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199616558-d6b8a418-8723-4bc9-9e7a-970f4d335bae.png)

122. Rename the Title to **Average Salary**

![image](https://user-images.githubusercontent.com/112718519/199616576-f8b5cdd3-67df-415a-8413-df11ac313bad.png)

123. Click the **More** Action icon
124. Hover over Show / Hide and deselect **Primary Value Labels**

![image](https://user-images.githubusercontent.com/112718519/199616589-351dc39c-43f7-456c-b618-0067a178791f.png)

⚠️Quality Check! Does your KPI look like this?

![image](https://user-images.githubusercontent.com/112718519/199616621-4663cfe0-e300-4bee-ace0-6766b967aec6.png)

🚩 Press CTRL + S to save your story. 



## Summary

**You have completed the entire Understanding the Basics of SAP Analytics Cloud Stories section!**

**You are now able to:**
- Create a set of visualizations (i.e. Chart, Geo, and Table) to illustrate key relationships within your data
- Understand the difference between the Builder Panel vs. Styling Panel 
- Create a set of basic calculations
- Include Chart Add-ons, such as a Variance

Continue to - [Exercise 2 - Integrating Planning into a Business Intelligence Story](../ex2/README.md)

