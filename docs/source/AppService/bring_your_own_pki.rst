=======================================================
Bring your own PKI
=======================================================

This document describes how to import your own certificates to the Bumblebee platform for encryption of 
data in flight. 


Bumblebee Endpoints and App Services are mutually authenticated for communication. 
The certificates are managed by the Bumblebee platform vault server.  
If you like to bring your own certificate you can do so by the Import External Certificate feature. 


The Import External Certificate applies to the Service Node Group level. This flexibility allows you choose which applications are critical and requires your own certificates. When a service node group is enabled with this capability, all applications associated with the App Services deployed in the Service Node Group use external certificates. 


Here are the configuration steps. 


1. Login to the Bumblebee console.
#. At the left navigation bar, click Service Nodes.
#. At the Service Nodes page, click Manage Node Groups on the right above the Service Nodes list. 
#. Select a Service Node Group, click Actions -> Import External Certificate
#. For Server Certificate filed, copy and pate in the server certificate for the app service side. 
#. For Private Key, copy and paste in the private key for decryption. 
#. For CA Chain, copy and paste the CA Chain associated with the server certificate. 
#. Click Save. (You may need to scroll down the pop up window to see the Save button)


|import_external_cert|



If you need to edit the above configuration due to, for example, expired certificate, go through the above steps again to make changes. 


To disable Import External Certificate, click Manage Node Group at the Service Node Group page, 
select the Service Node Group, click Actions -> Disable External Root CA. 

.. |import_external_cert| image:: media/import_external_cert