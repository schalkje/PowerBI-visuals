---
layout: docs
title: Creating a Custom Visual
description: In this exercise, you will create a custom visual, and also setup the development environment in the Power BI service.
group: quickstarts
toc: true
---

1. In Windows PowerShell, first, verify that the Power BI Visual Tools package has been installed.
```typescript
   pbiviz
```

2. Review the output, including the list of supported commands.
![](../images/pbiviz-output.png)

3. Navigate to your **MySolution** folder, using the folder path you used to install the course files.
```typescript
   cd D:\PowerBI\MySolution
```

4. To create a custom visual project, enter the following command.
CircleCard is the name of the project.
```typescript
   pbiviz new CircleCard
```

5. Navigate to the project folder.
```typescript
   cd CircleCard
```

6. Start the custom visual.
The visual is now running, hosted on your computer, and is ready for testing.
```typescript
   pbiviz start
```
*The visual is now running, hosted on your computer, and is ready for testing.*

7. Leave Windows PowerShell open.

## Testing the Custom Visual
In this task, you will upload a Power BI Desktop report, and then edit the report to display the custom visual.

1. In the Power BI window, at the top-right corner, click **Settings** (cog icon), and then select **Settings**.  
![](../images/settings-option.png)

2. At the left, select the **Developer** page.  
![](../images/developer-option.png)

3. In the right pane, check the **Enable Developer Visual for Testing** checkbox.  
![](../images/enable-developer-visual.png)

4. To upload a Power BI Desktop report, at the bottom-left corner, click **Get Data**.  
![](../images/get-data.png)

5. Select the **Files** tile.  
![](../images/get-files.png)

6. Select the **Local File** tile.  
![](../images/local-file.png)

7. In the **Choose File to Upload window**, navigate to **D:\PowerBI\Lab12\Assets** folder.

8. Select **Test Custom Visual.pbix**, and then click **Open**.  
*This Power BI Desktop report is a light-weight solution containing just two fields to support the
testing of the custom visual.*

9. Once uploaded, in the **Navigation** pane, select the **Test Custom Visual** report.

10. To edit the report, on the toolbar, click **Edit Report**.  
![](../images/edit-report.png)

11. In the **Visualizations** pane, select the **Developer Visual**.  
![](../images/visualizations-pane.png)  
*This visualization represents the custom visual that you started on your computer. It is only available when the developer settings have been enabled.*

12. Notice that a visualization was added to the report canvas.  
![](../images/update-count.png)  
*This is a very simple visual that displays the number of times its **Update** method has been called. At this stage the visual does not yet retrieve any data.*

13. In the **Fields** pane, check the **Quantity** field to add it to the visual.  
![](../images/fields-pane.png)  

14. Resize the visual, and notice that the update value increments.

15. In PowerShell, to stop the custom visual running, enter **Ctrl+C**, and when prompted to terminate
the batch job, enter **Y**, and then press **Enter**.  
*Tip: During the development and testing of your custom visual, if at any stage you receive errors or unexpected behavior, you should stop and restart the custom visual. Issues can be due to an inconsistent project build, often due to dependencies being added—or, because project files have not yet been saved.*  

*You have now setup the development environment. In the next exercise, you will commence developing the custom visual by using D3 visual elements.*  

Next step: [Adding Visual Elements](../adding-visual-elements/)