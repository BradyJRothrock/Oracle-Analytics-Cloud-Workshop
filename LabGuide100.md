## Part 1 - Getting Started with Oracle Analytics Cloud (OAC)


This section focuses on getting started with OAC and introducing students to the interface.

Key takeaways from this lab:
- Starting an OAC instance
- Learning and getting acclimatized to the interface

## Oracle Analytics Cloud

Oracle Analytics Cloud is a cloud-first analytics platform, providing fast and flexible analysis of any data from any source. It is built on the industry-leading Oracle Business Intelligence platform and Oracle’s top tier cloud infrastructure.

Oracle Analytics Cloud delivers scalability, high availability, state-of-the-art security, and operational simplicity. This combination of proven technologies, world-class infrastructure, broad data access, and deep analytic capabilities makes Oracle Analytics Cloud the best solution for every user.

The goal of today’s workshop is to introduce you to the data visualization capabilities included in OAC. We will be analyzing data using local Excel files. OAC also allows you to analyze data based on a pre-built OAC subject area or coming directly from a wide variety of sources. These can include Oracle SaaS applications (e.g. ERP Cloud), databases, and 3rd party applications (e.g. Salesforce), amongst others.

## What are Oracle Analytics?

Oracle Analytics is a tool that enables you to explore analytical data visually and individually. The capabilities are available both via a web-based interface (OAC) as well as via a local client (Oracle Analytics Desktop).

Oracle Analytics makes it easy to visualize your data, so you can focus on exploring interesting patterns and outliers. Just upload your data files or connect to a data source, select the elements you are interested in, and let Oracle Analytics find the best way to visualize it. Of course, you can also choose from a wide range of visualizations yourself if you want to look at your data in a specific way.

- **Creating visualizations is easy**. Your data analysis work is an individual experience in exploration and discovery that can also be shared with other users. Oracle Analytics enables you to experiment with a wealth of different options for how to view your data. During this experimentation process, you can find correlations, discover patterns, and see trends in your content.

- Oracle Analytics provides you with tools for faster and simpler assembly of detailed reports arranged together in an appealing and meaningful display. Oracle Analytics goes even further, to give you dynamic views for focused, exploratory interaction with your data.

## Oracle Analytics provides the following:

>**Guidance**: Grammar-centric approach to visualizations combined with powerful keyword search and pattern detection to aid all users making new discoveries.

>**Richness**: Robust visualization library and streamlined dashboard construction provide all the tools needed for constructing sophisticated analysis across many different perspectives of data.

>**Visual Grammar**: Visualizations automatically created and updated by applying visual grammar to data selections made by user. All visualization types share foundation in visual grammar.

>**Keyword Search**: All relevant artifacts are indexed for search. Unfamiliar data models can be intuitively accessed using keywords.

>**Pattern Brushing**: Sophisticated technique to highlight correlations between visualizations. Patterns highlighted across all components on the canvas.

>**Data Blending**: Combining two or more data sources for analysis.

## Provisioning an Oracle Analytics Cloud Instance

1. From any browser go to oracle.com/cloud/sign-in.html to access the Oracle Cloud.

    [https://www.oracle.com/cloud/sign-in.html](https://www.oracle.com/cloud/sign-in.html)

    ![](images/login-screen.png " ")

2.  Sign into the **Single Sing-On (SSO)** by clicking **Continue**. This is required because the **Identify Provider** will be required to create our Oracle Analytics Cloud Instance.  
*NOTE:  Do NOT click the Sign-In button, this will sign you in without your Identify Provider and you will not be able to create the instance.*

    ![](images/single-sign-on.png " ")

3. Enter your username and password and click on **Sign In**.

    ![](images/oracle-cloud-signin.png " ")

4. Once you log in you will see a page similar to the one below.  Click on the hamburger icon in the upper left corner to reveal the menu.

    ![](images/hamburger.png " ")  

5. Click on **Analytics** -> **Analytics Cloud**

    ![](images/menu.png " ")

6. On the next screen, click on **Create Instance**.

    ![](images/create-analytics-instance.png " ")

7. Now, give your instance a **Name**.

    ![](images/100/img_1a_7_3.png " ")
    
    Next, we will configure our instance. Click on the **Feature Set** dropdown.

    ![](images/100/img_1a_7_1.png " ")

    Choose **Self-service Analytics**  and leave the rest of the options as is.

    ![](images/100/img_1a_7_2.png " ")

    

8. Review your selections. Make sure your fields match the fields mentioned in the previous step. In case of issues, return to the previous screen and make the required changes. Then click **Create**.

    ![](images/100/img_1a_8_1.png " ")

9. Now, wait for the instance to be created. This can take up to half an hour.

    ![](images/100/img_1a_9_1.png " ")

10. Once created select **Analytics Home Page**.

    ![](images/100/img_1a_10_1.png " ")

    Doing so will take you to the OAC home page which we will be reviewing in the next section.

    ![](images/100/img_1b_1.png " ")

11. It's important to note that once we're done using the instance we need to **Stop** the instance or else it could use multiple dollars a day of our trial credits. Restarting the instance at a later time takes roughly 5 minutes.

    ![](images/100/img_1a_10_3.png " ")
## Reviewing the Home page and the primary menus

On logging into OAC, you will see the home page.

![](images/100/img_1b_1.png " ")  

1. Start by clicking on the hamburger menu in the top-left of the UI. This will open the drawer menu.

    ![](images/100/img_1b_1_1v2.png " ")

2. You can use this menu to navigate through the application.

    ![](images/100/img_1b_2_1.1v2.png " ")

    ![](images/100/img_1b_2_1.2v2.png " ")

    The application follows standard web and application interface protocols, thus supporting both left and right click interactions. In terms of general navigation, there are 4 key menus accessible at the top of the screen or via a hamburger menu in the top left (not all screens will show the top menu bar but the hamburger navigation is always available).

    >**Home**: Application start up page from where you can view existing projects, data sets, data flows or create new ones.

    >**Catalog**:  Collections of visualizations and the underlying data sources. **Folders** are simply means by which to organize projects.

    >**Data**: Display or create **Data Sets** (instances of data such as a specific Excel file);
        >> **Connections** (connections to data sources such as a database or SaaS application to pull data files); or
        >> **Data Flows** (ability to curate data from data sources including adding calculations, merging multiple sources, and managing columns).

    >**Machine Learning**: This page shows all the available machine learning models ready for use in projects.

    >**Jobs**: This page shows all the status of data replication, data flow, and sequence operations.

    >**Console**: Administrative menu for managing **Custom Plugins** (e.g. new types of analyses obtained from the Oracle Analytics Store or custom built), **Maps** layers (e.g. new backgrounds for map-based analyses) and other administrative tasks.

    >**Academy**: Home to important links to the OAC documentation and videos that help you accomplish common tasks in the OAC.

3. At the top-right of the UI, click on the **Create** button.

    ![](images/100/img_1b_3_1v2.png " ")

    This window allows you to create a Visualization project, a data set, a connection to an external source, a data flow, or a sequence.

Now that you can start and navigate around OAC, let’s get started with some analyses!

[Continue to Part 2](/Oracle-Analytics-Cloud-Workshop/?lab=part-2--basic-introduction-core-features)