# Project 4 repository:
This repository contains a UiPath project that is used to run User Acceptance Tests on the connected office web app. The UiPath project is separated into different workflows, as it much easier to test each workflow on its own. All the workflows is then combined into one in the main sequence to do all of the testing. The process can be runned from UiPath Orchestrator or from within the UiPath Studio app. The Automation will start and perform the UATs.

## Steps of the process:
- First the test data is read from excel into DataTables.
- Next is login, the automation navigates to the following website: [](https://connectedoffice-devicemanagement.azurewebsites.net/) and logs in with the credentials.
- After the login the testing is done. First on Zone then Category and lastly on Device.
- With the testing a loop is used to loop through the specific data table, then a workflow is invoked to perform the tests on the web app.
- The testing is done in specific order. First the item from the data table is created to test create and read, next some value is Updated by adding " - Edited" to the value to indicate a record has been updated. After all the values have been created and updated for zone, category and device the delete is tested. The delete process first tests the device then zone then category.
- The delete is done after all the elements has been created because there has to be a zone and category in order to select a zone or category from the drop down.
- The delete also starts with the device because if a zone or category is deleted before a device that is part of that zone or category the device is automatically removed.
- After each test the excel sheet "Test Results" is updated to reflect that the test was completed.
- After all the tests the process logs out of the web app and displays a message that testing has completed.

## Orchestrator:
The automation is published to Orchestrator in order to run the test from UiPath assistant or from Orchestrator itself. The process name is: Connected.Office.Web.Application.User.Acceptance.Testing. The other process is not related to this subject.
![image](https://user-images.githubusercontent.com/90188915/198055151-10815d4e-c008-47c9-8cc4-9d5f52d2a43c.png)

## Reference list:

- [References.docx](https://github.com/dennisvantonder/CMPG323-Project-4-31609988/blob/main/References.docx)
