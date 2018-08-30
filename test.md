# F5 CloudFormation Templates for Amazon Web Services (AWS) 

## NICs

Deploy a BIG-IP VE with the number of NICs you choose.

| **Description**                                    | **BYOL**                    | **BIG-IQ**               | **PAYG**                |
|----------------------------------------------------|-----------------------------|--------------------------|-------------------------|                                                                
| 1 NIC    **existing** stack                        | [README][1nicbyolrm]        | [README][1nicbigiqrm]    | [README][1nicpaygrm]    |
| 1 NIC    **production** stack                      | [README][1nicbyolrmpub]     | [README][1nicbigiqrmpub] | [README][1nicpaygrmpub] |
|                                                    |                             |                          |                         |
| 2 NICs   **existing** stack                        | [README][2nicbyolrm]        | [README][2nicbigiqrm]    | [README][2nicpaygrm]    |
| 2 NICs   **production** stack                      | [README][2nicbyolrmpub]     | [README][2nicbigiqrmpub] | [README][2nicpaygrmpub] |
|                                                    |                             |                          |                         |
| 3 NICs   **existing** stack                        | [README][3nicbyolrm]        | [README][3nicbigiqrm]    | [README][3nicpaygrm]    |
| 3 NICs   **production** stack                      | [README][3nicbyolrmpub]     | [README][3nicbigiqrmpub] | [README][3nicpaygrmpub] |
|                                                    |                             |                          |                         | 
| 3-8 NICs **existing** stack                        | [README][nnicbyolrm]        | [README][nnicbigiqrm]    | [README][nnicpaygrm]    |
| 3-8 NICs **production** stack                      | [README][nnicbyolrmpub]     | [README][nnicbigiqrmpub] | [README][nnicpaygrmpub] |
    

## Failover clusters

Deploy BIG-IP VEs that fail over to one another.

| **Description**                                    | **BYOL**                  | **BIG-IQ**                | **PAYG**                 |
|----------------------------------------------------|---------------------------|---------------------------|--------------------------|
| 2 NIC cluster, same AZ **existing** stack          | [README][2clbyolrm]       | [README][2clbigiqrm]      | [README][2clpaygrm]      | 
| 2 NIC cluster, same AZ **production** stack        | [README][2clbyolrmpub]    | [README][2clbigiqrmpub]   | [README][2clpaygrmpub]   | 
| 2 NIC cluster, different AZs **production** stack  | [README][2clbyolrmpubAZ]  | [README][2clbigiqrmpubAZ] | [README][2clpaygrmpubAZ] | 
|                                                    |                           |                           |                          |
| 3 NIC cluster, same AZ **existing** stack          | [README][3clbyolrm]       | [README][3clbigiqrm]      | [README][3clpaygrm]      | 
| 3 NIC cluster, same AZ **production** stack        | [README][3clbyolrmpub]    | [README][3clbigiqrmpub]   | [README][3clpaygrmpub]   | 
| 3 NIC cluster, different AZs **production** stack  | [README][3clbyolrmpubAZ]  | [README][3clbigiqrmpubAZ] | [README][3clpaygrmpubAZ] |


## Auto scaling

Deploy a BIG-IP VE that auto scales based on traffic thresholds.

| **Description**                                    | **BIG-IQ**                  | **PAYG**               |
|----------------------------------------------------|-----------------------------|------------------------|
| Auto scale LTM                                     | [README][ltmasbigiqrm]      | [README][ltmaspaygrm]  |
| Auto Scale WAF                                     | [README][wafasbigiqrm]      | [README][wafaspaygrm]  |

# F5 ARM templates for Microsoft Azure

etc, etc
