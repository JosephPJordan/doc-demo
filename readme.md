# F5 AWS CloudFormation templates
[![Slack Status](https://f5cloudsolutions.herokuapp.com/badge.svg)](https://f5cloudsolutions.herokuapp.com)
[![Releases](https://img.shields.io/github/release/f5networks/f5-aws-cloudformation.svg)](https://github.com/f5networks/f5-aws-cloudformation/releases)
[![Issues](https://img.shields.io/github/issues/f5networks/f5-aws-cloudformation.svg)](https://github.com/f5networks/f5-aws-cloudformation/issues)

## Introduction

Welcome to the GitHub repository for F5's CloudFormation templates for deploying F5 in Amazon Web Services.  All of the templates in this repository have been developed by F5 Networks engineers.

For information on getting started using F5's CFT templates on GitHub, see [Amazon Web Services: Solutions 101](http://clouddocs.f5.com/cloud/public/v1/aws/AWS_solutions101.html) and the README files in each directory.  


<details><summary><strong>Click to expand Support information</strong></summary>
<p>
Across all branches in this repository, there are two directories: *supported* and *experimental*.

  - **supported**<br>
  The *supported* directory contains CloudFormation templates that have been created and fully tested by F5 Networks. These templates are fully supported by F5, meaning you can get assistance if necessary from F5 Technical Support via your typical methods.

  - **experimental**<br>
  The *experimental* directory also contains CloudFormation templates that have been created by F5 Networks. However, these templates have not completed full testing and are subject to change. F5 Networks does not offer technical support for templates in the experimental directory, so use these templates with caution.

  </p></details>

<details><summary><strong>Click to expand Template information</strong></summary>
<p>
  
## Template information
Descriptions for each template are contained at the top of each template in the *Description* key.
For additional information, including how the templates are generated, and assistance in deploying a template, see the README file on the individual template pages.

### Matrix for tagged releases
F5 has created a matrix that contains all of the tagged releases of the F5 Cloud Formation Templates (CFTs) for Amazon AWS, and the corresponding BIG-IP versions, license types, and throughput levels available for a specific tagged release. See https://github.com/F5Networks/f5-aws-cloudformation/blob/master/aws-bigip-version-matrix.md.
</p></details>



## Table of Supported F5 CloudFormation templates for AWS deployments
The following tables contain links to the current *supported* F5 CloudFormation templates. Click the links to view the README files which include the Launch buttons and additional information. 


| **Description**                                    | **BYOL**                    | **BIG-IQ**               | **PAYG**                |
|----------------------------------------------------|-----------------------------|--------------------------|-------------------------|                                                             
| **Number of NICs** : Deploy a BIG-IP VE with the number of NICs you choose.                                   |
| 1 NIC    *existing* stack                        | [README][1nicbyolrm]        | [README][1nicbigiqrm]    | [README][1nicpaygrm]    |
| 1 NIC    *production* stack                      | [README][1nicbyolrmpub]     | [README][1nicbigiqrmpub] | [README][1nicpaygrmpub] |
|                                                    |                             |                          |                         |
| 2 NICs   *existing* stack                        | [README][2nicbyolrm]        | [README][2nicbigiqrm]    | [README][2nicpaygrm]    |
| 2 NICs   *production* stack                      | [README][2nicbyolrmpub]     | [README][2nicbigiqrmpub] | [README][2nicpaygrmpub] |
|                                                    |                             |                          |                         |
| 3 NICs   *existing* stack                        | [README][3nicbyolrm]        | [README][3nicbigiqrm]    | [README][3nicpaygrm]    |
| 3 NICs   *production* stack                      | [README][3nicbyolrmpub]     | [README][3nicbigiqrmpub] | [README][3nicpaygrmpub] |
|                                                    |                             |                          |                         | 
| 3-8 NICs *existing* stack                        | [README][nnicbyolrm]        | [README][nnicbigiqrm]    | [README][nnicpaygrm]    |
| 3-8 NICs *production* stack                      | [README][nnicbyolrmpub]     | [README][nnicbigiqrmpub] | [README][nnicpaygrmpub] |
| | |
| **Failover clusters** : Deploy BIG-IP VEs that fail over to one another.|
| 2 NIC cluster, same AZ *existing* stack          | [README][2clbyolrm]       | [README][2clbigiqrm]      | [README][2clpaygrm]      | 
| 2 NIC cluster, same AZ *production* stack        | [README][2clbyolrmpub]    | [README][2clbigiqrmpub]   | [README][2clpaygrmpub]   | 
| 2 NIC cluster, different AZs *production* stack  | [README][2clbyolrmpubAZ]  | [README][2clbigiqrmpubAZ] | [README][2clpaygrmpubAZ] | 
|                                                    |                           |                           |                          |
| 3 NIC cluster, same AZ *existing* stack          | [README][3clbyolrm]       | [README][3clbigiqrm]      | [README][3clpaygrm]      | 
| 3 NIC cluster, same AZ *production* stack        | [README][3clbyolrmpub]    | [README][3clbigiqrmpub]   | [README][3clpaygrmpub]   | 
| 3 NIC cluster, different AZs *production* stack  | [README][3clbyolrmpubAZ]  | [README][3clbigiqrmpubAZ] | [README][3clpaygrmpubAZ] |
| | |
| **Auto scaling**: Deploy a BIG-IP VE that auto scales based on traffic thresholds.
| Auto scale LTM (frontend via ELB)                  | | [README][ltmasbigiqrm]      | [README][ltmaspaygrm]  |
| Auto scale LTM (frontend via DNS)                  | | [README][ltmasbigiqdns]     | [README][ltmaspaygrm]  |
| Auto Scale WAF (frontend via ELB)                  | | [README][wafasbigiqrm]      | [README][wafaspaygrm]  |
| Auto Scale WAF (frontend via DNS)                  | | [README][wafasbigiqdns]     | [README][wafaspaygrm]  |






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

<!--- N-nics NO public IP - aka PRODUCTION -->

[nnicbyolrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/n-nic/production-stack/byol

    
[nnicbigiqrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/n-nic/production-stack/bigiq


[nnicpaygrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/n-nic/production-stack/payg


<!--- N-nics WITH public IP - aka EXISTING  -->

[nnicbyolrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/n-nic/existing-stack/byol

    
[nnicbigiqrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/n-nic/existing-stack/bigiq


[nnicpaygrmpub]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/standalone/n-nic/existing-stack/payg

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





<!--- Auto scaling LTM - via LB-->


[ltmaspaygrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/autoscale/ltm/via-lb/1nic/existing-stack/payg

[ltmasbigiqrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/autoscale/ltm/via-lb/1nic/existing-stack/bigiq

<!--- Auto scaling LTM - via DNS-->


[ltmaspaygdns]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/autoscale/ltm/via-dns/1nic/existing-stack/payg

[ltmasbigiqdns]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/autoscale/ltm/via-dns/1nic/existing-stack/bigiq


<!--- Auto scaling WAF -->

[wafaspaygrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/autoscale/waf/via-lb/1nic/existing-stack/payg

[wafasbigiqrm]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/autoscale/ltm/via-lb/1nic/existing-stack/bigiq

<!--- Auto scaling WAF -->

[wafaspaygdns]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/autoscale/waf/via-dns/1nic/existing-stack/payg

[wafasbigiqdns]: https://github.com/F5Networks/f5-aws-cloudformation/tree/master/supported/autoscale/ltm/via-dns/1nic/existing-stack/bigiq


---


### Copyright

Copyright 2014-2018 F5 Networks Inc.


### License


## Apache V2.0

Licensed under the Apache License, Version 2.0 (the "License"); you may not use
this file except in compliance with the License. You may obtain a copy of the
License at:

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and limitations
under the License.


## Contributor License Agreement

Individuals or business entities who contribute to this project must have
completed and submitted the F5 Contributor License Agreement
