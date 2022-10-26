# Project 4 repository:
This repository contains a UiPath project that is used to run User Acceptance Tests on the connected office web app. The UiPath project is separated into different workflows, it much easier to test each workflow on its own. All the workflows is then combined into one in the main sequence to do all of the testing. To run the project to test the web app go to the UiPath Orchestrator link and click on run process. The Automation will start and perform the UATs.

##Steps of the process:
- First the test data is read from excel into DataTables.
- Next is login, the automation navigates to the following website: ()[https://connectedoffice-devicemanagement.azurewebsites.net/]
