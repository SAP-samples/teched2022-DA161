# Exercise 2 – Integrating Planning into a Business Intelligence Story

**Objective:** You should develop a basic understanding of planning capabilities in SAP Analytics Cloud.

**Estimated Time:** 20 mins

**Exercise Description:** You are managing a dashboard that contains planned financial data for TCS Technologies. You have already completed a preliminary plan for 2023, however based on new information, some final adjustments are required before submitting it to upper management. 

**Key Features:**
* Make updates to planned data
* Understand the Planning Panel and Version Management Panel
* Run a data action to perform a batch calculation 

⚠️**Disclaimer**
When completing exercises, some data values or screenshots may not match what you see on your screen. It is because the current exercise is based on a feature that is currently in BETA. 

----------------------------------------------------------------------------------------------------------------------------------------

ℹ️ Welcome to Planning!

🚩 We are going to make changes to planned financial data. First, let's make a copy of the last planned version for 2023.

1. Click on the Financial Plan tab in the top panel 

![image](https://user-images.githubusercontent.com/112718519/198351548-c58c90b9-9a1a-418f-bd03-c5644f8d4d9b.png)

2. Click on any cell in the Table

![image](https://user-images.githubusercontent.com/112718519/200690296-b835c503-2550-4359-bbb7-c49d09b1b936.png)

3. Click the **Version Management** icon in the top panel

![image](https://user-images.githubusercontent.com/112718519/198356498-2feae846-62ad-48f3-9d49-0913e4f2e354.png)

ℹ️ Welcome to Version Management! This is where you can manage any public/private versions that are associated with the data model. In this example, all versions are public, which means that the values are visible to other users. You can make changes directly on a public version or work with a private version instead.

4. First, let's make a private version of 23 Plan. Click on the **Copy** icon.

![image](https://user-images.githubusercontent.com/112718519/199292519-5adf706c-d12d-4dfd-8810-2070e2e3a352.png)

5. Rename the Version Name to **XX - 23 Plan**. XX can be replaced by your ID number.

![image](https://user-images.githubusercontent.com/112718519/200690927-7db9c7b2-2277-4a5a-9a58-38ed42198ec6.png)

6. Click **OK** 

![image](https://user-images.githubusercontent.com/112718519/200690980-1b6e7520-3217-4054-90fb-02305fcf7d81.png)

ℹ️ The private version that we just created now appears in the Version Management panel.

7. Click **Close**

![image](https://user-images.githubusercontent.com/112718519/199292557-8409cc7f-bd80-4f28-87df-b459d0c6c688.png)

8. We want to filter the story to only show data belonging to XX - 23 Plan. In the Version filter, select **XX - 23 Plan**.

![image](https://user-images.githubusercontent.com/112718519/199126556-77df54c3-b38f-4a1c-a64c-23b050b4cf40.png)

🚩 Now, we can start making changes to your data. To begin, let’s make some adjustments to raw material charges for BestBikes GmbH to account for some ongoing inflation pressures we are expecting specifically with suppliers in that region. 

9. First, click the **story filter** at the top panel. Click **BestBikes GmbH**.

![image](https://user-images.githubusercontent.com/112718519/198352156-6a606f53-3d43-4973-84ae-21634b09d4c2.png)

10. In the Financial Account filter panel, click **Raw Materials**

![image](https://user-images.githubusercontent.com/112718519/198672383-0d581a2b-a6c4-4983-9132-4ae8c9d6d7d4.png)

🚩 The planned changes to changes to raw material will not take effect until our new supply contract becomes active, which will occur after Q1/2023 (i.e. increases will not apply to the first three months of the year). 

11. Highlight the cells from **January to March 2023**. 

![image](https://user-images.githubusercontent.com/112718519/200692297-2e60c218-3609-4c0d-9956-fee36da86e0d.png)

12. Right click the highlighted cells and click **Lock Cell**. 

🚩 By clicking Lock Cell, we are no longer able to apply edits and changes to the cells.

![image](https://user-images.githubusercontent.com/112718519/200692315-e678f8ca-052c-4e7a-9c3d-c77814fcba11.png)

13. Now, we want to increase the raw material charges by 10% for the year 2023. Click into the value for 2023.

![image](https://user-images.githubusercontent.com/112718519/200692374-76ebf301-a31f-4634-98c5-0f4a7554c454.png)

14. Type in **+10%** directly into the cell

![image](https://user-images.githubusercontent.com/112718519/200692388-dfc3d69f-d461-4f43-a4a6-2e6afbe9c245.png)

ℹ️ Now, all the values are increased by 10% except for January 2023 to March 2023. This is because we have previously locked these cells. The increase in raw material charges are only applied to April 2023 to December 2023.

⚠️ **Quality check!** Does your Table look like this?

![image](https://user-images.githubusercontent.com/112718519/200692810-4aac3b1f-93f2-469d-89db-4e4f8c7ac27f.png)

🚩 Let's change the story filter so that we are filtering the data to show bikes in the Chinese market (China Bikes Ltd). 

15. Click the story filter in the top panel. Click **China Bikes Ltd**.

![image](https://user-images.githubusercontent.com/112718519/199125688-708e3410-aaaa-4c0b-92a0-abf4def7c17f.png)

16. In the Plan Currency filter panel, click **Local Currency** (Note: SAP Analytics Cloud allows the user to plan, forecast, and/or report in any number of currencies depending on specific model and report settings)

![image](https://user-images.githubusercontent.com/112718519/199292628-d76277dd-df1e-485b-a73b-a98500512aca.png)

17. Scroll to the bottom of the dashboard. In the Financial Account filter panel, click **Gross Sales**

![image](https://user-images.githubusercontent.com/112718519/199292681-b9046bcc-6729-4026-835c-879159410cd8.png)

18. Click the **arrow** to expand All Channels, which will show unassigned data for Gross Sales

![image](https://user-images.githubusercontent.com/112718519/200693650-afab1ed3-ad4f-4807-89d4-ce384046e12f.png)

🚩 The unassigned data is assumed to be the total Gross Sales, all of which has occurred via our retail channel up until this point. However, next year we are going to run a pilot project in China to also sell directly via a newly developed Web Store. For this reason, we want to distribute the unassigned data for Gross Sales into different channels, which includes the Web Store and Retailer network. Before we do that, we want to display all channel members so that they are visible in the Table.

19. Right-click on the **SAP_XPA_CHANNEL header** in the Table. In Show/Hide, click **Unbooked**.

![image](https://user-images.githubusercontent.com/112718519/200693670-f1e869a2-659f-4133-b7d3-54de1fe6a201.png)

🚩 Currently, there are no values in Web Store and Retail Stores, so we want to distribute the unassigned data for Gross Sales into these two channels. Let's assume Web Store consumes 10% of Gross Sales and Retail Stores consume 90% of Gross Sales.

20. Let's right click into the unassigned value for 2023. Click **Distribute Value**.

![image](https://user-images.githubusercontent.com/112718519/200693713-70950f96-f621-4aa1-a0fc-1475607cedb9.png)

ℹ️ Welcome to the Planning Panel! This is where you can specify the distribution of values to one or more cells. Or, you can also redistribute the values of a group of cells.

21. Under Recommendations, click **Distribute to SAP_XPA_CHANNEL members of the same level**

![image](https://user-images.githubusercontent.com/112718519/199125787-9640cc4e-010f-451e-8a9e-f677dd76523d.png)

22. Under Cell, select **Overwrite**

![image](https://user-images.githubusercontent.com/112718519/199125797-55418bee-d000-467d-a4c1-78c3999db557.png)

23. Under Input Values, select **Input Weights**

![image](https://user-images.githubusercontent.com/112718519/199125808-b25f7559-e903-42d0-b0b2-fd6e0953f1df.png)

24. Now, we can specify the weights that we want to assign to Web Store and Retails Stores. Enter **10** for Web Store.

![image](https://user-images.githubusercontent.com/112718519/199125827-099cf07f-146d-452c-8109-371d92286b9d.png)

25. Enter **90** for Retail Stores

![image](https://user-images.githubusercontent.com/112718519/199125839-65811b99-acaa-435a-a3be-0d04e03aef6b.png)

26. Click **Apply**

![image](https://user-images.githubusercontent.com/112718519/199125862-b818b4fc-55ed-49ae-b2df-16359eb155e3.png)

⚠️ **Quality check!** All the unassigned data for Gross Sales are now distributed to the corresponding channels. Does your Table look like this?

![image](https://user-images.githubusercontent.com/112718519/200694420-417188d3-b4af-424b-8ca4-50888fe7a817.png)

🚩 Finally, we want to make some adjustments to Headcount for our Japanese business (Nippon Bikes) in anticpation of further growth in that market beyond 2023.  Navigate to the page in your story that contains Headcount data. 

27. Click on the **Employee Plan** tab

![image](https://user-images.githubusercontent.com/112718519/199125903-091929e2-e25e-48fa-a085-585ba6925ef1.png)

28. Click **XX - 23 Plan**

![image](https://user-images.githubusercontent.com/112718519/199125911-bc160994-f85c-44e3-a25d-96fad7cfe5c2.png)

29. Click the **story filter** in the top panel. Click **Nippon Bikes**.

![image](https://user-images.githubusercontent.com/112718519/199125938-7f8ce2dc-3254-46a4-9d81-4acebfeef9e9.png)

🚩 For August through December 2023, we are looking to ramp up Headcount in Sales & Marketing. As a result of the additional Headcount, you are also anticipating that sales will increase. 

30. In Sales & Marketing for August 2023, type in **17**
31. In Sales & Marketing for September 2023, type **20**
32. For Sales & Marketing in October 2023, type **23**
33. For Sales & Marketing in November 2023, type **25**
34. For Sales & Marketing in December 2023, type **27**

![image](https://user-images.githubusercontent.com/112718519/199125988-d4324ea3-e405-4e56-b9cb-b54627b91627.png)

35. Now, we want to ensure that changes with the Headcount data are reflected in the overall Financial Plan. Click the **Financial Plan** tab.

![image](https://user-images.githubusercontent.com/112718519/199126017-5948c8f3-2403-4450-bc98-f76f99773113.png)

36. Click into the **story filter**. Click **All**.

![image](https://user-images.githubusercontent.com/112718519/199126030-48ce7415-449e-48b5-b7ac-63030c45e5b9.png)

37. In the Plan Currency filter panel, click **US Dollars** 

![image](https://user-images.githubusercontent.com/112718519/199126046-52affde5-8adc-4bb7-9999-c00e8771790d.png)

38. Scroll to the bottom of the dashboard. In the Financial Account filter panel, click **Operating Income**

![image](https://user-images.githubusercontent.com/112718519/199126056-e8aa5d01-18d1-4e45-8ebc-bd46ccc94a0c.png)

39. Click **Run Data Action**, which is the blue button

![image](https://user-images.githubusercontent.com/112718519/200695076-346b95f4-9731-4f56-92bc-49257ad759b7.png)

ℹ️ The Data Action Trigger runs a batch calculation to recalculate personnel costs related to the increase in Headcount.

40. Click the **version icon** to open a list of target versions

![image](https://user-images.githubusercontent.com/112718519/199126087-54d177fa-cf4f-45fc-a964-d356eaf8b592.png)

41. Click the private version. In this case, it would be XX - 23 Plan. Note that the label of the version will show the ID (which includes your username) and description. 

![image](https://user-images.githubusercontent.com/112718519/199126100-702ef249-ee58-4019-b31a-80a53f8cadc3.png)

42. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199126111-25e70e90-ae6e-4b07-9b6a-25c5919370d9.png)

43. Click **Run**.  The Data Action will be running the calculation in the background and updating your data.

![image](https://user-images.githubusercontent.com/112718519/199126124-d8f43832-d041-46dc-8148-6329dd357fec.png)

ℹ️ After running the Data Action Trigger, the widgets are updated to reflect the new calculation. The two KPIS, Operating Income XX - 23 Plan and Total Labour Cost, both have updated values. The Table also has updated values highlighted in yellow, which includes values for Operating Income, Operating Expenses and Personnel Costs.

⚠️ **Quality check!** Does your story look like this? 

![image](https://user-images.githubusercontent.com/112718519/200695429-9b627e25-5f19-4359-a432-306ac0d5ef3a.png)


## Summary

**You have completed the entire Integrating Planning into a Business Intelligence Story section!**

**You are now able to:**
* Conduct changes to planned data
* Use the Planning Panel to distribute values
* Use the Version Management Panel to create versions
* Run a data action to perform a batch calculation 

Continue to - [Exercise 3 - Integrating Scripting](../ex3/README.md)

