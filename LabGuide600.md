## Part 6 – Predicting Subscriptions - Machine Learning

Key takeaways from this lab:
- Using the **Machine Learning** abilities of OAC

## What is Machine Learning?
Machine learning, at its most basic, is the usage of algorithms to parse data, learn from it, and then make a determination or prediction about something. The Machine Learning abilities of OAC allow you to make predictions based on your data set. Data Visualization also provides scripts to train data models that you can add to other data sets to predict trends and patterns in data.

## Scenario

When customers purchase products through a partner, KoolKart would like to include a discount coupon in the shipping confirmation email as an incentive for users to subscribe to the KoolKart mailing list. Now, Isla Stuart, who is a Digital Marketing Specialist, has to understand the customer demographics and figure out how big the incentive should be.

To do this, Isla  has already obtained 4 different data sets: Orders, Customers, Subscriptions and Partner Sales. She wants to look at subscription patterns on the KoolKart website and develop a model that looks at past subscription data to determine how Customer Age Group, Customer Gender, Customer Country and  purchased Product Category influence the likeliness to subscribe.

Isla knows that she needs to use KoolKart Orders and KoolKart Customers data sets together. Most importantly, she decides to utilize the Data Flow functionality of OAC that allows her to create a data set tailored to her needs. Let's start!

## Creating a Dataflow and Predicting Subscriptions

>Isla now wants to predict the likeliness of new customers to subscribe and to directly correlate the amount of the coupon to how much they are likely to subscribe anyway.

>She wants to take advantage of existing data gathered by looking at subscription patterns on KoolKart website and to develop a model that looks at past subscription data to determine the influence of Customer Age Group, Customer Gender, Customer Country and purchased Product Category into the likeliness to subscribe.

1. Use **Data Flow Editor** to create model.

    Now, click on the Home button.

    ![](images/500/img_5a_1_1v2.png " ")

    Select **Create** and then **Data Flow**.

    ![](images/500/img_5a_1_2.png " ")

    Select **Create Data Set** to load in the Excel file.

    ![](images/200/img_2a_2_2.png " ")

    Download the <a href="https://github.com/oracle/learning-library/raw/master/workshops/dvcs-5/Exercise%20Files/KoolKart%20Subscriptions.xlsx">**KoolKart Subscription.xlsx**</a> file.

    Select **Drop data file here or click to browse** and choose the **KoolKart Subscription** data set.

    ![](images/500/img_5e_1_4.png " ")

    Select **Add** to add the **KoolKart Subscription** data set.

    ![](images/500/img_5e_2_1.png " ")

2. Add a Binary Classifier to the **Data Flow**.

    Make sure you're on the **Data Flow Steps** tab.

    ![](images/500/img_5a_2_1.png " ")

    Select **Train Binary Classifier** and drag it to the **+** in front of the **KoolKart Subscription** data set.

    ![](images/500/img_5e_2_2.png " ")

    Select the **Naïve Bayes for Classification** script from the menu that opens up.

    ![](images/500/img_5e_2_3v2.png " ")

    Your data flow should look something like this:

    ![](images/500/img_5e_2_4.png " ")

    Set a prediction target by clicking on **Select a column** and select **Subscribed**.

    ![](images/500/img_5e_2_5.png " ")

    Click **Save Model** and name the model **Subscribed Prediction Model**.

    ![](images/500/img_5e_2_6.png " ")

    Save the Data Flow and name it **Subscribed Predictions** and select OK.

    ![](images/500/img_5e_2_7.png " ")

    Click **Run Data Flow** to execute the data flow.

    ![](images/500/img_5e_2_8.png " ")

3. Create a Scenario that will predict subscription confidence.

    Return to the home page.

    ![](images/500/img_5a_1_1v2.png " ")

    Open the **Sales & Forecast Project**.

    ![](images/500/img_5e_3_1av2.png " ")

    Create a new canvas and rename it to **Subscription Prediction**.

    ![](images/500/img_5e_3_1.png " ")

    ![](images/500/img_5e_3_2.png " ")

    Download the <a href="https://github.com/oracle/learning-library/raw/master/workshops/dvcs-5/Exercise%20Files/KoolKart%20Partner%20Sales%20.xlsx">**KoolKart Partner Sales.xlsx**</a> file.

    Click the **+** next to the **Data**, select the **Add Data Set** option.

    ![](images/500/img_5e_3_3.png " ")

    Select **Create Data Set** to load in the Excel file.

    ![](images/200/img_2a_2_2.png " ")  

    Select the **Drop data here or click to browse** and navigate to the **KoolKart Partner Sales** file or drag and drop the file onto the file icon.

    ![](images/500/img_5e_3_5.png " ")

    Turn **OrderID** into an attribute.

    ![](images/500/img_5e_3_6.png " ")

    Return to the **Visualize** tab and click the **+** next to the **Data**.

    Select the **Create Scenario** option.

    ![](images/500/img_5e_3_7.png " ")

    Once the **Create Scenario – Select Model** menu shows up, select the **Subscribed Prediction Model**.

    ![](images/500/img_5e_3_8.png " ")

    Once the **Create Scenario – Map Your Data** menu loads, select the **KoolKart Partner Sales** data set. Select **Done**.

    ![](images/500/img_5e_3_9.png " ")

    Select **Customer Name**. Press and hold the **Control(Windows)** or **Command(Mac)** key and click on **PredictionConfidence**. Then, right click and select **Pick Visualization**.

    ![](images/500/img_5e_3_10.png " ")

    Select **Pivot Table**.

    ![](images/500/img_5e_3_11v2.png " ")

    Drag **Subscribed Prediction** to the Color.

    ![](images/500/img_5e_3_12.png " ")

    >If you have successfully completed the steps, you will see the visualization below. From looking at the chart, we can predict which customers are more likely to get a subscription.

    ![](images/500/img_5e_3_15.png " ")

Congratulations! You have completed the workshop.

In this workshop, we were able to quickly assess the effectiveness of your social media campaigns on sales and how sales trends correspond to social media tone/sentiment. We also used OAC's machine learning abilities to predict the likelihood of customer's subscribing to KoolKart's mailing list.

This concludes our Oracle Analytics workshop.
