Getting Started and FAQs
=========================

Getting Started FAQs
-----------------------

Where do I start if I am the provider of an application?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Click App Services to create an App Service for your application. 

If your application is located on-prem, follow the instructions to create an App Service for an on-prem app 
If your application is located in AWS, follow the instructions to create an App Service for an AWS app. 
If your application is located in Azure, follow the instructions to create an App Service for Azure app. 

Where do I start if I am the consumer to an application?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Click Endpoints to create an Endpoint to an App Service. Make sure you have the App Service ID from the application provider. Follow the instructions to create an Endpoint. 


What is the end to end workflow?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Check out this tutorial: end-to-end configuration workflow. 


General FAQs
----------------

What does Bumblebee Networks do?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Bumblebee Networks provides a Global Private Link service securely connecting private applications.   


We try to build a better tool for network engineers and application owners by bringing the experience of cloud networking to on-prem and everywhere. For example, if you have worked with AWS PrivateLink or Azure Private Link, you see how easy it is to connect a VPC to applications in different VPC or in different accounts, which otherwise could be quite difficult as the VPCs' network address ranges overlap. However if you look at on-prem networking for connecting different locations and customers, such scenario typically requires using BGP, IPSec and NAT to solve. These technologies have been around for a long time, complex to manage and require in depth specialty knowledges. We try to change that by giving customers the same experience they have come to enjoy in the cloud networking to on-prem.


To learn more, check out The story of Bumblebee Networks.


What does marketplace mean for Bumblebee Networks?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you have a private application and register it on the Bumblebee Networks platform, anyone who wishes to consume this application can come to the platform and request access. Once you approve them, network connectivity is built and traffic passes through Bumblebee Networks. 


What are the use cases for the platform?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

B2B (Extranet) Networking. If you have a business application that your customers and partners need to access securely, you can register your application on the Bumblebee platform. Your customers and partners make requests on the platform and upon your approval they are allowed access. The consumers are authenticated and authorized, the traffic is encrypted. 
Branch office networking. If you have remote offices or physical stores that need to send data or access applications in the data center, deploy Endpoint Node in these locations and build authenticated and authorized secure connectivity to these applications. 
Global Private Link for multi-cloud and cross region. Extend the native PrivateLink service to cross region and multi-cloud, simple to use and all cloud native. 
VPN Replacement. Anytime you need to build a secure network connectivity between networks with IPSec, you can build using Bumblebee instead. 
Overlapping Network Addresses. Any time you need to build connectivity for application access from networks with overlapping network addresses, use Bumblebee  platform to build secure connectivity without the hassle of IPSec and NAT. 
IP Whitelisting. If you IP Whitelist public IP addresses to restrict application access for security reason, you are instead to use Bumblebee platform to authenticate and authorize each customer with no on-going maintenance headache of every changing public IP addresses. 

Is there a configuration tutorial?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Yes. Read Tutorial: end-to-end configuration workflow. 


What is the Bumblebee Networks packet flow?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can read the information in the Bumblebee Networks packet flow document. 


App Services
---------------

How do I register my application on Bumblebee Networks?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You register your application by creating an App Service construct on the platform. We currently support two scenarios: application on-prem and application in AWS. Follow the instruction on How to create an App Service for on-prem applications for connecting to an on-prem application. Follow the instructions on How to create an App Service for AWS applications. 


What are the deployment requirements for Service Node?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Check out Endpoint Node and Service Node deployment requirements. 


How to troubleshoot a Service Node?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Check out the document on How to troubleshoot an Endpoint Node or Service Node. 


How to increase App Service performance?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

For App Service on-prem, add a new Service Node by following the instructions here. 

For App Service in AWS, contact support@bumblebeenet.com 



Endpoints 
------------

How do I make request to access application on Bumblebee Networks?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You make request to access applications by creating Endpoint construct on the platform. We currently support accessing from on-prem scenario. To create an Endpoint, follow the instruction How to create an Endpoint. 


What are the deployment requirements for Endpoint Node?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Check out Endpoint Node and Service Node deployment requirements. 


How to add more Endpoints on an Endpoint Node?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

An Endpoint Node can host multiple Endpoints each associating with different App Services. Check out How to add more Endpoints on an Endpoint Node using secondary IPs. 


How to troubleshoot an Endpoint?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Check out How to troubleshoot Endpoint reachability. 


Can I create an Endpoint Node on my MAC?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Yes. While Endpoint Node is a virtual machine in a OVA file format built for vmware vCenter or vSphere host client, you can try out the Endpoint Node on your PC or MAC if they are Intel processor based, as long as you install vmware Workstation or vmware Fusion. 


For ARM processor based MAC, check out the instructions on how to convert the OVA to emulate Intel processor. 


How to troubleshoot an Endpoint Node?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Check out How to troubleshoot Endpoint Node or Service Node. 


How to increase Endpoint performance?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Check out How to increase Endpoint performance by scaling out.  




