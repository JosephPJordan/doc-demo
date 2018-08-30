# F5 AWS CloudFormation templates

[![Slack Status](https://f5cloudsolutions.herokuapp.com/badge.svg)](https://f5cloudsolutions.herokuapp.com)
[![Releases](https://img.shields.io/github/release/f5networks/f5-aws-cloudformation.svg)](https://github.com/f5networks/f5-aws-cloudformation/releases)
[![Issues](https://img.shields.io/github/issues/f5networks/f5-aws-cloudformation.svg)](https://github.com/f5networks/f5-aws-cloudformation/issues)

 
Welcome to the GitHub repository for F5 CloudFormation templates (CFTs). Use these templates to deploy BIG-IP VE in Amazon Web Services. The templates in this repository were developed by engineers at F5.    

If you are new to GitHub and AWS CFTs from F5, you may want to check out [Amazon Web Services: Solutions 101](http://clouddocs.f5.com/cloud/public/v1/aws/AWS_solutions101.html).  

All branches in this repository have two directories: *supported* and *experimental*.

  - **supported**<br>
  The *supported* directory contains templates that were created and fully tested by F5 Networks. These templates are fully supported by F5, meaning you can get assistance if necessary from F5 Technical Support.

  - **experimental**<br>
  The *experimental* directory also contains CloudFormation templates that were created by F5 Networks. However, these templates have not completed full testing and are subject to change. F5 Networks does not offer technical support for templates in the experimental directory, so use these templates with caution.

## Release history matrix
To view a history of the tagged releases of the F5 CFTs for AWS and the corresponding BIG-IP versions, license types, and throughput levels available for each release, see https://github.com/F5Networks/f5-aws-cloudformation/blob/master/aws-bigip-version-matrix.md.

## CVE-2017-6168 information  
If you have launched an F5 CFT from a prior release, see the <a href="#important">important note</a> at the bottom of this page.

## Supported F5 CloudFormation templates for AWS
The following contains information on F5 supported CloudFormation templates.
  
### Stack types
There are two supported stack types for our AWS templates.

- *Existing Stack* <br> Existing stack templates require that the networking infrastructure is available prior to deploying. Existing stack templates launch with a public IP address.
- *Production Stack* <br> Production stack templates also require the networking infrastructure, however these templates deploy without creating or attaching any public IP addresses to the BIG-IP VEs. 

See the individual README files for more information on these stack types.

We also have **experimental** <a href="https://github.com/F5Networks/f5-aws-cloudformation/tree/master/experimental">Learning stack templates</a> which deploy full environments (including the BIG-IP) from scratch. 

### Licensing options

Each template has three possible licensing choices:
- *BYOL* - Bring Your Own License. Purchase a license from F5. 
- *PAYG* - Pay as You Go. License automatically and pay for the time your instances are running.
- *BIG-IQ license pool* - Use your existing BIG-IQ device with an existing pool of BYOL licenses to license your BIG-IP VEs.


**Important**: 
- Individual templates may have specific prerequisites; review the README file before attempting to launch a template. 
- Ensure you are in the correct AWS region before clicking the **Launch Stack** button.
 

The following CloudFormation templates are **supported** by F5. 
 
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

| **Description**                                    | **BIG-IQ**          | **PAYG**               |
|----------------------------------------------------|-----------------------------|------------------------|
| Auto scale LTM                                     | [README][ltmasbigiqrm]      | [README][ltmaspaygrm]  |
| Auto Scale WAF                                     | [README][wafasbigiqrm]      | [README][wafaspaygrm]  |
  





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

 
   
---
<a name="important"></a>
<table>
 <tr>
  <td align=center>:warning: <strong>IMPORTANT<strong> :warning:  </td>
 </tr>
 <tr>
  <td>If you used an F5 CFT template prior to <a href="https://github.com/F5Networks/f5-aws-cloudformation/releases/tag/v2.7.1">release 2.7.1</a>, BIG-IP virtual servers configured with a Client SSL profile may be vulnerable to an Adaptive Chosen Ciphertext attack (AKA Bleichenbacher attack, CVE-2017-6168). For complete information on this vulnerability, see https://support.f5.com/csp/article/K21905460. <br>F5 has released hotfixes for all vulnerable releases. <strong><em>All of the templates in the current release in this repository use non-vulnerable BIG-IP VE images</em></strong>.  If you are using a BIG-IP image launched from a previous version of a template, use the following guidance:<br>  
   <ul>
    <li><em>If you have an existing BIG-IP VE deployment in AWS</em>  <br>See the <a href="https://support.f5.com/csp/article/K21905460">Security Advisory</a>, which contains information about upgrading your BIG-IP VE to a non-vulnerable version.</li>
    <li><em>For <strong>new</strong> BIG-IP VE deployments in AWS</em><br> The F5 CFT templates in <a href="https://github.com/F5Networks/f5-aws-cloudformation/releases/tag/v2.7.1">release 2.7.1</a> and later use non-vulnerable images. We recommending using the templates in the <a href="https://github.com/F5Networks/f5-aws-cloudformation/releases">latest release</a> for new deployments.</li>
    <li><em>For <strong>new</strong> BIG-IP VE deployments using a template in an older tagged release on GitHub</em><br>  If you have a specific need for using an older F5 CFT template, see <a href="aws-update-bigip-image.md">Changing the BIG-IP VE image in an F5 CFT template</a> for instructions on updating the BIG-IP images referenced in the template.</li>
   </ul></td>
 </tr>
 </table>

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
