## Part 5 – Predicting Subscriptions - Machine Learning

Key takeaways from this lab:
- Learning how to create data flows

## Creating a Data Flow for KoolKart Orders and Customers

1. Create a **Data Flow** and add a **Data Set**.

    Download the <a href="https://github.com/oracle/learning-library/raw/master/workshops/dvcs-5/Exercise%20Files/KoolKart%20Orders.xlsx">**KoolKart Orders.xlsx**</a> file.

    Now, select the hamburger menu button and click on the Home button.

    ![](images/500/img_5a_1_1v2.png " ")

    Select **Create** and then **Data Flow**.

    ![](images/500/img_5a_1_2.png " ")

    Select **Create Data Set** to load in the Excel file.

    ![](images/200/img_2a_2_2.png " ")

    Select **Drop data file here or click to browse** and select the **KoolKart Orders** data set.

    ![](images/200/img_2a_2_3.png " ")

    Click **Add** to add the **KoolKart Orders** to begin the data flow.

    ![](images/500/img_5a_1_3.png " ")

2. Once the **Data Flow Editor** opens up, select the **Data Flow Steps** tab.

    ![](images/500/img_5a_2_1.png " ")

    Download the <a href="https://github.com/oracle/learning-library/raw/master/workshops/dvcs-5/Exercise%20Files/KoolKart%20Customers.xlsx">**KoolKart Customers.xlsx**</a> file.

    Click the **Add Data** icon and drag it to the editor.

    ![](images/500/img_5a_2_2.png " ")

    Now, add the **KoolKart Customers** file by selecting **Create Data Set**, followed by **Drop data file here or click to browse** and then selecting **Add**, like we did in the previous steps.

    Click on **Join** and add it to the data flow.
    ![](images/500/img_5a_2_3.png " ")

    Ideally, OAC should detect the joining logic, but in case it doesn't, you will see an Incomplete join message.

    Click on the circle to complete the join.

    ![](images/500/img_5a_2_4v2.png " ")

    If you've successfully made the join, the dataflow will reflect the image below.

    ![](images/500/img_5a_2_5v2.png " ")

3. The **Movies & Music** category is not required for the analysis. So, we add a filter to the **Data Flow**.

    Select **Filter** and drag between **KoolKart Orders** and **Join**.

    ![](images/500/img_5a_3_1v2.png " ")

    Select the **+** and select the category attribute.

    ![](images/500/img_5a_3_2.png " ")

    Select **Movies & Music** to move it to the **Selections**. Click on the hamburger option, and select **Exclude Selections**.

    ![](images/500/img_5a_3_3.png " ")

4. Add **Select Columns** to the Data flow and exclude the duplicated **Customer ID**.

    Select **Select Columns** and drag it to **+** on in front of Join.

    ![](images/500/img_5a_4_1v2.png " ")

    Select **Customer_ID1** and click on **Remove Selected**.

    ![](images/500/img_5a_4_2v2.png " ")

5. Group Sales data into Regions.

    Select **+** next to **Select Columns** and then select **Group**.

    ![](images/500/img_5a_5_1v2.png " ")

    Click **Select column** and select **Customer Country**.

    ![](images/500/img_5a_5_1b.png " ")

    Set the group name to **Sales Region**.
    Then, name the first group **NA** and add **Canada** and **USA** to the group.

    ![](images/500/img_5a_5_2.png " ")

    Click **+ Group** to add a second group and name it **EMEA**. Add **France**, **United Kingdom**, and **Germany** to the group.

    Click **+ Group** to add a third group and name it **APAC**. Add **Japan** to the group.

    ![](images/500/img_5a_5_3.png " ")

    Now, drag **Save Data Set** into the editor. Save the data set as **KoolKart Orders & Customers**. Set **Order ID** and **Customer ID** to attributes.

    ![](images/500/img_5a_5_3_2v2.png " ")

    ![](images/500/img_5a_5_3_3v2.png " ")

    Save the **Data Flow** by clicking the Save button in the top corner.

    ![](images/500/img_5a_5_4.png " ")

    Name the data flow **KoolKart Dataflow**.

    ![](images/500/img_5a_5_5.png " ")

    Click **Run Data Flow** to execute the data flow.

    ![](images/500/img_5e_2_8.png " ")

    ![](images/500/img_5a_5_7v2.png " ")

## Using KoolKart Dataflow for Sales Analysis

1. Click on the hamburger button on the top left corner and select **Home**.

    ![](images/500/img_5e_1_1.png " ")

    Create a new project by double clicking on the the **KoolKart Orders & Customers** data set on the home page or clicking on the ellipses menu and selecting **Create Project**.

     ![](images/500/img_8a_2_1v2.png " ")

     ![](images/500/img_5a_6_1v2.png " ")

2. Go to the **Prepare** tab and select the **Customer Country** column.  

    ![](images/300/img_3d_1_1.png " ")

    ![](images/500/img_5b_2_2v2.png " ")

    Select the recommendation **Enrich Customer Country with continent**.

    ![](images/500/img_5b_2_3v2.png " ")

    >Notice, how the recommendation allows us to group the countries into sales regions with just 1 click and do so much more. Since, we have already grouped our data, let's return to visualizing.

    Click on **Visualize**.

     ![](images/300/img_3c_1_1.png " ")

