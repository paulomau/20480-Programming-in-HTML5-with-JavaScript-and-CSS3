# Module 9: Adding Offline Support to Web Applications

# Lesson 2: Adding Offline Support by Using the Application Cache

### Demonstration: Adding Offline Support to Web Applications

#### Preparation Steps 

1. Ensure that you have cloned the 20480C directory from GitHub. It contains the code segments for this course's labs and demos. https://github.com/MicrosoftLearning/20480-Programming-in-HTML5-with-JavaScript-and-CSS3/tree/master/Allfiles.

#### Demonstration Steps

1.	Read the Lab Scenario to students and point out that they should read each scenario before attempting the lab for a module.
2.	Point out to students that the Exercise Scenario for each exercise contains a description of what they will accomplish in the exercise, and is also essential reading.
3.	Start Visual Studio, and open the **ContosoConf.sln** solution in the **Allfiles\Mod09\Labfiles\Solution\Exercise 2** folder.
4.	In Solution Explorer, expand the **ContosoConf** project, and then double-click **appcache.manifest**.
5.	In the Code Editor window, scroll through the file and explain that it lists the items that will be cached by the web browser.
6.	In Solution Explorer, expand the **scripts** folder, and then double-click **offline.js**.
7.	In the Code Editor window, find the following code:
    ```javascript
        if (!navigator.onLine) {
            hideLinksThatRequireOnline();
        }
    ```
8.	Explain that this statement detects whether the browser has a network connection. If it does not, the **hideLinksThatRequireOnline()** function modifies the links in the navigation bar to ensure that pages that require network connectivity (such as the **Location** and **Register** pages) do not appear.
9.	In Solution Explorer, expand the **scripts** folder, expand the **pages** folder, and then double-click **schedule.js**.
10.	In the Code Editor window, find the **setStar()** function. Point out that this function saves information about sessions that the user has selected (by clicking the star icon) to local storage, and also posts this information to the web server. Similarly, the **unsetStar()** function removes information about selected sessions from local storage. In this way, the user can still record which sessions they are interested in, even if the browser does not have a network connection.

©2018 Microsoft Corporation. All rights reserved.

The text in this document is available under the  [Creative Commons Attribution 3.0 License](https://creativecommons.org/licenses/by/3.0/legalcode), additional terms may apply. All other content contained in this document (including, without limitation, trademarks, logos, images, etc.) are  **not**  included within the Creative Commons license grant. This document does not provide you with any legal rights to any intellectual property in any Microsoft product. You may copy and use this document for your internal, reference purposes.

This document is provided &quot;as-is.&quot; Information and views expressed in this document, including URL and other Internet Web site references, may change without notice. You bear the risk of using it. Some examples are for illustration only and are fictitious. No real association is intended or inferred. Microsoft makes no warranties, express or implied, with respect to the information provided here.
