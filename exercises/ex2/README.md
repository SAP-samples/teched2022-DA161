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

![image](https://user-images.githubusercontent.com/112718519/198351908-21a0aa4a-4c9e-43a6-b6c3-6713ed531e9e.png)

3. Click the **Version Management** icon in the top panel

<img src="https://user-images.githubusercontent.com/112718519/198351947-46c989db-91ae-4ec7-866b-334c65869721.png" width="700" />

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

![image](https://user-images.githubusercontent.com/112718519/198352176-9e844b64-2a22-43c4-8b10-e79677ab1df9.png)

🚩 The planned changes to changes to raw material will not take effect until our new supply contract becomes active, which will occur after Q1/2023 (i.e. increases will not apply to the first three months of the year). 

11. Highlight the cells from **January to March 2023**. 

![image](https://user-images.githubusercontent.com/112718519/198352217-71580a4f-99bc-4815-ad25-34828ecd1663.png)

12. Right click the highlighted cells and click **Lock Cell**. 

🚩 By clicking Lock Cell, you are no longer able to apply edits and changes to the cells.

![image](https://user-images.githubusercontent.com/112718519/198352236-19e214ad-590a-4603-ba2c-94476a42b21b.png)

13. Now, you want to increase the raw material charges by 10% for the year 2023. Click into the value for 2023.

![image](https://user-images.githubusercontent.com/112718519/198352565-f361d6b4-4d59-42b8-9c96-fb8775870e33.png)

14. Type in **+10%** directly into the cell

![image](https://user-images.githubusercontent.com/112718519/198352599-05fd5b79-66d6-4fb6-9612-28b976ad68ce.png)

ℹ️ Now, all the values are increased by 10% except for January 2023 to March 2023. This is because you have previously locked these cells. The increase in raw material charges are only applied to April 2023 to December 2023.

![image](https://user-images.githubusercontent.com/112718519/198352677-8628bce1-b009-44c7-8d41-37a8425adfe1.png)

⚠️ **Quality check!** Does your Table look like this?

🚩 Let's change the story filter so that you are filtering the data to show bikes in the Chinese market (China Bikes Ltd). 

15. Click the story filter in the top panel. Click **China Bikes Ltd**.

![image](https://user-images.githubusercontent.com/112718519/198352753-e824d8cf-6c1b-4935-b491-c196680fc180.png)

16. In the Financial Account filter panel, click **Gross Sales**
17. 
![image](https://user-images.githubusercontent.com/112718519/198352774-b5c8d471-9ad7-4948-affb-3efb0a50ae45.png)

17. In the Plan Currency filter panel, click **Local Currency**

![image](https://user-images.githubusercontent.com/112718519/198352790-a1e677ac-d912-4734-88f4-7740ad00d99e.png)

18. Click the **arrow** to expand All Channels, which will show unassigned data for Gross Sales

<img src="https://user-images.githubusercontent.com/112718519/198352815-1c44bd79-835a-4de1-87fc-d35a1e717196.png" width="650" />

🚩 The unassigned data is assumed to be the total Gross Sales, all of which has occurred via our retail channel up until this point. However, next year we are going to run a pilot project in China to also sell direct via a newly developed Web Store.  For this reason, we want to distribute the unassigned data for Gross Sales into different channels, which includes the Web Store and Retailer network. Before you do that, you want to display all channel members so that they are visible in the Table.

19. Right-click on the **SAP_XPA_CHANNEL header** in the Table. In Show/Hide, click Unbooked.

<img src="https://user-images.githubusercontent.com/112718519/198352884-f50f7591-e85b-497d-bdf8-cd2437483e42.png" width="650" />

🚩 Currently, there are no values in Web Store and Retail Stores, so you want to distribute the unassigned data for Gross Sales into these two channels. You assume Web Store consumes 10% of Gross Sales and Retail Stores consume 90% of Gross Sales.

20. Let's right click into the unassigned value for 2023. Click **Distribute Value**.

<img src="https://user-images.githubusercontent.com/112718519/198352989-4fe5a087-1cb2-48b0-8734-1ae85bae8ebd.png" width="650" />

ℹ️ Welcome to the Planning Panel! This is where you can specify the distribution of values to one or more cells. Or, you can also redistribute the values of a group of cells.

21. Under Recommendations, click **Distribute to SAP_XPA_CHANNEL members of the same level**

![image](https://user-images.githubusercontent.com/112718519/198353058-f7b63410-43ba-4d52-b0ff-0c088600f025.png)

22. Under Cell, select **Overwrite**

![image](https://user-images.githubusercontent.com/112718519/198353106-44110fe0-f854-4af0-92cd-9f6ba675d99d.png)

23. Under Input Values, select **Input Weights**

![image](https://user-images.githubusercontent.com/112718519/198353121-0348e375-03b5-48fe-8a3c-48530561df1a.png)

24. Now, you can specify the weights that you want to assign to Web Store and Retails Stores. Enter **10** for Web Store.

![image](https://user-images.githubusercontent.com/112718519/198353173-f866c59c-4960-4f5c-be1a-a9fba9801efd.png)

25. Enter **90** for Retail Stores

![image](https://user-images.githubusercontent.com/112718519/198353193-2e8324aa-2645-4196-935b-8ebb27b6dd01.png)

26. Click **Apply**

![image](https://user-images.githubusercontent.com/112718519/198353215-d982880f-7bef-4d89-b367-6564e0500430.png)

⚠️ **Quality check!** All the unassigned data for Gross Sales are now distributed to the corresponding channels. Does your Table look like this?

<img src="https://user-images.githubusercontent.com/112718519/198353260-fe4f48ab-84db-478d-b0de-c2d509b7309c.png" width="900" />

🚩 Finally, you want to make some adjustments to Headcount for our Japanese business (Nippon Bikes) in anticpation of further growth in that market beyond 2023.  Navigate to the page in your story that contains Headcount data. 

27. Click on the **Employee Plan** tab

![image](https://user-images.githubusercontent.com/112718519/198353337-7aad8797-c3cb-4ce1-80fc-18025d97d536.png)

28. Click **XX - 23 Plan**

<img src="https://user-images.githubusercontent.com/112718519/198353359-5c5badcc-8606-49ec-b5eb-cb7cab2581af.png" width="600" />

29. Click the **story filter** in the top panel. Click **Nippon Bikes**.

![image](https://user-images.githubusercontent.com/112718519/198353407-70e951e8-7e5b-4a12-95fa-81eb6e961460.png)

🚩 For August through December 2023, we are looking to ramp up Headcount in Sales & Marketing. As a result of increasing Headcount, you are also anticipating that sales will increase in future years. 

30. In Sales & Marketing for August 2023, type in **17**

![image](https://user-images.githubusercontent.com/112718519/198353420-bca39763-11f8-4ecc-84e2-e2c3a2d673b5.png)

31. In Sales & Marketing for September 2023, type **20**

![image](https://user-images.githubusercontent.com/112718519/198353435-d69f3dd4-4e39-4c39-b8e6-3b2a0ea1fbe4.png)

32. For Sales & Marketing in October 2023, type **23**

![image](https://user-images.githubusercontent.com/112718519/198353459-98e71cf2-6e3e-4e39-ae35-29659b4b3542.png)

33. For Sales & Marketing in November 2023, type **25**

![image](https://user-images.githubusercontent.com/112718519/198353477-1d2efb7f-d65d-4055-a1fe-5a56e35731d0.png)

34. For Sales & Marketing in December 2023, type **27**

![image](https://user-images.githubusercontent.com/112718519/198353499-051787c7-9557-4ec7-b5b4-0b78eed57483.png)

⚠️ **Quality check!** Does your table look like this?

![image](https://user-images.githubusercontent.com/112718519/198353517-2e42dce0-6084-4ed4-bba9-33097f3ef550.png)

35. Now, you want to ensure that changes with the Headcount data are reflected in the overall Financial Plan. Click the **Financial Plan** tab.

![image](https://user-images.githubusercontent.com/112718519/198353539-295b4a18-6a73-450c-a0b2-fb443178d53b.png)

36. Click into the **story filter**. Click **All**.

![image](https://user-images.githubusercontent.com/112718519/198353559-30e76d76-b514-4e89-a381-b7d36d4d42da.png)

37. In the Financial Account filter panel, click **Operating Income**

![image](https://user-images.githubusercontent.com/112718519/198353577-d1cc8089-be84-446c-ab0b-8b7250eeb6fb.png)

38. In the Plan Currency filter panel, click **US Dollars** 

![image](https://user-images.githubusercontent.com/112718519/198353593-8425e6a4-7125-488f-beb1-8d0cc90b845b.png)

39. Click the **Run Data Action** button

![image](https://user-images.githubusercontent.com/112718519/198353627-5e3654f9-d6c8-41a6-92fe-a5903697f50b.png)

ℹ️ The Data Action Trigger runs a batch calculation to recalculate personnel costs related to the increase in Headcount.

40. Click the **version icon** to open a list of target versions

![image](https://user-images.githubusercontent.com/112718519/198353661-7fb47083-33a1-49f6-a2f0-9713068950f6.png)

41. Click the private version that you created. In this case, it would be XX - 23 Plan.

![image](https://user-images.githubusercontent.com/112718519/198353675-711a5599-d461-48b9-88b5-72fc479c636d.png)

42. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/198353695-58cc9fce-1d44-4e2e-b5a2-4c7868eaa429.png)

43. Click **Run**.  The Data Action will be running the calculation in the background and updating your data.

![image](https://user-images.githubusercontent.com/112718519/198353706-8d64bfcc-b8bb-4b2f-9d81-df514de18c20.png)

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

