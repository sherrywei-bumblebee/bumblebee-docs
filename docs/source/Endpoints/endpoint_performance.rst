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

On-prem Endpoint can be scaled out by deploying more Endpoints in the same Endpoint group. 