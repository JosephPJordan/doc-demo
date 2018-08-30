# F5 CloudFormation Templates for Amazon Web Services (AWS) 
The following list contains links to the README file documentation for each of the F5 Supported CloudFormation templates.

### NICs

Deploy a BIG-IP VE with the number of NICs you choose.

| **Description**                                    | **BYOL**                    | **BIG-IQ**               | **PAYG**                |
|----------------------------------------------------|-----------------------------|--------------------------|-------------------------|                                                                
| 1 NIC    **existing** stack                        | [README][1nicbyolrm]     | [README][1nicbigiqrm]    | [README][1nicpaygrm]  |
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
    

### Failover clusters

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


### Auto scaling

Deploy a BIG-IP VE that auto scales based on traffic thresholds.

| **Description**                                    | **BIG-IQ**                  | **PAYG**               |
|----------------------------------------------------|-----------------------------|------------------------|
| Auto scale LTM                                     | [README][ltmasbigiqrm]      | [README][ltmaspaygrm]  |
| Auto Scale WAF                                     | [README][wafasbigiqrm]      | [README][wafaspaygrm]  |

# F5 ARM templates for Microsoft Azure

etc, etc

<!--- N-nics NO public IP - aka PRODUCTION -->

[nnicbyolrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/n-nic/production-stack/byol

    
[nnicbigiqrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/n-nic/production-stack/bigiq


[nnicpaygrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/n-nic/production-stack/payg


<!--- N-nics WITH public IP - aka EXISTING  -->

[nnicbyolrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/n-nic/existing-stack/byol

    
[nnicbigiqrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/n-nic/existing-stack/bigiq


[nnicpaygrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/n-nic/existing-stack/payg



<!--- 1 nic NO public IP - aka PRODUCTION -->

[1nicbyolrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/1nic/production-stack/byol
    
[1nicbigiqrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/1nic/production-stack/bigiq

[1nicpaygrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/1nic/production-stack/payg


<!--- 1 nic WITH public IP - aka EXISTING -->

[1nicbyolrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/1nic/existing-stack/byol
    
[1nicbigiqrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/1nic/existing-stack/bigiq

[1nicpaygrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/1nic/existing-stack/payg



<!--- 2 nics NO public IP - aka PRODUCTION -->

[2nicbyolrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/2nic/production-stack/byol
    
[2nicbigiqrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/2nic/production-stack/bigiq

[2nicpaygrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/2nic/production-stack/payg


<!--- 2 nics WITH public IP - aka EXISTING  -->


[2nicbyolrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/2nic/existing-stack/byol
    
[2nicbigiqrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/2nic/existing-stack/bigiq

[2nicpaygrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/2nic/existing-stack/payg



<!--- 3 nics NO public IP - aka PRODUCTION -->

[3nicbyolrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/3nic/production-stack/byol
    
[3nicbigiqrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/3nic/production-stack/bigiq

[3nicpaygrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/3nic/production-stack/payg


<!--- 3 nics WITH public IP - aka EXISTING -->


[3nicbyolrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/3nic/existing-stack/byol
    
[3nicbigiqrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/3nic/existing-stack/bigiq

[3nicpaygrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/3nic/existing-stack/payg



<!--- clustered 2 nic same AZ NO public IP - aka PRODUCTION -->

[2clbyolrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/same-net/via-api/2nic/production-stack/byol
    
[2clbigiqrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/same-net/via-api/2nic/production-stack/bigiq

[2clpaygrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/same-net/via-api/2nic/production-stack/payg


<!--- clustered 2 nic same AZ WITH public IP - aka EXISTING -->


[2clbyolrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/same-net/via-api/2nic/existing-stack/byol
    
[2clbigiqrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/same-net/via-api/2nic/existing-stack/bigiq

[2clpaygrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/same-net/via-api/2nic/existing-stack/payg


<!--- clustered 2 nic DIFT AZ WITH public IP - aka EXISTING -->

<!--- JOE  there is something wrong with the links in this section. can you check it out?  mostly i think it's the name of the big-iq template  --->

[2clbyolrmpubAZ]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/across-net/via-api/2nic/existing-stack/byol
    
[2clbigiqrmpubAZ]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/across-net/via-api/2nic/existing-stack/bigiq

[2clpaygrmpubAZ]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/across-net/via-api/2nic/existing-stack/payg




<!--- clustered 3 nic same AZ NO public IP - aka PRODUCTION -->

[3clbyolrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/same-net/via-api/3nic/production-stack/byol
    
[3clbigiqrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/same-net/via-api/3nic/production-stack/bigiq

[3clpaygrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/same-net/via-api/3nic/production-stack/payg



<!--- clustered 3 nic same AZ WITH public IP - aka EXISTING -->


[3clbyolrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/same-net/via-api/3nic/existing-stack/byol
    
[3clbigiqrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/same-net/via-api/3nic/existing-stack/bigiq

[3clpaygrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/same-net/via-api/3nic/existing-stack/payg



<!--- clustered 2 nic DIFT AZ WITH public IP - aka EXISTING -->


[3clbyolrmpubAZ]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/across-net/via-api/3nic/existing-stack/byol
    
[3clbigiqrmpubAZ]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/across-net/via-api/3nic/existing-stack/bigiq

[3clpaygrmpubAZ]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/failover/across-net/via-api/3nic/existing-stack/payg





<!--- Auto scaling LTM -->


[ltmaspaygrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/autoscale/ltm/via-lb/1nic/existing-stack/payg

[ltmasbigiqrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/autoscale/ltm/via-lb/1nic/existing-stack/bigiq


<!--- Auto scaling WAF -->

[wafaspaygrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/autoscale/waf/via-lb/1nic/existing-stack/payg

[wafasbigiqrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/autoscale/ltm/via-lb/1nic/existing-stack/bigiq

