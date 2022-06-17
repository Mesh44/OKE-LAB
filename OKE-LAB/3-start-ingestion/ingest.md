
# LAB 3: Installing the OKE HELM Chart

## Introduction

*   Add details

Estimated time: ?  

##### Objectives

*   Download HELM
*   Install HELM
*   ?




##### Prerequisites

*   Ensure that Lab 2 – Prerequisites lab is completed
*   Also ?



## Task 1: Download HELM Chart.



##### Introduction

In this task we will download the Helm charts and ??  

1.  Go to [https://github.com/oracle-quickstart/oci-kubernetes-monitoring](https://github.com/oracle-quickstart/oci-kubernetes-monitoring)

In your browser

1.  Press Code and download the Zip file to your local desktop

![](attachments/4157037481/4157037482.png)  

## Task 2: Upload the OCI-Kubernetes-monitoring-main.zip to the Cloud shell

1.  Open the Cloud Shell by clicking the **\>\_** icon from the top right corner in the Oracle Cloud console.

![](attachments/4157037481/4157037483.png)

1.  From the Cloud Shell create a directory to store the downloaded file

mkdir ~/OKE-LAB  

1.  Click the navigation menu (three-bar icon) in the Cloud Shell title bar to open the menu. Then select **Upload**.

![](attachments/4157037481/4157037484.png)

1.  Click **select from your computer** link and select the Java agent installer file from your computer. This is the file that you downloaded in the earlier steps.


![](attachments/4157037481/4157037485.png)  


1.  Click **Upload**.

![](attachments/4157037481/4157037486.png)  


1.  Wait for the file transfer to complete.


![](attachments/4157037481/4157037487.png)  

1.  Verify the file has been transferred to your cloud shell area


ls oci-kubernetes-monitoring-main.zip  
![](attachments/4157037481/4157037488.png)  

## Task 3: Unzip download



1.  Move the zip file to OKE-LABS and unzip


mv oci-kubernetes-monitoring-main.zip OKE-LAB/; cd OKE-LAB/; unzip oci-kubernetes-monitoring-main.zip

1.  Once unzipped, move into the following directories, where you will see three directory folders

cd oci-kubernetes-monitoring-main/logan/; ls  
![](attachments/4157037481/4157037489.png)  







## Task 4: Configuring HELM Chart

In this section we will configure the values.yaml file with the information we obtained in the prerequires section.  

1.  Open Cloud shell
2.  cd ~/OKE-LAB/oci-kubernetes-monitoring-main/logan/helm-chart
3.  vi values.yaml



Within values.yaml locate the line :  
url:  
and add the location  
url: iad.ocir.io/ax1wgjs6b2vc/oci\_la\_fluentd:ol8-1.0  
url: iad.ocir.io/ax1wgjs6b2vc/oci\_la\_fluentd:0l8-1.0  




Within values.yaml locate the following lines and replace them with the information copied in the prerequisites (LAB2) section – ensure that the format of the file is not changed  


1.  Logging Analytics Namespace  
    ociLANamespace
2.  Logging Analytics Default Log Group ID  
    ociLALogGroupID
3.  Kubernetes Cluster ID  
    kubernetesClusterID
4.  Kubernetes Cluster NAME  
    kubernetesClusterName  


    For example:  

5.  Logging Analytics Namespace  
    ociLANamespace: omcinternal
6.  Logging Analytics Default Log Group ID  
    ociLALogGroupID: ocid1.loganalyticsloggroup.oc1.iad.amaaaaaae5xv5jiauggucqgs2kalzfbjtnbwhiuemwabq2rgmyei4yr7wybq
7.  Kubernetes Cluster ID  
    kubernetesClusterID: ocid1.cluster.oc1.iad.aaaaaaaak65vzol4lbb64jtudvufvgpfsv4nwirawjmj4fe6sca4n2fzjgqa
8.  Kubernetes Cluster NAME  
    kubernetesClusterName: MS-OKE-LA-LAB  
    Save the file.  
    Here is an example of my values.yaml file  
    ![](attachments/4157037481/4157037490.png)  

    ## Task 5: Install the helm chart.

    Now that you have populated the values.yaml file. It's time to install the helm chart.  

9.  Copy and paste the following, ensuring

mahesh\_k\_s@cloudshell:helm-chart(us-ashburn-1)$ helm install okelab -values ~/OKE LAB/oci-kubernetes-monitoring-main/logan/helm-chart/values.yaml ~/OKE-LAB/oci- Kubernetes- monitoring-main/logan/helm-chart  
The output should be like:  
WARNING: Kubernetes configuration file is group-readable. This is insecure. Location: /home/mahesh\_k\_s/.kube/config  
WARNING: Kubernetes configuration file is world-readable. This is insecure. Location: /home/mahesh\_k\_s/.kube/config  
NAME: okelab  
LAST DEPLOYED: Fri Jun 10 06:25:52 2022  
NAMESPACE: default  
STATUS: deployed  
REVISION: 1  
TEST SUITE: None  

## Task 6: Check the helm chart has been installed successfully


No check the helm chart has been successfully installed. Copy and paste the following.  
mahesh\_k\_s@cloudshell:helm-chart(us-ashburn-1)$ helm history okelab  
The output should be similar to:  
WARNING: Kubernetes configuration file is group-readable. This is insecure. Location:  
/home/mahesh\_k\_s/.kube/config  
WARNING: Kubernetes configuration file is group-readable. This is insecure. Location:  
/home/mahesh\_k\_s/.kube/config  
REVISION UPDATED STATUS CHART APP VERSION DESCRIPTION  
1 Fri Jun 10 06:25:52 2022 deployed oci-la-fluentd-1.0.2 2.0.3 Install complete

You may now [proceed to the next lab](#next).


## Acknowledgements
* **Author** - Ashwini R, Senior Member of Technical Staff
* **Contributors** -  Kumar Varun, Product Manager
* **Last Updated By/Date** - <Name, Group, Month Year>
