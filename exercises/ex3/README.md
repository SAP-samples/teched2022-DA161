# Exercise 3 – Integrating Scripting

**Objective:** You should develop a basic understanding of scripting capabilities in SAP Analytics Cloud.

**Estimated Time:** 20 mins

**Exercise Description:** In Exercise 2, our customers were able to execute planning actions. As they were working through the planning dashboard, they realized that they weren't sure what rates were being used for the calculations in the Financial Plan and Employee Plan. We want to provide them a better understanding of what those rates are by utilizing scripting capabilities in SAP Analytics Cloud.

**Key Features:**
* Understand how to add a popup in a dashboard
* Utilize a button to increase user interaction in a popup
* Write scripts to open and close a popup 

⚠️**Disclaimer**
When completing exercises, some data values or sceenshots may not match what you see on your sceen. It is because the current exercise is based on a feature that is currently in BETA. 

----------------------------------------------------------------------------------------------------------------------------------------

1. Click **Edit** 

![image](https://user-images.githubusercontent.com/112718519/198360329-af917931-431d-422c-8b1e-9d3bc1471293.png)

2. Now that we are an editor of the dashboard, we can see that there is a hidden page. Click the **Employee Rates Table** tab.

![image](https://user-images.githubusercontent.com/112718519/198360386-fb87d369-15c7-407b-9627-60410c9ad58d.png)

🚩 The Employee Rates Table provides us with an understanding of the rates that are used for calculations in the Financial Plan and Employee Plan. However, we want to access the Employee Rates Table in an easier way. In order to do that, we want to provide a jumpoff point in the Employee Plan Table that can show us the rates.

3. First, we want to copy the table. Right click into the Table and click **Copy**. Alternatively, we can also press **Ctrl+C**.

![image](https://user-images.githubusercontent.com/112718519/198360455-4d190c51-5297-4694-a9cd-aaf734ac78c8.png)

4. Click on the **Employee Plan** tab

![image](https://user-images.githubusercontent.com/112718519/198360764-e62ddf43-4bf1-4acf-88d4-c0e82c956557.png)

5. Click on the **Left Side Panel** icon 

![image](https://user-images.githubusercontent.com/112718519/198360800-154749b2-b098-47fe-b526-1001ae33651b.png)

6. **Click Outline**

![image](https://user-images.githubusercontent.com/112718519/198360871-38f1af0e-1428-44cd-b977-f6a0fc1c5af1.png)

7. The blue circular dot on the Left Side Panel indicates that Page 3 is the current active page. On Page 3, click on the **More** icon.

![image](https://user-images.githubusercontent.com/112718519/198361779-6e2d33be-311c-4ee2-8131-42d9e6b3f7ee.png)

8. Click **Add Popup** 

![image](https://user-images.githubusercontent.com/112718519/198361559-5daba728-5342-40b4-b2f2-cf0cca8116d5.png)

9. Press **Ctrl+V** to paste the Table into the Popup

![image](https://user-images.githubusercontent.com/112718519/198361611-834d1df0-8155-4253-9908-71bbf6f20759.png)

10. Click **Continue**

![image](https://user-images.githubusercontent.com/112718519/198361820-5e046d7c-4c00-46fd-aad7-bfe6884fffc6.png)

⚠️ **Quality check!** Does your Popup look like this?

![image](https://user-images.githubusercontent.com/112718519/198361991-cfea35ae-6888-46b8-a9ab-a60708c09a58.png)

11. Click the **Right Side Panel** icon to open the Styling panel

![image](https://user-images.githubusercontent.com/112718519/198362025-553f51df-9746-44c5-a092-5d8f5ed1a7d5.png)

12. We want to resize the Popup. In the Styling panel, scroll down until you see the width and height. Change the width to 1700.

![image](https://user-images.githubusercontent.com/112718519/198362094-ef605f33-0721-4b9e-8708-26584abf359d.png)

13. Change the height to 524

![image](https://user-images.githubusercontent.com/112718519/198362144-f6f56a42-6c29-450d-9382-6a8a160d0c42.png)

14. Click the **Right Side Panel** icon to close the Styling panel

![image](https://user-images.githubusercontent.com/112718519/198362228-4b838422-a68c-4cdb-a507-bebf2100a1e7.png)

15. Now, we want to make sure that we have the ability to close the Employee Rates Table in the Popup via a Button. We will add a Button by clicking the **Add** icon in the top panel.

![image](https://user-images.githubusercontent.com/112718519/198362294-3a0a7147-29fb-469d-b1ba-3e90b082ecd9.png)

16. Click **Button**

![image](https://user-images.githubusercontent.com/112718519/198362356-d17d744d-cfd5-4419-91f5-b439646e65c3.png)

17. We want to move the Button to the top right of the Table. Click the edge of the Button and drag. 

18. Drag the Button to the top right of the Table

![image](https://user-images.githubusercontent.com/112718519/198362482-cbc58e04-a721-44d7-889e-0cdb12e1f906.png)

19. We want to rename the Button. Click the **Right Side Panel** icon to open the Styling panel.

![image](https://user-images.githubusercontent.com/112718519/198362554-9bb0db51-745f-4464-928d-db67338d3219.png)

20. Under Text, rename the Button to **Close Rates Table**

![image](https://user-images.githubusercontent.com/112718519/198362612-e393c90b-5cb7-47f0-b1c3-0b0e94b3d82d.png)

21. Click the **Right Side Panel** icon to close the Styling panel

![image](https://user-images.githubusercontent.com/112718519/198362681-55d55eac-d655-4675-b6ba-49f12d6bb5ec.png)

22. We want to resize the Button to make it larger. Click on the bottom left corner of the Button.

23. Drag the button to lengthen the width

![image](https://user-images.githubusercontent.com/112718519/198362881-49244db2-c68b-4c84-957a-29ea142e718f.png)

24. Now, we will begin the scripting. Click on the **Employee Plan** tab.
![image](https://user-images.githubusercontent.com/112718519/198363080-e11d9da4-3804-4bc4-b28f-a28db8f28faf.png)

25. Click onto the shape. After clicking, notice how the left vertical panel automatically highlights the shape that is currently selected.

![image](https://user-images.githubusercontent.com/112718519/198363152-a329b1e4-9d61-465e-97ef-46d6dab3c459.png)

26. In Shape_7, click the **Edit Scripts** icon

![image](https://user-images.githubusercontent.com/112718519/198363213-b31bafd0-ebe2-4cfa-af65-64c1cddfc2ca.png)

27. Click **onClick**

![image](https://user-images.githubusercontent.com/112718519/198363265-60848d79-7a37-4038-8bb2-02e0242478b8.png)

🚩 Welcome to Scripting! Scripting allows you to write scripts that can perform complex actions for widgets, such as customizing user interactions in widgets. While writing the scripts, you can press Ctrl + Space on your keyboard to show all the available scripting commands. 

28. Type **Popup_1.**

![image](https://user-images.githubusercontent.com/112718519/198363328-8269dd31-a86f-4f26-9987-6b6a55afda8b.png)

29. Press **Ctrl + Space** on your keyboard to open a list of available scripting commands. Click open. This command enables the Popup to open when it is clicked.

![image](https://user-images.githubusercontent.com/112718519/198363507-e874e3f6-3202-4ecf-b894-f753657d6cd3.png)

30. Press the semicolon ; on your keyboard

![image](https://user-images.githubusercontent.com/112718519/198363549-c2e2752a-5152-431e-95a4-78983b0f3ecb.png)

31. After writing a script to open the Popup, we now want to write another script to close the Popup. Click **Popup_1** in the Left Side Panel.

![image](https://user-images.githubusercontent.com/112718519/198363599-0429b90b-39ec-44a2-960b-0e12ab2aea91.png)

32. Scroll to the right of the Table until we see the Button. Click on the **Close Rates Table Button**.

![image](https://user-images.githubusercontent.com/112718519/198363883-b1dded9e-d232-4d3e-83ca-86e98be42e36.png)

33. Click on the **More Actions** icon

![image](https://user-images.githubusercontent.com/112718519/198363940-7718be03-3a38-454f-b15a-5f4b8468496e.png)

34. In Edit Scripts, click **onClick**

![image](https://user-images.githubusercontent.com/112718519/198363973-0253d3d1-51f8-4467-a5cc-71f2c7ace490.png)

35. Type **Popup_1.**

![image](https://user-images.githubusercontent.com/112718519/198364070-75426d79-06e3-41e6-b4e2-3ef821ceaee7.png)

36. Press **Ctrl + Space** on our keyboard to show a list of available commands. Click **close**.

![image](https://user-images.githubusercontent.com/112718519/198364119-818e1027-5dbf-4fb4-a878-7c48738e224d.png)

37. Press the semicolon ; on your keyboard

![image](https://user-images.githubusercontent.com/112718519/198364148-5094f179-3276-405e-b663-959e9093af3f.png)

38. Now, we will save our dashboard. Under File, click **Save**.

![image](https://user-images.githubusercontent.com/112718519/198364167-fa69ae4c-ebcb-4d84-a7ad-ea0c1fe5f6ed.png)

39. Now, we will go into View mode to test out the Popup. Click **View**, which will bring us to a new tab.

![image](https://user-images.githubusercontent.com/112718519/198364327-06d5b6b2-5151-409e-a6f6-99894e014eef.png)

40. Click the Employee Plan tab

![image](https://user-images.githubusercontent.com/112718519/198364346-03d7f7ed-1028-4206-a872-f2e2e0c9c3e0.png)

41. Click on the **shape** to launch the Employee Rates Table

![image](https://user-images.githubusercontent.com/112718519/198364526-d32380cb-1d14-4e1f-a344-79dee2018444.png)

42. Now that the Popup is open, we can now close it. Press on the **Close Rates Table Button**.

![image](https://user-images.githubusercontent.com/112718519/198364540-2af1c828-21d8-433b-b533-c8138a312791.png)


## Summary

**You have completed the entire Integrating Scripting section!**

**You are now able to:**
* Understand how to add a popup in a dashboard
* Utilize a button to increase user interaction in a popup
* Write scripts to open and close a popup 

Continue to - [Task1 - Evaluate the Usability of the Left Side Panel](../task1/README.md)

