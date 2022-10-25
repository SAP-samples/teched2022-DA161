# Exercise 2 – Integrating Planning into a Business Intelligence Story

**Objective:** You should develop a basic understanding of planning capabilities in SAP Analytics Cloud.

**Estimated Time:** 20 mins

**Exercise Description:** You are managing a dashboard that contains planned financial data for TCS Technologies. You have already completed a preliminary plan for 2023, however based on some new information some final adjustments are required before sending it out to the various regions for any last minute adjustments they may have. 

**Key Features:**
* Make updates to planned data
* Understand the Planning Panel and Version Management Panel
* Run a data action to perform a batch calculation 

⚠️**Disclaimer**
When completing exercises, some data values or sceenshots may not match what you see on your sceen. It is because the current exercise is based on a feature that is currently in BETA. 

----------------------------------------------------------------------------------------------------------------------------------------

ℹ️ Welcome to Planning!

🚩 Welcome to Section 2 of TechEd! You are going to make changes to planned financial data. First, you will be making a copy of the last planned version for 2023. 

1. Click on any cell in the Table

![image](https://user-images.githubusercontent.com/112718519/197855251-1a4e3988-c6f1-42f3-9875-6fc64fc21314.png)

2. Click the **Version Management** icon in the top panel

![image](https://user-images.githubusercontent.com/112718519/197855407-e8642188-5b9e-42cd-b17b-cbc828138cd1.png)

ℹ️ Welcome to Version Management! This is where you can manage any public/private versions that are associated with the data model. In this example, all versions are public, which means that the values are visible to other users. You can make changes directly on a public version or work with a private version instead.

3. First, let's make a private version of 23 Plan. Click on the **Copy** icon.

![image](https://user-images.githubusercontent.com/112718519/197856355-55ae0266-3da5-42c9-bcb2-fe68d99b8887.png)

4. Rename the Version Name to **XX - 23 Plan**. XX can be replaced by your ID number.

![image](https://user-images.githubusercontent.com/112718519/197856499-e04f1531-3746-4754-8564-9e32e7c3300f.png)

5. Click **OK** 

![image](https://user-images.githubusercontent.com/112718519/197856555-c3e81d72-f1e7-4b65-8439-75cb5bf7a9db.png)

ℹ️ The private version that you just created now appears in the Version Management panel.

6. Click **Close**

![image](https://user-images.githubusercontent.com/112718519/197856824-289404a3-c744-4514-a0ec-6e16df33aa26.png)

7. You want to filter the story to only show data belonging to XX - 23 Plan. In the Version filter, select **XX - 23 Plan**.

![image](https://user-images.githubusercontent.com/112718519/197857141-8f4f583a-2ae3-4dc2-a961-12de698a55ad.png)

🚩 Now, you can start making changes to your data. To begin, let’s make some adjustments to raw material charges for BestBikes GmbH to account for some ongoing inflation pressures you are expecting specifically with suppliers in that region. 

8. First, click the **story filter** at the top panel. Click **BestBikes GmbH**.

![image](https://user-images.githubusercontent.com/112718519/197857321-9f18fc0c-a95b-4a2b-b243-f55e145995bc.png)

9. In the Financial Account filter panel, click **Raw Materials**

![image](https://user-images.githubusercontent.com/112718519/197857446-56fdc527-ef62-4944-8c52-0800774bbc87.png)

🚩 The planned changes to changes to raw material will not take effect until our new supply contract becomes active, which will occur after Q1/2023 (i.e. increases will not apply to the first three months of the year). 

10. Highlight the cells from **January to March 2023**. 

![image](https://user-images.githubusercontent.com/112718519/197857593-65972a8b-94f9-4ded-aade-7005ae8cf933.png)

11. Right click the highlighted cells and click **Lock Cell**. 

🚩 By clicking Lock Cell, you are no longer able to apply edits and changes to the cells.

![image](https://user-images.githubusercontent.com/112718519/197857750-33a69b42-21a0-423e-98a3-5a39ebbe3ca0.png)

12. Now, you want to increase the raw material charges by 10% for the year 2023. Click into the value for 2023.

![image](https://user-images.githubusercontent.com/112718519/197857806-23ca38db-3b06-4962-925f-703d04353801.png)

13. Type in **+10%** directly into the cell

![image](https://user-images.githubusercontent.com/112718519/197857846-23063384-04a6-4be9-b6c6-a1890aa3d71b.png)

ℹ️ Now, all the values are increased by 10% except for January 2023 to March 2023. This is because you have previously locked these cells. The increase in raw material charges are only applied to April 2023 to December 2023.

![image](https://user-images.githubusercontent.com/112718519/197857953-2adba33f-66e4-480b-aa26-48e6fbe1498c.png)

⚠️ **Quality check!** Does your Table look like this?

🚩 Let's change the story filter so that you are filtering the data to show bikes in the Chinese market (China Bikes Ltd). 

14. Click the story filter in the top panel. Click **China Bikes Ltd**.

![image](https://user-images.githubusercontent.com/112718519/197858769-aa895356-10fa-48bf-9289-9a27ef9375a7.png)

15. In the Financial Account filter panel, click **Gross Sales**

![image](https://user-images.githubusercontent.com/112718519/197858825-4b6868cf-8753-4ab5-8ff5-76baf41cd38a.png)

16. In the Plan Currency filter panel, click **Local Currency**

![image](https://user-images.githubusercontent.com/112718519/197858876-4074856c-5a47-4395-9898-b67d0e7bd80a.png)

17. Click the **arrow** to expand All Channels, which will show unassigned data for Gross Sales

![image](https://user-images.githubusercontent.com/112718519/197858961-676bb33d-9e15-48fb-8af7-6774a53ed5ef.png)

🚩 The unassigned data is assumed to be the total Gross Sales, all of which has occurred via our retail channel up until this point. However, next year we are going to run a pilot project in China to also sell direct via a newly developed Web Store.  For this reason, we want to distribute the unassigned data for Gross Sales into different channels, which includes the Web Store and Retailer network. Before you do that, you want to display all channel members so that they are visible in the Table.

18. Right-click on the **SAP_XPA_CHANNEL header** in the Table. In Show/Hide, click Unbooked.

![image](https://user-images.githubusercontent.com/112718519/197859068-bbddced9-6047-4903-9dd2-b797cd97ab66.png)

🚩 Currently, there are no values in Web Store and Retail Stores, so you want to distribute the unassigned data for Gross Sales into these two channels. You assume Web Store consumes 10% of Gross Sales and Retail Stores consume 90% of Gross Sales.

19. Let's right click into the unassigned value for 2023. Click **Distribute Value**.

![image](https://user-images.githubusercontent.com/112718519/197859208-2c3536b1-fbd5-4a01-b451-55b55dbd2778.png)

ℹ️ Welcome to the Planning Panel! This is where you can specify the distribution of values to one or more cells. Or, you can also redistribute the values of a group of cells.

20. Under Recommendations, click **Distribute to SAP_XPA_CHANNEL members of the same level**

![image](https://user-images.githubusercontent.com/112718519/197859357-15903864-ecc8-4b82-86e2-798ec03d462b.png)

21. Under Cell, select **Overwrite**

![image](https://user-images.githubusercontent.com/112718519/197859424-c83c6fce-5109-4dda-a6df-c45b11dba27b.png)

22. Under Input Values, select **Input Weights**

![image](https://user-images.githubusercontent.com/112718519/197859491-bfd19d79-a7ea-4ace-8b39-26253ae020cc.png)

23. Now, you can specify the weights that you want to assign to Web Store and Retails Stores. Enter **10** for Web Store.

![image](https://user-images.githubusercontent.com/112718519/197859549-8b691cb2-b46a-4739-b4a6-3ea334ec3d0c.png)

24. Enter **90** for Retail Stores

![image](https://user-images.githubusercontent.com/112718519/197859579-b2028ae7-9bfa-490f-971e-7b847c1859c2.png)

25. Click **Apply**

![image](https://user-images.githubusercontent.com/112718519/197859615-cb53e735-5093-49af-b3bc-c49ce444e96d.png)

⚠️ **Quality check!** All the unassigned data for Gross Sales are now distributed to the corresponding channels. Does your Table look like this?

![image](https://user-images.githubusercontent.com/112718519/197859709-b1701458-c17f-41fe-ac92-26e8c463dae0.png)

🚩 Finally, you want to make some adjustments to Headcount for our Japanese business (Nippon Bikes) in anticpation of further growth in that market beyond 2023.  Navigate to the page in your story that contains Headcount data. 

26. Click the arrow in the top panel to navigate to the **Employee Plan** page.

![image](https://user-images.githubusercontent.com/112718519/197862137-7f9205e1-05db-49d0-8a5c-595e1ebd3746.png)

27. Click **XX - 23 Plan**

![image](https://user-images.githubusercontent.com/112718519/197862188-5d62021b-7535-4cff-8b0f-da0b36c13682.png)

28. Click the **story filter** in the top panel. Click **Nippon Bikes**.

![image](https://user-images.githubusercontent.com/112718519/197862517-165f070a-563a-4a99-afd0-50c39c91dfa0.png)

🚩 For August through December 2023, we are looking to ramp up Headcount in Sales & Marketing. As a result of increasing Headcount, you are also anticipating that sales will increase in future years. 

29. In Sales & Marketing for August 2023, type in **17**

![image](https://user-images.githubusercontent.com/112718519/197862614-d3a01f2c-db99-4a9b-87f7-3272cb86a7cb.png)

30. In Sales & Marketing for September 2023, type **20**

![image](https://user-images.githubusercontent.com/112718519/197864226-e564fcfc-1914-404c-b2fc-f469fcd93245.png)

31. For Sales & Marketing in October 2023, type **23**

![image](https://user-images.githubusercontent.com/112718519/197864291-711c9c1a-3dcd-49da-ac23-f784b4523732.png)

32. For Sales & Marketing in November 2023, type **25**

![image](https://user-images.githubusercontent.com/112718519/197864366-ddafa652-5544-438f-a373-64d06ca6814f.png)

33. For Sales & Marketing in December 2023, type **27**

![image](https://user-images.githubusercontent.com/112718519/197864426-2ec889fe-8433-46c9-8cfb-227f025ec9be.png)

⚠️ **Quality check!** Does your table look like this?

![image](https://user-images.githubusercontent.com/112718519/197864554-098cc072-4681-4dea-a8ec-fc692d2bdbb5.png)

34. Now, you want to ensure that changes with the Headcount data is reflected in the overall Financial Plan. Click the arrow in the top panel to navigate to the **Financial Plan** tab.

![image](https://user-images.githubusercontent.com/112718519/197864651-0d46c25d-c872-428b-9ca0-2992d984da20.png)

35. Click into the **story filter**. Click **All**.

![image](https://user-images.githubusercontent.com/112718519/197864725-7c6e0527-f50e-474e-8a21-fb179bfb42c2.png)

36. In the Financial Account filter panel, click **Operating Income**

![image](https://user-images.githubusercontent.com/112718519/197864800-8188afa3-afd9-4e2c-9d45-8e5fd1ab0979.png)

37. In the Plan Currency filter panel, click **US Dollars** 

![image](https://user-images.githubusercontent.com/112718519/197864843-8061901c-3ddb-4fa2-9b00-de28ace614a3.png)

38. Click the **Run Data Action** button

![image](https://user-images.githubusercontent.com/112718519/197864891-ac978afb-e5ca-4016-9fe7-43d26fd397ad.png)

ℹ️ The Data Action Trigger runs a batch calculation to recalculate personnel costs related to the increase in Headcount.

39. Click the **version icon** to open a list of target versions

![image](https://user-images.githubusercontent.com/112718519/197864987-72c78389-7e20-4dd5-85ac-76dc28fe9334.png)

40. Click the private version that you created. In this case, it would be XX - 23 Plan.

![image](https://user-images.githubusercontent.com/112718519/197865026-8e045807-db24-4a0d-85a4-94ac9c4af123.png)

41. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/197865065-4c1e238e-ff49-4850-9c0d-ee443184bb79.png)

42. Click **Run**.  The Data Action will be running the calculation in the background and updating your data.

![image](https://user-images.githubusercontent.com/112718519/197865097-550d637a-4ede-425d-9378-bd18b3b29598.png)

⚠️ **Quality check!** Does your Table look like this? 

![image](https://user-images.githubusercontent.com/112718519/197865162-9e4a9180-0056-4922-abb3-a2777456d010.png)


## Summary

**You have completed the entire Integrating Planning into a Business Intelligence Story section!**

**You are now able to:**
* Conduct changes to planned data
* Use the Planning Panel to distribute values
* Use the Version Management Panel to create versions
* Run a data action to perform a batch calculation 

Continue to - [Exercise 3 - Integrating Scripting](../ex3/README.md)

