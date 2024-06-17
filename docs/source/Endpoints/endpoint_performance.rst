=====================
Scaling Endpoint
=====================

Scaling Cloud Endpoint
===========================

This section describes to you how to scale up or down a Bumblebee Endpoint for cloud deployment. 
It applies to AWS and Azure. The use case is to connect an VPC or VNet to an App Service on-prem or in the cloud. 
For how to configure an Bumblebee Endpoint, refer to How to create an Endpoint for consumers in AWS VPC


When you first launches a Bumblebee endpoint for AWS or Azure, the endpoint size is 1, 
it has a sustained throughput of 500mbps with a burst rate to 2Gbps. Here are the steps to size up or down. 


1. Login to Bumblebee portal
#. At the left navigation bar, click Endpoints
#. Select the Endpoint of interest, click Actions -> Resize Endpoints
#. Select Size Up to increase the size by 1, select Size Down to decrease the size by 1. 
#. Click Confirm. 



The current maximum number of size for the Endpoint is 500 which is equivalent to 250Gbps. If you need anything beyond this throughput, contact support@bumblebeenet.com


Each additional size is billed the same as one Endpoint. 

Scaling on-prem Endpoint
===========================

On-prem Endpoint can be scaled out by deploying more Endpoint Nodes in the same Endpoint group. 

|endpoint_node_group|

Step 1: Create a new endpoint node
-----------------------------------------

1. Login to the Bumblebee portal
#. Click Endpoint Nodes on the main navigation bar
#. Click Create Endpoint Node
#. Enter a name for the Endpoint Node name
#. For Endpoint Node Group, select Use Existing
#. Select one node group
#. Click Create Endpoint Node
#. Click Prepare OVA for Download
#. Click Download 
#. Install the OVA in the same on-prem location as the already installed node. It does not need to be on the same subnet. 
#. Power up the OVA. 
#. On the Bumblebee console, you should see it registered and in up state. If it does not come up, follow up the 
    instructions `here <https://bumblebee-networks-bumblebee-docs.readthedocs-hosted.com/en/latest/EndpointNodes/troubleshoot_endpoint_node.html>`_ to troubleshoot. 

Step 2: Create a new endpoint
---------------------------------

Follow the instructions `here <https://bumblebee-networks-bumblebee-docs.readthedocs-hosted.com/en/latest/EndpointNodes/create_endpoint_node.html>`_ to create a new Endpoint for the same App Service on the newly deployed Endpoint Node. 


Hosts initiated traffic will be load balanced to different Endpoints from this point on. 

|endpoint_node_group| image:: media/endpoint_node_group