3. Create Visualizations **Order Amount** by **Date** and **Category**.

    Select **Order Amount** and **Order Date** and select **Pick Visualization**.

    ![](images/500/img_5a_6_2v2.png " ")

    After you select **Pick Visualization**, select the **Line** chart.

    ![](images/500/img_5a_6_3v2.png " ")

    Double click the **Category** attribute to add it to your visualization. Switch the chart from a **Line** chart to an **Area** chart.

    ![](images/500/img_5b_1_1v2.png " ")

    Select **Order Date** dropdown in **Data Elements** section. Select **Month** and drag it to **Category (X-Axis)** to replace **Order Date**.

    ![](images/500/img_5b_1_2.png " ")

    ![](images/500/img_5b_1_3.png " ")

4. Create Visualization for **Order Amount** by **Category** and **Sub Category**.

    Select **Category**, **Sub Category**, and **Order Amount**. Right click and select **Pick Visualization**. Select **Tree Map**.

    ![](images/500/img_8b_2_2.png " ")

    ![](images/500/img_8b_2_3.png " ")

5. Create Visualization for **Order Amount** by **Order Date**.

    Select **Order Amount** and **Order Date**. Right click attributes while selected then select **Create Best Visualization**.

    ![](images/500/img_5b_3_1.png " ")

    Right click the visualization and select **Add Statistics** then select **Trend Line**.

    ![](images/500/img_5b_3_2v2.png " ")

    Right click the visualization and select **Add Statistics** then select **Forecast**.

    ![](images/500/img_5b_3_3v2.png " ")

    Refer to the visualization settings in **Project Components Menu** and select the **Analytics** option.

    Select the **Forecast** dropdown and enter 6 in the **Periods** textbox.

    ![](images/500/img_5b_3_4.png " ")

    Change the **Model** to **ARIMA**.

    ![](images/500/img_5b_3_5.png " ")

    You're canvas should reflect the picture below.

    ![](images/500/img_5b_3_6.png " ")

    Hover over the **Canvas 1** tab with your cursor and select the downward arrow to **Rename**. You can also right click to select **Rename**.

    ![](images/500/img_5b_3_7v2.png " ")

    Rename the canvas to "Sales".

    ![](images/500/img_5b_3_8.png " ")

    Save the project and name it "Machine Learning".

    ![](images/500/img_5b_3_9.png " ")

    ![](images/500/img_5b_3_10.png " ")

## Creating Visualization for Customer Analysis

1. Create a visualization of **Order Amount** by **Customer Age Group**.

    Create a new Canvas.

    ![](images/500/img_5c_2_1.png " ")

    Select **Order Amount** and **Customer Age Group**. While the attributes are selected, right click and select **Create Best Visualization**.

    ![](images/500/img_5c_2_2.png " ")

    Change chart type to a **Donut** chart.

    ![](images/500/img_5c_2_3.png " ")

    Move **Customer Age Group** to **Color**.

    ![](images/500/img_5c_2_4.png " ")

    Select **Order Amount** and **Customer Country**. While the attributes are selected, right click and select **Pick Visualization**.

    ![](images/500/img_5c_2_5.png " ")

    Choose the **Map Chart**.

    ![](images/500/img_5c_2_6v2.png " ")

    Your canvas should reflect the picture below:

   ![](images/500/img_5c_2_7.png " ")

    >Navigate to settings section and select the data layers section. Here you can also adjust the map layers, the layer type, and transparency of the map.

    >No changes need to be made to the data layers section.

    ![](images/500/img_5c_2_6.1.png " ")
    Select **Order Amount** and **Customer Gender**. While the attributes are selected, right click and select **Pick Visualization**.

   ![](images/500/img_5c_2_8.png " ")

    Choose the **Pie Chart**.

   ![](images/500/img_5c_2_9v2.png " ")

    Right-click the **Pie Chart** and select **Color** then **Manage Assignments**.

   ![](images/500/img_5c_2_10v2.png " ")

    Choose the color pink for F and the color royal blue for M.

   ![](images/500/img_5c_2_11.png " ")

   ![](images/500/img_5c_2_12.png " ")

    Move pie chart under the donut chart.

   ![](images/500/img_5c_2_13.png " ")

    Name the canvas “Customers” and save the project.
   ![](images/500/img_5c_2_14.png " ")

## Using the Explain feature to create a visualization

The **Explain** feature allows you to uncover insights and patterns about a particular column within a data set.

1. Right-click the **Category** attribute and selected **Explain Category**.

   ![](images/500/img_5d_1_1.png " ")

2. Look at **Explain Category** window and observe some the basic insights.

   ![](images/500/img_5d_2_1.png " ")

  The **Explain** feature parses the data set and presents different insights about the **Category** column. Listed below is a description of what **Basic Facts**, **Key Drivers**, **Segments** and **Anomalies** entail:

>**Basic Facts** - Shows basic distribution of the data element (attribute or measure) values across the data set and its breakdown against each one of the measures in the data set.

>**Key Drivers** - Shows data elements (attributes or measures) that are more highly correlated to the outcome for the selected data. You will see charts showing the distribution of the selected attribute value across each of the correlated attributes values.

>**Segments that Explain** - Shows segments or group in the data set, after examining all the records that can predict the value of the selected data element. You can select a particular segment or group and then continue to analyze it.

>**Anomalies** - Shows group of anomalies or unusual values in the data set that you can relate to the selected data element (attribute or measure). You can review and select particular group of anomalies.

3. Add a visualization to the the canvas using the explain feature.

    Select the check on the right corner of the visual and click **Add Selected**.

    ![](images/500/img_5d_3_1.png " ")

    If you've successfully added the visualization, your canvas should reflect the image below.

    ![](images/500/img_5d_3_2.png " ")

    Delete the **Explain Category** canvas by right clicking the tab and selecting **Delete Canvas**.

    ![](images/500/img_5d_3_3.png " ")

[Continue to Part 6](/Oracle-Analytics-Cloud-Workshop/?lab=part-6-machine-learning)