Embedded URL in power BI for Custom Report
Approach 1
In Power BI 
Please follow the steps below to embed the URL.
1.	In Power BI desktop, create a custom table with column/measure URL.
2.	Column/ Measure value should be like below.
For example,
a.	URL = https://www.microsoft.com/en-in/
3.	Create a blank visual, insert a text box/blank button. I choose Blank Button
 
 ![image](https://github.com/user-attachments/assets/666ce724-4ff4-4718-a2f1-28ba74e060bb)

4.	In Format pane, Enable the action, select web URL option from Type.
 ![image](https://github.com/user-attachments/assets/1e649726-6c21-476a-8817-9b3c6c50808f)


5.	Go to web URL formula, select the URL column which we created.
 ![image](https://github.com/user-attachments/assets/26a3f0cf-741b-4de3-b634-250d4dbe25c3)

6.	Click ok.
7.	After formatting style, text the button looks like below.
 ![image](https://github.com/user-attachments/assets/999da650-7409-4114-bb95-ad18dc59961e)

8.	Save and publish the report in Power BI service.
9.	After we clicked the button, it will open a new tab with the given URL.
    
Power BI Limitation.
Power BI does not support opening URLs in the same window. when you embed your report in a web application. This is because Power BI embeds links with the target= “_blank” attribute, which means that all links will be opened in a new tab1.There is no direct way to change this behavior, as the browser will not allow you to access the embedded iframe due to the CORS policy1.
 Approach 2
In Power Apps
Please follow the steps below to embed the URL.
1.	In Power Apps, Create a blank canvas app.
2.	Choose Form, create a screen and insert the button from the insert option.
 ![image](https://github.com/user-attachments/assets/be33e9d5-892a-4046-b9eb-2c732fb7315c)


3.	Insert a button and label. Add suitable text/title.
4.	Select the button, in the formula bar, onSelect property.

To open the URL in the same window

5.	Add launch function to open the URL in the same window.
For Example - Launch ("https://www.example.com”, {}, LaunchTarget.Replace);

To open the URL in the new window

6.	Add launch function to open the URL in the new window.
For Example – Launch ("https://www.example.com);
7.	Save and test it.
8.	After testing, click the publish button available on the top to publish the app.
 ![image](https://github.com/user-attachments/assets/32046c28-c3a7-4c33-aa89-0768f377662e)

![image](https://github.com/user-attachments/assets/dad8cd22-d8cc-46ab-808b-2f8557ebcca6)

 

9.	Go to the home page, select Apps, we will see the list of APPs which we have created so far.
10.	Select the radio button and click the play button.


Approach 3
Integrate Power Apps in Power BI Desktop

Please follow the steps below to embed the URL.
1.	In Power BI Desktop, select power apps visual from the visualization Pane.
 ![image](https://github.com/user-attachments/assets/690a4562-9609-42d5-98c9-b209fe64113d)

2.	Select any column from data fields.
 ![image](https://github.com/user-attachments/assets/bdbed1c4-d38c-4d89-a501-8efa7bf03010)


3.	It will ask to choose app or create new, when we click on create new app, it will navigate to Power Apps site.
4.	If you choose to create an app, you can choose in which environment to create it.
5.	Create a new canvas app which we already cover in approach 2. Follow the same.
6.	Once app creation is done, we need to select choose app option.
7.	A list of apps will be shown, we can choose the app which we created/ suitable as per our requirement.
8.	Save and publish the report in power BI Service.
9.	After publishing the report, click the button and it will open the new tab with the given URL.
Power Apps LaunchTarget function limitation

Using a LaunchTarget with any value other than New in embedded scenarios (for example, Power BI or SharePoint) is not supported and may result in unexpected behavior.  In the future, this behavior may change, or may cause an error.


For more references:
Launch and Param functions in Power Apps - Power Platform | Microsoft Learn
Solved: PowerBi Embedded Open WebUrl in same Tab - Microsoft Fabric Community
Power Apps visual for Power BI - Power Apps | Microsoft Learn
