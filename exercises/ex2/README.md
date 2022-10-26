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

🚩 Before we get started, refer to the Getting Started section to find the starting dashboard for this exercise and create a copy of the starting dashboard. 

ℹ️ Welcome to Planning!

🚩 You are going to make changes to planned financial data. First, you will be making a copy of the last planned version for 2023.

1. Click on any cell in the Table

![image](https://user-images.githubusercontent.com/112718519/197855251-1a4e3988-c6f1-42f3-9875-6fc64fc21314.png)

2. Click the **Version Management** icon in the top panel

![image](https://user-images.githubusercontent.com/112718519/197899218-91460dbd-d4b2-45ba-aa06-60c248d1f866.png)

ℹ️ Welcome to Version Management! This is where you can manage any public/private versions that are associated with the data model. In this example, all versions are public, which means that the values are visible to other users. You can make changes directly on a public version or work with a private version instead.

3. First, let's make a private version of 23 Plan. Click on the **Copy** icon.

![image](https://user-images.githubusercontent.com/112718519/197899265-969d8fc3-eb93-4ffc-a1dd-8791b7eb2c22.png)

4. Rename the Version Name to **XX - 23 Plan**. XX can be replaced by your ID number.

![image](https://user-images.githubusercontent.com/112718519/197899311-de3b58c5-85ea-4f2a-beb4-cbe5215550f5.png)

5. Click **OK** 

![image](https://user-images.githubusercontent.com/112718519/197899325-0069a5c4-017b-4894-afbf-df9f9bcf6625.png)

ℹ️ The private version that you just created now appears in the Version Management panel.

6. Click **Close**

![image](https://user-images.githubusercontent.com/112718519/197899348-f054afb9-6ad0-4ea3-b599-d0c942532b73.png)

7. You want to filter the story to only show data belonging to XX - 23 Plan. In the Version filter, select **XX - 23 Plan**.

![image](https://user-images.githubusercontent.com/112718519/197899387-7ea56b15-0350-47f3-9b00-9b1f19a04a34.png)

🚩 Now, you can start making changes to your data. To begin, let’s make some adjustments to raw material charges for BestBikes GmbH to account for some ongoing inflation pressures you are expecting specifically with suppliers in that region. 

8. First, click the **story filter** at the top panel. Click **BestBikes GmbH**.

![image](https://user-images.githubusercontent.com/112718519/197899396-6667710d-eac9-4882-89d8-47d3b49ed59b.png)

9. In the Financial Account filter panel, click **Raw Materials**

![image](https://user-images.githubusercontent.com/112718519/197899420-639dc987-9982-44c6-add0-6196f3052276.png)

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

![image](https://user-images.githubusercontent.com/112718519/197899513-39934dd5-4096-47a8-a3f9-b103c6673bf2.png)

15. In the Financial Account filter panel, click **Gross Sales**

![image](https://user-images.githubusercontent.com/112718519/197899533-b67e1c69-6fc0-4b11-b895-496d4a0928aa.png)

16. In the Plan Currency filter panel, click **Local Currency**

![image](https://user-images.githubusercontent.com/112718519/197899550-86536d77-29cb-497d-9cbe-4675b339f8f0.png)

17. Click the **arrow** to expand All Channels, which will show unassigned data for Gross Sales

![image](https://user-images.githubusercontent.com/112718519/197900365-9101732a-759a-48a7-a7a0-ef344c40400b.png)

🚩 The unassigned data is assumed to be the total Gross Sales, all of which has occurred via our retail channel up until this point. However, next year we are going to run a pilot project in China to also sell direct via a newly developed Web Store.  For this reason, we want to distribute the unassigned data for Gross Sales into different channels, which includes the Web Store and Retailer network. Before you do that, you want to display all channel members so that they are visible in the Table.

18. Right-click on the **SAP_XPA_CHANNEL header** in the Table. In Show/Hide, click Unbooked.

![image](https://user-images.githubusercontent.com/112718519/197900396-c96d7f1b-ac62-4638-bd78-d83f92cab93c.png)

🚩 Currently, there are no values in Web Store and Retail Stores, so you want to distribute the unassigned data for Gross Sales into these two channels. You assume Web Store consumes 10% of Gross Sales and Retail Stores consume 90% of Gross Sales.

19. Let's right click into the unassigned value for 2023. Click **Distribute Value**.

![image](https://user-images.githubusercontent.com/112718519/197900416-2a1e15db-d8c9-4332-a32b-f817c75efd85.png)

ℹ️ Welcome to the Planning Panel! This is where you can specify the distribution of values to one or more cells. Or, you can also redistribute the values of a group of cells.

20. Under Recommendations, click **Distribute to SAP_XPA_CHANNEL members of the same level**

![image](https://user-images.githubusercontent.com/112718519/197899581-37094eb7-48d9-40cb-b884-2be230ffd54a.png)

21. Under Cell, select **Overwrite**

![image](https://user-images.githubusercontent.com/112718519/197899598-d10b1f23-369b-4532-ac1b-a3ea4e222081.png)

22. Under Input Values, select **Input Weights**

![image](https://user-images.githubusercontent.com/112718519/197899617-535cf39c-bc0f-4e9e-b1ca-31d4180ddabd.png)

23. Now, you can specify the weights that you want to assign to Web Store and Retails Stores. Enter **10** for Web Store.

![image](https://user-images.githubusercontent.com/112718519/197899641-37a9e3b2-948d-47af-bbd2-ccf7d83b5e49.png)

24. Enter **90** for Retail Stores

![image](https://user-images.githubusercontent.com/112718519/197899659-4c898299-5f89-448e-9eef-67f1edf00528.png)

25. Click **Apply**

![image](https://user-images.githubusercontent.com/112718519/197899683-d85cbde3-dc45-416d-89e0-98988b6f99a3.png)

⚠️ **Quality check!** All the unassigned data for Gross Sales are now distributed to the corresponding channels. Does your Table look like this?

![image](https://user-images.githubusercontent.com/112718519/197859709-b1701458-c17f-41fe-ac92-26e8c463dae0.png)

🚩 Finally, you want to make some adjustments to Headcount for our Japanese business (Nippon Bikes) in anticpation of further growth in that market beyond 2023.  Navigate to the page in your story that contains Headcount data. 

26. Click on the **Employee Plan** tab

<img src="https://user-images.githubusercontent.com/112718519/198103855-283d964c-c212-47d5-9fef-77a7c66db250.png" width="750" />

27. Click **XX - 23 Plan**

<img src="https://user-images.githubusercontent.com/112718519/197899722-a073d61a-6fb7-4779-835a-6fd3f319137e.png" width="600" />

28. Click the **story filter** in the top panel. Click **Nippon Bikes**.

![image](https://user-images.githubusercontent.com/112718519/197899744-8c80af46-594a-485d-8f68-d5c933faf639.png)

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

34. Now, you want to ensure that changes with the Headcount data are reflected in the overall Financial Plan. Click the **Financial Plan** tab.

<img src="https://user-images.githubusercontent.com/112718519/198103315-87684d6e-cbee-4009-bf62-5b481fd4f7c6.png" width="750" />

35. Click into the **story filter**. Click **All**.

![image](https://user-images.githubusercontent.com/112718519/197899822-dab7e71b-fd0a-42a0-b68a-72b41214105e.png)

36. In the Financial Account filter panel, click **Operating Income**

![image](https://user-images.githubusercontent.com/112718519/197899829-33a2b7fd-4ae5-45de-9f03-bcc81a334654.png)

37. In the Plan Currency filter panel, click **US Dollars** 

![image](https://user-images.githubusercontent.com/112718519/197899843-5b113fd6-e5db-4946-87f1-04d87b05a11a.png)

38. Click the **Run Data Action** button

![image](https://user-images.githubusercontent.com/112718519/197899861-8ebe1780-5c2b-433e-8ec9-ec9dfc4e61d5.png)

ℹ️ The Data Action Trigger runs a batch calculation to recalculate personnel costs related to the increase in Headcount.

39. Click the **version icon** to open a list of target versions

![image](https://user-images.githubusercontent.com/112718519/197899875-34b92f2b-fe30-4914-9e4e-165a5232831b.png)

40. Click the private version that you created. In this case, it would be XX - 23 Plan.

![image](https://user-images.githubusercontent.com/112718519/197899884-00a436c0-6389-4a2b-a627-e39bf47bd57b.png)

41. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/197899899-87c33bd3-be96-4667-9dd9-d0958e53a3a4.png)

42. Click **Run**.  The Data Action will be running the calculation in the background and updating your data.

![image](https://user-images.githubusercontent.com/112718519/197899915-45a871ad-8a93-47ad-93a0-08f55e00978c.png)

ℹ️ After running the Data Action Trigger, the widgets are updated to reflect the new calculation. The two KPIS, Operating Income XX - 23 Plan and Total Labour Cost, both have updated values. The Table also has updated values highlighted in yellow, which includes values for Opearting Income, Operating Expenses and Personnel Costs.

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

