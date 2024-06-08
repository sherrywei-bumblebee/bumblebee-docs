=======================================
Multi-Hosting for site redundancy
=======================================


Introduction to Multi-Hosting for redundancy
=================================================

Bumblebee App Services and Endpoints can be deployed in clusters to both scale out and 
provide high redundancies. 


There are scenarios where the application or entire site or region go down, and for such situations 
Bumblebee Networks provides the Multi-Hosting capability to redundancies to a backup site. 
The diagram below illustrates a scenario where an on-prem application or the data center go down, with Multi-Hosting configured, 
Endpoints automatically re-connect to the backup deployment, and in this diagram the backup deployment is in AWS. 


|multi_hosting_illustration|



In the above diagram, the primary App Service is in the data center and the backup in cloud. 
Below is another example where the deployment failover to a different cloud region. 

|multi_hosting_cloud_failover|

There maybe multiple backups in the priority order. 


If the second hosting site is on-prem, you need to create, download and install a service node to the site. 


Configuration Steps 
=====================

The following are the steps to configure Multi-Hosting.


1. Login to Bumblebee portal.
#. At the left navigation bar, click App Services.
#. Click the App Service you wish to create multi-hosting sites.
#. Click the Multi-Hosting tab.
#. Clicking Add Hosting
#. Select the Hosting location, on-prem, AWS or Azure
#. 

    - If you select on-prem, enter the application FQDN name or IP address at the new hosting site, select a service node group in the new hosting site. Click Create. This configuration is similar to create an App Service for on-prem. Refer to this article if you need additional information. 
    - If you select AWS, select the region for the new hosting, enter the AWS Endpoint Service name for the new hosting, click Create. This configuration is similar to create an App Service for AWS. Refer to this article for additional information. 
    - If you select Azure, select the region for the new hosting, enter the Azure Private Link Service ID for the application in the new hosting VNet. This configuration is similar to create an App Service for Azure. Refer to this article for additional information. 

#. Done

Visibility and Troubleshooting
=================================

Once you have created a new hosting, you should see it listed on the Multi-Hosting page. The new host Admin State should be "available" and the Op State should be "up".


On the Endpoints tab under a selected App Service, you should see a field Hosting ID to each connected Endpoints. This field indicates which hosting the endpoint is connected to. 


Current Limitations
========================

Currently when an App Service is configured, it takes the highest priority, priority 1. 
Each new hosting created takes lower priority according to the sequence of creation. 
Currently you cannot change the priority order without deleting the hosting and create again. 
The work around is to create the hosting sequentially based their fail over priorities. 
For example, the first hosting is the primary, the seconds hosting takes over when the first one fail, 
and the third hosting takes over when the second one fail. 


Another limitation is there is no automatic fail back. Once hosting switches to, say, 
a lower priority site, it stays there until it fails and it then switches back to the primary. 


The third limitation is the multiple hosting sites cannot handle traffic simultaneously. 
The traffic handling is strictly in the priority order. 