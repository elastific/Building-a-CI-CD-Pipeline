# Overview

In this project, we will build a Github repository from scratch and create a scaffolding that will assist us in performing both Continuous Integration and Continuous Delivery. We'll use Github Actions along with a Makefile, requirements.txt and application code to perform an initial lint, test, and install cycle. Next, we'll integrate this project with Azure Pipelines to enable Continuous Delivery to Azure App Service.

## Project Plan
to follow DevOps best practices, we have built a KANBAN board in Trello (link is provided below). we have also built a complete project plan spreadsheet showing quarterly goals as well as yearly goals. The second tab in teh spreadsheet also shows the tasks need to be done in order to achieve the desired goals in first quarter (link to spreadsheet is provided below):

* https://trello.com/b/EyCoP9U9/project-2-building-a-ci-cd-pipeline
* https://1drv.ms/x/s!Avgo3Dz-bhJ9mOcUELSVukJ9XOCAUg?e=98GCw0

## Instructions

* Architectural Diagram (Shows how key parts of the system work)>

https://1drv.ms/u/s!Avgo3Dz-bhJ9mOl_FuJ-x4UP5OZcSQ?e=b7Akb3

To be able to run the python project, you need to first clone the repo using SSH or HTTP provided in the page (https://github.com/elastific/Building-a-CI-CD-Pipeline).

You also need to make sure you build a virtual environment either on your local machine (using conda or venv) that runs python 3.5. When the venv is setup, make sure to activate it, then install all the dependensies listed in requirements.txt file (could be via `pip isnatll -r requirements.txt` or `make install`).
When you first run the app.py in a terminal, you need to open up a second terminal to be able to test (run make_prediction.sh for local, or make_predict_azure_app.sh for Azure Cloud Shell).

* Project running on Azure App Service: a link to a screenshot is provided below:

https://1drv.ms/u/s!Avgo3Dz-bhJ9mOlx0mycH4FKoAs7qA?e=jHCzEk

* Project cloned into Azure Cloud Shell: links to screenshots are provided below:

https://1drv.ms/u/s!Avgo3Dz-bhJ9mOdHAePgvkV83gIYrw?e=A9h4b0

https://1drv.ms/u/s!Avgo3Dz-bhJ9mOdHAePgvkV83gIYrw?e=myH4hq

* Passing tests that are displayed after running the `make all` command from the `Makefile`: a link to a screenshot is provided below:

https://1drv.ms/u/s!Avgo3Dz-bhJ9mOdm44_zvMqbX3Ef_A?e=E4UKAV


* Output of a test run: a link to a screenshot is brought below:

https://1drv.ms/u/s!Avgo3Dz-bhJ9mOlx0mycH4FKoAs7qA?e=mH4oBQ

* Successful deploy of the project in Azure Pipelines: 

link here (https://1drv.ms/u/s!Avgo3Dz-bhJ9mOlyF4hav1guLl-RJQ?e=8p3lMX)

* Running Azure App Service from Azure Pipelines automatic deployment:


* Successful prediction from deployed flask app in Azure Cloud Shell.  [Using this file as a template for the deployed prediction](https://github.com/udacity/nd082-Azure-Cloud-DevOps-Starter-Code/blob/master/C2-AgileDevelopmentwithAzure/project/starter_files/flask-sklearn/make_predict_azure_app.sh). A link to a screenshot is provided below:

https://1drv.ms/u/s!Avgo3Dz-bhJ9mOlrgAA4drs1vaeG0Q?e=lwfhi6

the test run results are also put here as text:

$ sh make_prediction.sh
Port: 5000
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   260  100    48  100   212    123    544 --:--:-- --:--:-- --:--:--   668
{
  "prediction": [
    20.35373177134412
  ]
}

* Output of streamed log files from deployed application

$ sh make_prediction.sh
Port: 5000
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   260  100    48  100   212    123    544 --:--:-- --:--:-- --:--:--   668

> 

## Enhancements

- The Application webpage is extremely simple and has no way of outputting the prediction in the page, we can work on that.
- The model has been built using rather old version of scikit-learn that has stopped supporting some of the modules used in the model, so a re-train of the model seems inevitable.
- Tests done using Pytest are all trivial, we could build and implement some serious tests
- a mobile app could be built
- technical reference documentation could be developed and published
- having music, illustrations, animations, etc added to the webpag 


## Demo 

here is a link to our demo video:
https://1drv.ms/v/s!Avgo3Dz-bhJ9mO02ghUYueI1wswVdw?e=yHwTwY


![Python application test with Github Actions - v2](https://github.com/elastific/Building-a-CI-CD-Pipeline/workflows/Python%20application%20test%20with%20Github%20Actions%20-%20v2/badge.svg)
