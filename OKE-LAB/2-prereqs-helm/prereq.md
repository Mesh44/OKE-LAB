
# LAB 2: Prerequisites for installing OKE HELM Charts



## Introduction

In this lab, you will gather information which will be needed later to install the OKE HELM chart, create a compartment and log group to store logs from OKE  
Estimated time: ?  

#### Objectives

*   On boarding LA ¿ not DONE?
*   Create a compartment ¿ not DONE
*   Create a LA Log Group
*   Obtain and record information which will later be required in the values.yaml file, specifically
    *   Logging Analytics Namespace
    *   Kubernetes Cluster Name and Cluster ID





#### Prerequisites




## Task 1: Obtain Logging Analytics Namespace

For logs to be sent to Logging Analytics the Logging Analyics Namespace is required. Here we will locate the Namespace and copy it to a safe location so that we can paste it into the values.yaml file later.  

1.  From the main menu click on Observability & Manageability, on the right under Logging Analytics click on Administration


![](attachments/4157037466/4157037467.png)  


1.  From the Administration Overview page on the left under Resources section, click on select **Service Details**

![](attachments/4157037466/4157037468.png)

1.  Locate the Service Namespace. Copy the Service Namespace (in this case omcinternal) to a text file and save as you will need this later in the workshop

![](attachments/4157037466/4157037469.png)  
\*\*\*\*Above Image needs cropping \*\*\*\*  


## *Task 2. Obtain the Kubernetes Cluster name and Cluster ID*

1.  From the Main Menu go to **Developers Service** and then click on **Kubernetes Cluster (OKE)** on the right.

![](attachments/4157037466/4157037470.png)  


1.  From the next screen under Name, locate your Cluster Name and click on it.


![](attachments/4157037466/4157037471.png)  

1.  On the next screen locate the Cluster Name (in my case Ms-OKE-LA-LAB) and copy it to a text file. Also click **Copy** next to the Cluster ID and paste that value to a text file and save, as you will need these values later in the workshop.

![](attachments/4157037466/4157037472.png)  



































## *Task 3: Create a Log Group**.*

Why is the log group required?

1.  From the OCI menu, select **Observability and Manageability,** then **Administration** from the right side under Logging Analytics.


\*\*Need an image \*\*\*  

1.  From the **Logging** **Analytics Administration Page**, under Resources click on **Log Groups**

![](attachments/4157037466/4157037473.png)

1.  Click **Create Log Group** on the Log Groups page, ensuring you are in the correct compartment. (My my case it's SCP). Enter a Name of the Log Group n(in this case OKE-LA-LAB) and optional Description. Then click **Create**.

![](attachments/4157037466/4157037474.png)  


1.  After the Log Group has been created click on it.

![](attachments/4157037466/4157037475.png)  


1.  Locate the OCID for the group and click **Copy.** Paste and save the OCID to a test file as you will need it later.

![](attachments/4157037466/4157037476.png)
You may now [proceed to the next lab](#next).


## Acknowledgements
* **Author** - Ashwini R, Senior Member of Technical Staff
* **Contributors** -  Kumar Varun, Product Manager
* **Last Updated By/Date** - <Name, Group, Month Year>
