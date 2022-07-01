# Lab 1: Verify Weblogic Application



## Introduction

This workshop uses the **WebLogic Operator** Demo app which is a simple JSP-based WebLogic application you created in the prerequisite [**Migrating WebLogic Server to Kubernetes on OCI**](https://apexapps.oracle.com/pls/apex/dbpm/r/livelabs/workshop-attendee-2?p210_workshop_id=567&p210_type=2&session=102696148940850) workshop. In this Lab you will verify the WebLogic Operator application is running and ready.  

#### Estimated time: 5 minutes

#### Objectives

*   Ensure the WebLogic Operator Demo application is running.



#### Prerequisites

*   Completion of the [**Migrating WebLogic Server to Kubernetes on OCI**](https://apexapps.oracle.com/pls/apex/dbpm/r/livelabs/workshop-attendee-2?p210_workshop_id=567&p210_type=2&session=102696148940850) workshop, Tasks 1, 2, 3 and 4.



## Task 1: Verify the application in a browser

1.  Click the navigation icon in the top left corner (three bars) in the Oracle Cloud console, and choose **Developer Services** > **Kubernetes Clusters (OKE)**.

![Image alt text](images/01.jpg "Image title")

2.  Locate the compartment you created the Kubernetes cluster when you performed the prerequisite [**Migrating WebLogic Server to Kubernetes on OCI**](https://apexapps.oracle.com/pls/apex/dbpm/r/livelabs/workshop-attendee-2?p210_workshop_id=567&p210_type=2&session=102696148940850) workshop. Then click the name of the cluster.

![Image alt text](images/02.jpg "Image title")

3.  On the Cluster Details page, click the **Access Cluster** button.

![Image alt text](images/03.jpg "Image title")

4.  Select **Cloud Shell Access**, then click **Launch Cloud Shell**.

![Image alt text](images/04.jpg "Image title")

5.  Look at the bottom of the page, and you will see a Cloud Shell window and command prompt ready for input.

![Image alt text](images/05.jpg "Image title")

6.  In the **Access Your Cluster** page that is still opened at the upper side of console, locate the textbox with the OCI command, and click **Copy**.

![Image alt text](images/06.jpg "Image title")

7.  Paste the command into the Cloud Shell and execute. It configures the Cloud Shell session to work with the cluster.

![Image alt text](images/07.jpg "Image title")

***NOTE***: Save the command to a text file on your laptop, and execute it every time when you start a new Cloud Shell session, while working the labs in this workshop.

8.  In the Cloud Shell, run the following command.
````
<copy>kubectl get svc --all-namespace</copy>
````


The output will be similar to the image below. The namespace of the WebLogic Server services used in the WebLogic workshop is ***sample-domain1-ns*** by default.  
![Image alt text](images/08.jpg "Image title")

9.  Within the same command output, locate the LoadBalancer service. Note down the External-IP.

![Image alt text](images/09.jpg "Image title")

10. On your computer, open a new browser tab and access the application with the following URL pattern:
```
http://(External IP of the Load Balancer)/opdemo/?dsname=testDatasource
```
Make sure the WebLogic Operator Demo application launches as in the image below.  
![Image alt text](images/10.jpg "Image title")
Refresh the browser and the Hostname should change.

11.  If you have not set up the application, or you cannot start the application, please visit the [**Migrating WebLogic Server to Kubernetes on OCI**](https://apexapps.oracle.com/pls/apex/dbpm/r/livelabs/workshop-attendee-2?p210_workshop_id=567&p210_type=2&session=102696148940850) workshop, and complete the tutorials from Task 1 to Task 4.
