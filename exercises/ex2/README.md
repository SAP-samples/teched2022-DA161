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

1. Click on the Financial Plan tab in the top panel 

![image](https://user-images.githubusercontent.com/112718519/198351548-c58c90b9-9a1a-418f-bd03-c5644f8d4d9b.png)

2. Click on any cell in the Table

![image](https://user-images.githubusercontent.com/112718519/198356466-4440061e-6928-4860-a84b-a8dba0d2b3ab.png)

3. Click the **Version Management** icon in the top panel

![image](https://user-images.githubusercontent.com/112718519/198356498-2feae846-62ad-48f3-9d49-0913e4f2e354.png)

ℹ️ Welcome to Version Management! This is where you can manage any public/private versions that are associated with the data model. In this example, all versions are public, which means that the values are visible to other users. You can make changes directly on a public version or work with a private version instead.

4. First, let's make a private version of 23 Plan. Click on the **Copy** icon.

![image](https://user-images.githubusercontent.com/112718519/198352025-7425b580-7a86-489f-a2a9-dd9551b4c433.png)

5. Rename the Version Name to **XX - 23 Plan**. XX can be replaced by your ID number.

![image](https://user-images.githubusercontent.com/112718519/198352046-44f3243d-9fd7-458f-a4e6-d0a5fb2b8b23.png)

6. Click **OK** 

![image](https://user-images.githubusercontent.com/112718519/198352058-c4774e05-ac7c-48ef-9b99-5f3bf4e1688f.png)

ℹ️ The private version that you just created now appears in the Version Management panel.

7. Click **Close**

![image](https://user-images.githubusercontent.com/112718519/198352087-8997df07-c0cf-4b41-a05b-837842eecee9.png)

8. You want to filter the story to only show data belonging to XX - 23 Plan. In the Version filter, select **XX - 23 Plan**.

![image](https://user-images.githubusercontent.com/112718519/198352123-0497beba-0e49-4105-b715-a93bb57f473e.png)

🚩 Now, you can start making changes to your data. To begin, let’s make some adjustments to raw material charges for BestBikes GmbH to account for some ongoing inflation pressures you are expecting specifically with suppliers in that region. 

9. First, click the **story filter** at the top panel. Click **BestBikes GmbH**.

![image](https://user-images.githubusercontent.com/112718519/198352156-6a606f53-3d43-4973-84ae-21634b09d4c2.png)

10. In the Financial Account filter panel, click **Raw Materials**

![image](https://user-images.githubusercontent.com/112718519/198672383-0d581a2b-a6c4-4983-9132-4ae8c9d6d7d4.png)

11. Click on the **arrow** to expand 2023 values

![image](https://user-images.githubusercontent.com/112718519/198673232-ed129f1a-aa9d-44ea-ba54-f4c87c5c9f3a.png)

🚩 The planned changes to changes to raw material will not take effect until our new supply contract becomes active, which will occur after Q1/2023 (i.e. increases will not apply to the first three months of the year). 

12. Highlight the cells from **January to March 2023**. 

![image](https://user-images.githubusercontent.com/112718519/198673524-c2d519cf-ab4a-42f7-bdb2-40267a3a3370.png)

13. Right click the highlighted cells and click **Lock Cell**. 

🚩 By clicking Lock Cell, you are no longer able to apply edits and changes to the cells.

![image](https://user-images.githubusercontent.com/112718519/198673613-7a926024-8a5f-4b9e-af66-e622e1446a69.png)

14. Now, you want to increase the raw material charges by 10% for the year 2023. Click into the value for 2023.

![image](https://user-images.githubusercontent.com/112718519/198673705-8bba7d3e-3b86-4898-9f76-841ef504e623.png)

15. Type in **+10%** directly into the cell

![image](https://user-images.githubusercontent.com/112718519/198673724-fa5aaac4-19b8-447f-a89f-fca46a6be4d7.png)

ℹ️ Now, all the values are increased by 10% except for January 2023 to March 2023. This is because you have previously locked these cells. The increase in raw material charges are only applied to April 2023 to December 2023.

⚠️ **Quality check!** Does your Table look like this?

![image](https://user-images.githubusercontent.com/112718519/198673777-60efac1f-5c08-42a6-a074-53fd3ac93b89.png)

🚩 Let's change the story filter so that you are filtering the data to show bikes in the Chinese market (China Bikes Ltd). 

16. Click the story filter in the top panel. Click **China Bikes Ltd**.

![image](https://user-images.githubusercontent.com/112718519/198673990-057eb2f2-1f2d-4899-a946-831dc2a6295d.png)

17. In the Plan Currency filter panel, click **Local Currency**

![image](https://user-images.githubusercontent.com/112718519/198674057-3c940b12-a1b4-4d91-acba-901c15a44cfc.png)

18. Scroll to the bottom of the dashboard. In the Financial Account filter panel, click **Gross Sales**

![image](https://user-images.githubusercontent.com/112718519/198674178-33c45352-241c-49c8-942e-c48ceb53de1f.png)

19. Click the **arrow** to expand All Channels, which will show unassigned data for Gross Sales

![image](https://user-images.githubusercontent.com/112718519/198674318-cf059071-f066-4f62-9ba2-7356f4937c3e.png)

🚩 The unassigned data is assumed to be the total Gross Sales, all of which has occurred via our retail channel up until this point. However, next year we are going to run a pilot project in China to also sell directly via a newly developed Web Store. For this reason, we want to distribute the unassigned data for Gross Sales into different channels, which includes the Web Store and Retailer network. Before you do that, you want to display all channel members so that they are visible in the Table.

20. Right-click on the **SAP_XPA_CHANNEL header** in the Table. In Show/Hide, click Unbooked.

![image](https://user-images.githubusercontent.com/112718519/198674405-00cd1de7-67bc-4573-b422-10e8adeea724.png)

🚩 Currently, there are no values in Web Store and Retail Stores, so you want to distribute the unassigned data for Gross Sales into these two channels. You assume Web Store consumes 10% of Gross Sales and Retail Stores consume 90% of Gross Sales.

21. Let's right click into the unassigned value for 2023. Click **Distribute Value**.

![image](https://user-images.githubusercontent.com/112718519/198674535-ec777d83-285e-4236-9125-1b46cf997621.png)

ℹ️ Welcome to the Planning Panel! This is where you can specify the distribution of values to one or more cells. Or, you can also redistribute the values of a group of cells.

22. Under Recommendations, click **Distribute to SAP_XPA_CHANNEL members of the same level**

![image](https://user-images.githubusercontent.com/112718519/198674584-95319dad-8215-423b-a51c-81c1aadaf697.png)

23. Under Cell, select **Overwrite**

![image](https://user-images.githubusercontent.com/112718519/198674631-420faef7-da02-4757-ae1e-3212597de257.png)

24. Under Input Values, select **Input Weights**

![image](https://user-images.githubusercontent.com/112718519/198674659-d6d802ed-2e4c-4ba7-a310-e26ce551ee7d.png)

25. Now, you can specify the weights that you want to assign to Web Store and Retails Stores. Enter **10** for Web Store.

![image](https://user-images.githubusercontent.com/112718519/198674952-b613b9a3-087d-47a7-a189-1e873b6c6417.png)

26. Enter **90** for Retail Stores

![image](https://user-images.githubusercontent.com/112718519/198674716-671841a2-be5f-4059-b584-8984412dd7b7.png)

27. Click **Apply**

![image](https://user-images.githubusercontent.com/112718519/198674744-7f36f2cb-ebb4-40e8-9f60-25fa2c1d5c9f.png)

⚠️ **Quality check!** All the unassigned data for Gross Sales are now distributed to the corresponding channels. Does your Table look like this?

![image](https://user-images.githubusercontent.com/112718519/198674798-e804f457-8c96-4f6a-a989-5e7d150f723a.png)

🚩 Finally, you want to make some adjustments to Headcount for our Japanese business (Nippon Bikes) in anticpation of further growth in that market beyond 2023.  Navigate to the page in your story that contains Headcount data. 

28. Click on the **Employee Plan** tab

![image](https://user-images.githubusercontent.com/112718519/198675006-75e1a4b7-c3a8-4aa8-8b3f-26ca45312621.png)

29. Click **XX - 23 Plan**

![image](https://user-images.githubusercontent.com/112718519/198675047-df2658ec-ddb7-406c-b19b-deb350087c0b.png)

30. Click the **story filter** in the top panel. Click **Nippon Bikes**.

![image](https://user-images.githubusercontent.com/112718519/198675078-5b87034b-2fae-4d6f-b4b6-8f3618192c35.png)

🚩 For August through December 2023, we are looking to ramp up Headcount in Sales & Marketing. As a result of increasing Headcount, you are also anticipating that sales will increase in future years. 

31. In Sales & Marketing for August 2023, type in **17**

<img src="https://user-images.githubusercontent.com/112718519/198675354-a282e983-2165-41a0-afe3-9c30dce80859.png" width= "750" />

32. In Sales & Marketing for September 2023, type **20**

<img src="https://user-images.githubusercontent.com/112718519/198675641-8d2c74ed-442e-4c4a-b36c-7103d983a6a3.png" width= "750" />

33. For Sales & Marketing in October 2023, type **23**

<img src="https://user-images.githubusercontent.com/112718519/198675751-68145de0-2f11-45b1-bf3a-89a8ff627e23.png" width= "750" />

34. For Sales & Marketing in November 2023, type **25**

<img src="https://user-images.githubusercontent.com/112718519/198675801-38a6ac3f-ad5a-4ef8-a037-028aa9885ace.png" width= "750" />

35. For Sales & Marketing in December 2023, type **27**

<img src="https://user-images.githubusercontent.com/112718519/198675962-54698eb9-b8c6-49af-86e1-e98d49410df6.png" width= "750" />

36. Now, you want to ensure that changes with the Headcount data are reflected in the overall Financial Plan. Click the **Financial Plan** tab.

![image](https://user-images.githubusercontent.com/112718519/198676162-6329605b-60b9-4b21-9fb8-b0e2bd0fe097.png)

37. Click into the **story filter**. Click **All**.

![image](https://user-images.githubusercontent.com/112718519/198676193-60eb5811-7d5d-4f8f-bbbe-b848b51ba52f.png)

38. In the Plan Currency filter panel, click **US Dollars** 

![image](https://user-images.githubusercontent.com/112718519/198676247-bb6c7631-b1b7-4f82-98a1-07586e57f95d.png)

39. Scroll to the bottom of the dashboard. In the Financial Account filter panel, click **Operating Income**

![image](https://user-images.githubusercontent.com/112718519/198676350-c3881036-9a64-4bc9-9bbd-efffdb4b4d92.png)

40. Click **Run Data Action**, which is the blue button button

![image](https://user-images.githubusercontent.com/112718519/198678260-4ebc3702-a1a8-4a63-b7ed-0d63c4ec3817.png)

ℹ️ The Data Action Trigger runs a batch calculation to recalculate personnel costs related to the increase in Headcount.

41. Click the **version icon** to open a list of target versions

![image](https://user-images.githubusercontent.com/112718519/198676435-0e4ff3ad-7adb-4eea-904f-e0db3da9023e.png)

42. Click the private version that you created. In this case, it would be XX - 23 Plan.

![image](https://user-images.githubusercontent.com/112718519/198676453-bb6dfcfd-71cb-42f3-9059-5fb7fd6cfb74.png)

43. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/198676478-2c083883-5628-4b0e-aea9-0b2c03476641.png)

44. Click **Run**.  The Data Action will be running the calculation in the background and updating your data.

![image](https://user-images.githubusercontent.com/112718519/198676490-2e5d52eb-4e5f-412b-ad5e-e6f385d0bcd4.png)

ℹ️ After running the Data Action Trigger, the widgets are updated to reflect the new calculation. The two KPIS, Operating Income XX - 23 Plan and Total Labour Cost, both have updated values. The Table also has updated values highlighted in yellow, which includes values for Opearting Income, Operating Expenses and Personnel Costs.

⚠️ **Quality check!** Does your story look like this? 

![image](https://user-images.githubusercontent.com/112718519/198676607-7d43d5f4-9ea1-4db9-8e29-fcb4447b970a.png)


## Summary

**You have completed the entire Integrating Planning into a Business Intelligence Story section!**

**You are now able to:**
* Conduct changes to planned data
* Use the Planning Panel to distribute values
* Use the Version Management Panel to create versions
* Run a data action to perform a batch calculation 

Continue to - [Exercise 3 - Integrating Scripting](../ex3/README.md)

