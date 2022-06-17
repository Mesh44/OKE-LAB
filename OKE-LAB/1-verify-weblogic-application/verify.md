# Lab 1: Verify Weblogic Application



## Introduction

This workshop uses the **WebLogic Operator** Demo app- a simple JSP-based WebLogic application you created in the prerequisite [**Migrating WebLogic Server to Kubernetes on OCI**](https://apexapps.oracle.com/pls/apex/dbpm/r/livelabs/workshop-attendee-2?p210_workshop_id=567&p210_type=2&session=102696148940850) workshop. Verify the WebLogic Operator application is running and ready.  
Estimated time: 5 minutes

#### Objectives

*   Ensure the WebLogic Operator Demo application is running



#### Prerequisites

*   Completion of the [**Migrating WebLogic Server to Kubernetes on OCI**](https://apexapps.oracle.com/pls/apex/dbpm/r/livelabs/workshop-attendee-2?p210_workshop_id=567&p210_type=2&session=102696148940850) workshop, Tasks 1, 2, 3 and 4.



## Task 1: Verify the application in a browser

1.  Click the navigation icon in the top left corner (three bars) in the Oracle Cloud console, and choose **Developer Services** > **Kubernetes Clusters (OKE)**.

![](attachments/4157037443/4157037444.png)

1.  Locate the compartment you created the Kubernetes cluster when you performed the prerequisite [**Migrating WebLogic Server to Kubernetes on OCI**](https://apexapps.oracle.com/pls/apex/dbpm/r/livelabs/workshop-attendee-2?p210_workshop_id=567&p210_type=2&session=102696148940850) workshop. Then click the name of the cluster.

![](attachments/4157037443/4157037445.png)

1.  On the Cluster Details page, click the **Access Cluster** button.

![](attachments/4157037443/4157037446.png)

1.  Select **Cloud Shell Access**, then click **Launch Cloud Shell**.

![](attachments/4157037443/4157037447.png)

1.  Look at the bottom of the page, and you will see a Cloud Shell window and command prompt ready for input.

![](attachments/4157037443/4157037448.png)

1.  1.  In the **Access Your Cluster** page that is still opened at the upper side of console, locate the textbox with the OCI command, and click **Copy**.

![](attachments/4157037443/4157037449.png)

1.  1.  Paste the command into the Cloud Shell and execute. It configures the Cloud Shell session to work with the cluster.

![](attachments/4157037443/4157037450.png)  
***NOTE***: Save the command to a text file on your laptop, and execute it every time when you start a new Cloud Shell session, while working the labs in this workshop.

1.  1.  In the Cloud Shell, run the following command.

*   kubectl get svc --all-namespaces

The output will be similar to the image below. The namespace of the WebLogic Server services used in the WebLogic workshop is ***sa******mp******le-domain1-ns*** by default.  
![](attachments/4157037443/4157037451.png)

1.  1.  Within the same command output, locate the LoadBalancer service. Note down the External-IP.

![](attachments/4157037443/4157037452.png)

1.  1.  On your computer, open a new browser tab and access the application with the following URL pattern:

http://<External IP of the Load Balancer>/opdemo/?dsname=testDatasource  
Make sure the WebLogic Operator Demo application launches as in the image below.  
![](attachments/4157037443/4157037453.png)

1.  If you have not set up the application yet, or you cannot start the application, please visit the [**Migrating WebLogic Server to Kubernetes on OCI**](https://apexapps.oracle.com/pls/apex/dbpm/r/livelabs/workshop-attendee-2?p210_workshop_id=567&p210_type=2&session=102696148940850) workshop, and complete the tutorials from the Task 1 to Task 4.
