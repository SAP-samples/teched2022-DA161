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

10. Highlight the cells from January to March 2023. 

![image](https://user-images.githubusercontent.com/112718519/197857593-65972a8b-94f9-4ded-aade-7005ae8cf933.png)

11. Right click the highlighted cells and click Lock Cell. 

🚩 By clicking Lock Cell, you are no longer able to apply edits and changes to the cells.

![image](https://user-images.githubusercontent.com/112718519/197857750-33a69b42-21a0-423e-98a3-5a39ebbe3ca0.png)

12. Now, you want to increase the raw material charges by 10% for the year 2023. Click into the value for 2023.

![image](https://user-images.githubusercontent.com/112718519/197857806-23ca38db-3b06-4962-925f-703d04353801.png)

13. Type in +10% directly into the cell

![image](https://user-images.githubusercontent.com/112718519/197857846-23063384-04a6-4be9-b6c6-a1890aa3d71b.png)

ℹ️ Now, all the values are increased by 10% except for January 2023 to March 2023. This is because you have previously locked these cells. The increase in raw material charges are only applied to April 2023 to December 2023.

![image](https://user-images.githubusercontent.com/112718519/197857953-2adba33f-66e4-480b-aa26-48e6fbe1498c.png)

⚠️ Quality check! Does your Table look like this?


## Summary

**You have completed the entire Integrating Planning into a Business Intelligence Story section!**

**You are now able to:**
- TODO

Continue to - [Exercise 3 - Integrating Scripting](../ex3/README.md)

