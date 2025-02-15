---

copyright:
 years: 2014, 2022
lastupdated: "2022-08-04"

keywords: kubernetes, versions, update, upgrade, BOM, bill of materials, versions, patch, 1.23

subcollection: containers

---

{{site.data.keyword.attribute-definition-list}}


# Kubernetes version 1.23 change log
{: #changelog_123}

View information about version changes for major, minor, and patch updates that are available for your {{site.data.keyword.containerlong}} clusters that run version 1.23. Changes include updates to Kubernetes and {{site.data.keyword.cloud_notm}} Provider components.
{: shortdesc}

## Overview
{: #changelog_overview_123}

Unless otherwise noted in the change logs, the {{site.data.keyword.containerlong_notm}} provider version enables Kubernetes APIs and features that are at beta. Kubernetes alpha features, which are subject to change, are disabled.

For more information about major, minor, and patch versions and preparation actions between minor versions, see [Kubernetes versions](/docs/containers?topic=containers-cs_versions).
{: tip}

Check the [Security Bulletins on {{site.data.keyword.cloud_notm}} Status](https://cloud.ibm.com/status?component=containers-kubernetes&selected=security) for security vulnerabilities that affect {{site.data.keyword.containerlong_notm}}. You can filter the results to view only Kubernetes Cluster security bulletins that are relevant to {{site.data.keyword.containerlong_notm}}. Change log entries that address other security vulnerabilities but don't also refer to an {{site.data.keyword.IBM_notm}} security bulletin are for vulnerabilities that are not known to affect {{site.data.keyword.containerlong_notm}} in normal usage. If you run privileged containers, run commands on the workers, or execute untrusted code, then you might be at risk.

Some change logs are for _worker node fix packs_, and apply only to worker nodes. You must [apply these patches](/docs/containers?topic=containers-kubernetes-service-cli#cs_worker_update) to ensure security compliance for your worker nodes. These worker node fix packs can be at a higher version than the master because some build fix packs are specific to worker nodes. Other change logs are for _master fix packs_, and apply only to the cluster master. Master fix packs might not be automatically applied. You can choose to [apply them manually](/docs/containers?topic=containers-kubernetes-service-cli#cs_cluster_update). For more information about patch types, see [Update types](/docs/containers?topic=containers-cs_versions#update_types).
{: note}

## Version 1.23 change log
{: #123_changelog}

Review the version 1.23 change log.
{: shortdesc}













### Change log for worker node fix pack 1.23.9_1540, released 01 August 2022
{: #1239_1540}

The following table shows the changes that are in the worker node fix pack 1.23.9_1540. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 18.04 packages |N/A|N/A| Worker node kernel & package updates for [CVE-2022-27404](https://nvd.nist.gov/vuln/detail/CVE-2022-27404){: external},[CVE-2022-27405](https://nvd.nist.gov/vuln/detail/CVE-2022-27405){: external},[CVE-2022-27406](https://nvd.nist.gov/vuln/detail/CVE-2022-27406){: external},[CVE-2022-29217](https://nvd.nist.gov/vuln/detail/CVE-2022-29217){: external},[CVE-2022-31782](https://nvd.nist.gov/vuln/detail/CVE-2022-31782){: external}. |
| Kubernetes | 1.23.8 | 1.23.9 | For more information, see the [change log](https://github.com/kubernetes/kubernetes/releases/tag/v1.23.9){: external}. |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.8_1537" caption-side="top"}

### Change log for master fix pack 1.23.9_1539, released 26 July 2022
{: #1239_1539}

The following table shows the changes that are in the master fix pack 1.23.9_1539. Master patch updates are applied automatically. 
{: shortdesc}


| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Calico | v3.21.5 | v3.23.3 | See the [Calico release notes](https://projectcalico.docs.tigera.io/releases){: external}. Updated the Calico custom resource definitions to include `preserveUnknownFields: false`. |
| Cluster health image | v1.3.8 | v1.3.9 | Updated `Go` dependencies and to use `Go` version `1.18.4`. Fixed minor typo in addon `daemonset not available` health status. |
| Gateway-enabled cluster controller | 1680 | 1792 | Updated to use `Go` version `1.17.11`. Updated image for [CVE-2022-2097](https://nvd.nist.gov/vuln/detail/CVE-2022-2097){: external} and [CVE-2022-29458](https://nvd.nist.gov/vuln/detail/CVE-2022-29458){: external}. |
| GPU device plug-in and installer | 2b0b6d1 | d8f1be0 | Updated `Go` dependencies and to use `Go` version `1.18.3`. |
| {{site.data.keyword.IBM_notm}} Calico extension | 980 | 997 | Updated to use `Go` version `1.17.11`. Updated universal base image (UBI) to version `8.6-854` to resolve CVEs. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.23.7-7 | v1.23.8-7 | Updated `Go` dependencies and to use `Go` version `1.17.11`. Updated to support the Kubernetes `1.23.8` release. |
| {{site.data.keyword.filestorage_full_notm}} plug-in and monitor | 410 | 412 | Updated to use `Go` version `1.18.3`. Updated universal base image (UBI) to version `8.6-854` to resolve CVEs. Improved Kubernetes resource watch configuration. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | 8c96932 | 0a187a4 | Updated universal base image (UBI) to resolve CVEs. |
| Key Management Service provider | v2.5.6 | v2.5.7 | Updated `Go` dependencies and to use `Go` version `1.18.4`. |
| Kubernetes | v1.23.8 | v1.23.9 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.23.9){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 1998 | 2058 | Updated image for [CVE-2022-2097](https://nvd.nist.gov/vuln/detail/CVE-2022-2097){: external}. |
| Portieris admission controller | v0.12.4 | v0.12.5 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.12.5){: external}. |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.8_1534" caption-side="top"}

### Change log for worker node fix pack 1.23.8_1537, released 18 July 2022
{: #1238_1537}

The following table shows the changes that are in the worker node fix pack 1.23.8_1537. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 18.04 packages | 4.15.0-188 | 4.15.0-189 | Worker node kernel & package updates for [CVE-2015-20107](https://nvd.nist.gov/vuln/detail/CVE-2015-20107){: external}, [CVE-2022-2097](https://nvd.nist.gov/vuln/detail/CVE-2022-2097){: external},[CVE-2022-22747](https://nvd.nist.gov/vuln/detail/CVE-2022-22747){: external}, [CVE-2022-24765](https://nvd.nist.gov/vuln/detail/CVE-2022-24765){: external}, [CVE-2022-29187](https://nvd.nist.gov/vuln/detail/CVE-2022-29187){: external},[CVE-2022-34480](https://nvd.nist.gov/vuln/detail/CVE-2022-34480){: external},[CVE-2022-34903](https://nvd.nist.gov/vuln/detail/CVE-2022-34903){: external}. |
| Kubernetes |N/A|N/A|N/A|
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.8_1535" caption-side="top"}

### Change log for worker node fix pack 1.23.8_1535, released 05 July 2022
{: #1238_1535}

The following table shows the changes that are in the worker node fix pack 1.23.8_1535. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 18.04 packages | 4.15.0-187 | 4.15.0-188 | Worker node kernel & package updates for [CVE-2022-1292](https://nvd.nist.gov/vuln/detail/CVE-2022-1292){: external},[CVE-2022-2068](https://nvd.nist.gov/vuln/detail/CVE-2022-2068){: external},[CVE-2022-2084](https://nvd.nist.gov/vuln/detail/CVE-2022-2084){: external},[CVE-2022-28388](https://nvd.nist.gov/vuln/detail/CVE-2022-28388){: external},[CVE-2022-32206](https://nvd.nist.gov/vuln/detail/CVE-2022-32206){: external},[CVE-2022-32208](https://nvd.nist.gov/vuln/detail/CVE-2022-32208){: external}. |
| Kubernetes |N/A|N/A|N/A|
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.8_1534" caption-side="top"}

### Change log for master fix pack 1.23.8_1534, released 22 June 2022
{: #master_1238_1534}

The following table shows the changes that are in the master fix pack 1.23.8_1534. Master patch updates are applied automatically. 
{: shortdesc}


| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.3.7 | v1.3.8 | Updated `Go` to version `1.17.11` and also updated the dependencies. |
| GPU device plug-in and installer | 382ada9 | 2b0b6d1 | Updated universal base image (UBI) to version `8.6-751`. Updated `Go` to version `1.17.10`. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.23.7-4 | v1.23.7-7 | Update module `github.com/{{site.data.keyword.IBM_notm}}/vpc-go-sdk` to `v0.20.0`. Update module `github.com/stretchr/testify` to `v1.7.2`. |
| Key Management Service provider | v2.5.5 | v2.5.6 | Updated `Go` to version `1.17.11` and also updated the dependencies. |
| Kubernetes | v1.23.7 | v1.23.8 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.23.8){: external}. |
| Kubernetes add-on resizer | 1.8.14 | 1.8.15 | See the [Kubernetes add-on resizer release notes](https://github.com/kubernetes/autoscaler/releases/tag/addon-resizer-1.18.15){: external}. |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.7_1531" caption-side="top"}

### Change log for worker node fix pack 1.23.8_1534, released 20 June 2022
{: #1238_1534}

The following table shows the changes that are in the worker node fix pack 1.23.8_1534. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 18.04 packages | 4.15.0-180 | 4.15.0-187 | Worker node kernel & package updates for [CVE-2021-46790](https://nvd.nist.gov/vuln/detail/CVE-2021-46790){: external}, [CVE-2022-1304](https://nvd.nist.gov/vuln/detail/CVE-2022-1304){: external}, [CVE-2022-1419](https://nvd.nist.gov/vuln/detail/CVE-2022-1419){: external}, [CVE-2022-1966](https://nvd.nist.gov/vuln/detail/CVE-2022-1966){: external}, [CVE-2022-21123](https://nvd.nist.gov/vuln/detail/CVE-2022-21123){: external}, [CVE-2022-21125](https://nvd.nist.gov/vuln/detail/CVE-2022-21125){: external}, [CVE-2022-21166](https://nvd.nist.gov/vuln/detail/CVE-2022-21166){: external}, [CVE-2022-21499](https://nvd.nist.gov/vuln/detail/CVE-2022-21499){: external}, [CVE-2022-28390](https://nvd.nist.gov/vuln/detail/CVE-2022-28390){: external}, [CVE-2022-30783](https://nvd.nist.gov/vuln/detail/CVE-2022-30783){: external}, [CVE-2022-30784](https://nvd.nist.gov/vuln/detail/CVE-2022-30784){: external}, [CVE-2022-30785](https://nvd.nist.gov/vuln/detail/CVE-2022-30785){: external}, [CVE-2022-30786](https://nvd.nist.gov/vuln/detail/CVE-2022-30786){: external}, [CVE-2022-30787](https://nvd.nist.gov/vuln/detail/CVE-2022-30787){: external}, [CVE-2022-30788](https://nvd.nist.gov/vuln/detail/CVE-2022-30788){: external}, [CVE-2022-30789](https://nvd.nist.gov/vuln/detail/CVE-2022-30789){: external}. |
| Haproxy | 468c09 | 04f862 | [CVE-2022-1271](https://nvd.nist.gov/vuln/detail/CVE-2022-1271){: external}. |
| containerd | v1.6.4 | v1.6.6 | See the [change log](https://github.com/containerd/containerd/releases/tag/v1.6.6){: external}, the [security bulletin](https://www.ibm.com/support/pages/node/6597989){: external} for [CVE-2022-31030](https://nvd.nist.gov/vuln/detail/CVE-2022-31030){: external}, and the [security bulletin](https://www.ibm.com/support/pages/node/6598049){: external} for [CVE-2022-29162](https://nvd.nist.gov/vuln/detail/CVE-2022-29162){: external}. |
| Kubernetes | 1.23.7 | 1.23.8 | For more information, see the [change log](https://github.com/kubernetes/kubernetes/releases/tag/v1.23.8){: external}. |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.7_1532" caption-side="top"}

### Change log for worker node fix pack 1.23.7_1532, released 7 June 2022
{: #1237_1532}

The following table shows the changes that are in the worker node fix pack 1.23.7_1532. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 18.04 packages | 4.15.0-177 | 4.15.0-180 | Worker node kernel & package updates for [CVE-2019-13050](https://nvd.nist.gov/vuln/detail/CVE-2019-13050){: external}, [CVE-2022-1664](https://nvd.nist.gov/vuln/detail/CVE-2022-1664){: external} , [CVE-2022-29581](https://nvd.nist.gov/vuln/detail/CVE-2022-29581){: external} |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.6_1530" caption-side="top"}

### Change log for master fix pack 1.23.7_1531, released 3 June 2022
{: #1237_1531}

The following table shows the changes that are in the master fix pack 1.23.7_1531. Master patch updates are applied automatically. 
{: shortdesc}


| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.3.6 | v1.3.7 | Updated Go to version 1.17.10 and also updated the dependencies. Update registry base image version to `104` |
| GPU device plug-in and installer | 9485e14 | 382ada9 | Updated `Go` to version `1.17.9` |
| {{site.data.keyword.IBM_notm}} Calico extension | 954 | 980 | Updated to use `Go` version `1.17.10`. Updated minimal UBI to version `8.5`. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.23.5-9 | v1.23.7-4 | Updated to support the Kubernetes `1.23.7` release and `Go` version `1.17.10` |
| {{site.data.keyword.filestorage_full_notm}} plug-in and monitor | 408 | 410 | Updated universal base image (UBI) to version `8.6-751` to resolve CVEs. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | 8c8c82b | 8c96932 | Updated `Go` to version `1.18.1` |
| Key Management Service provider | v2.5.4 | v2.5.5 | Updated `Go` to version `1.17.10` and updated the golang dependencies. |
| Kubernetes | v1.23.6 | v1.23.7 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.23.7){: external}. |
| Kubernetes Dashboard | v2.4.0 | v2.4.0 | The **default** Kubernetes Dashboard settings found in the `kubernetes-dashboard-settings` config map in the `kube-system` namespace have been updated to set `resourceAutoRefreshTimeInterval` to `60`. This default change is only applied to new clusters. The previous default value was `5`. If your cluster has Kubernetes Dashboard performance problems, see the steps for [changing the auto-refresh time interval](/docs/containers?topic=containers-ts-kube-dashboord-oom). |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 1916 | 1998 | Updated `Go` to version `1.17.10` and updated dependencies. |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.6_1527" caption-side="top"}

### Change log for worker node fix pack 1.23.6_1530, released 23 May 2022
{: #1236_1530}

The following table shows the changes that are in the worker node fix pack 1.23.6_1530. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 18.04 packages | 4.15.0-176 | 4.15.0-177 | Worker node kernel & package updates for [CVE-2019-20838](https://nvd.nist.gov/vuln/detail/CVE-2019-20838){: external}, [CVE-2020-14155](https://nvd.nist.gov/vuln/detail/CVE-2020-14155){: external}, [CVE-2020-25648](https://nvd.nist.gov/vuln/detail/CVE-2020-25648){: external}, [CVE-2020-35512](https://nvd.nist.gov/vuln/detail/CVE-2020-35512){: external}, [CVE-2021-26401](https://nvd.nist.gov/vuln/detail/CVE-2021-26401){: external}, [CVE-2022-0001](https://nvd.nist.gov/vuln/detail/CVE-2022-0001){: external}, [CVE-2022-0934](https://nvd.nist.gov/vuln/detail/CVE-2022-0934){: external}, [CVE-2022-26490](https://nvd.nist.gov/vuln/detail/CVE-2022-26490){: external}, [CVE-2022-27223](https://nvd.nist.gov/vuln/detail/CVE-2022-27223){: external}, [CVE-2022-27781](https://nvd.nist.gov/vuln/detail/CVE-2022-27781){: external}, [CVE-2022-27782](https://nvd.nist.gov/vuln/detail/CVE-2022-27782){: external}, [CVE-2022-28657](https://nvd.nist.gov/vuln/detail/CVE-2022-28657){: external}, [CVE-2022-29155](https://nvd.nist.gov/vuln/detail/CVE-2022-29155){: external}, [CVE-2022-29824](https://nvd.nist.gov/vuln/detail/CVE-2022-29824){: external}, [CVE-2017-9525](https://nvd.nist.gov/vuln/detail/CVE-2017-9525){: external}, [CVE-2022-28654](https://nvd.nist.gov/vuln/detail/CVE-2022-28654){: external}, [CVE-2022-28656](https://nvd.nist.gov/vuln/detail/CVE-2022-28656){: external}, [CVE-2022-28655](https://nvd.nist.gov/vuln/detail/CVE-2022-28655){: external}, [CVE-2022-28652](https://nvd.nist.gov/vuln/detail/CVE-2022-28652){: external}, [CVE-2022-1242](https://nvd.nist.gov/vuln/detail/CVE-2022-1242){: external}, [CVE-2022-28658](https://nvd.nist.gov/vuln/detail/CVE-2022-28658){: external}, [CVE-2021-3899](https://nvd.nist.gov/vuln/detail/CVE-2021-3899){: external}. |
| HA proxy | 36b0307 | 468c09 | [CVE-2021-3634](https://nvd.nist.gov/vuln/detail/CVE-2021-3634){: external}. |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.6_1529" caption-side="top"}

### Change log for worker node fix pack 1.23.6_1529, released 09 May 2022
{: #1236_1529}

The following table shows the changes that are in the worker node fix pack 1.23.6_1529. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 18.04 packages | N/A | N/A | Worker node package updates for [CVE-2021-36084](https://nvd.nist.gov/vuln/detail/CVE-2021-36084){: external}, [CVE-2021-36085](https://nvd.nist.gov/vuln/detail/CVE-2021-36085){: external}, [CVE-2021-36086](https://nvd.nist.gov/vuln/detail/CVE-2021-36086){: external}, [CVE-2021-36087](https://nvd.nist.gov/vuln/detail/CVE-2021-36087){: external}, [CVE-2022-1292](https://nvd.nist.gov/vuln/detail/CVE-2022-1292){: external}, [CVE-2022-22576](https://nvd.nist.gov/vuln/detail/CVE-2022-22576){: external}, [CVE-2022-27774](https://nvd.nist.gov/vuln/detail/CVE-2022-27774){: external}, [CVE-2022-27775](https://nvd.nist.gov/vuln/detail/CVE-2022-27775){: external}, [CVE-2022-27776](https://nvd.nist.gov/vuln/detail/CVE-2022-27776){: external}, [CVE-2022-29799](https://nvd.nist.gov/vuln/detail/CVE-2022-29799){: external}, [CVE-2022-29800](https://nvd.nist.gov/vuln/detail/CVE-2022-29800){: external}. |
| Kubernetes | N/A | N/A | N/A |
| Haproxy | f53b22 | 36b030 | [CVE-2022-1271](https://nvd.nist.gov/vuln/detail/CVE-2022-1271){: external}, [CVE-2022-1154](https://nvd.nist.gov/vuln/detail/CVE-2022-1154){: external}, [CVE-2018-25032](https://nvd.nist.gov/vuln/detail/CVE-2018-25032){: external}. |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.6_1528" caption-side="top"}

### Change log for master fix pack 1.23.6_1527, released 26 April 2022
{: #1236_1527}

The following table shows the changes that are in the master fix pack 1.23.6_1527. Master patch updates are applied automatically. 
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Calico | v3.21.4 | v3.21.5 | See the [Calico release notes](https://projectcalico.docs.tigera.io/archive/v3.21/release-notes/#v3215){: external}. |
| Cluster health image | v1.3.5 | v1.3.6 | Updated `Go` to version `1.17.9` and also updated the dependencies. Update `registry base image` version to `103`. |
| Gateway-enabled cluster controller | 1669 | 1680 | Updated metadata for a rotated key. |
| GPU device plug-in and installer| 13677d2 | 9485e14 | Updated Drivers to `470.103.01`. Updated metadata for a rotated key. |
| {{site.data.keyword.IBM_notm}} Calico extension | 950 | 954 | Updated to latest UBI-minimal image to resolve [CVE-2021-3999](https://nvd.nist.gov/vuln/detail/CVE-2021-3999){: external}, [CVE-2022-23218](https://nvd.nist.gov/vuln/detail/CVE-2022-23218){: external}, [CVE-2022-23219](https://nvd.nist.gov/vuln/detail/CVE-2022-23219){: external}, [CVE-2022-23308](https://nvd.nist.gov/vuln/detail/CVE-2022-23308){: external}, [CVE-2021-23177](https://nvd.nist.gov/vuln/detail/CVE-2021-23177){: external}, and [CVE-2021-31566](https://nvd.nist.gov/vuln/detail/CVE-2021-31566){: external}. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.23.5-3 | v1.23.5-9 | Updated `vpcctl` to the `3003` binary image. Update module `github.com/{{site.data.keyword.IBM_notm}}/vpc-go-sdk` to `v0.19.0` |
| {{site.data.keyword.cloud_notm}} RBAC Operator | 6c43ef1 | 8c8c82b | Updated `Go` to version `1.17.8` |
| {{site.data.keyword.filestorage_full_notm}} plug-in and monitor | 407 | 408 | Fixed [CVE-2022-0778](https://nvd.nist.gov/vuln/detail/CVE-2022-0778){: external}. |
| Key Management Service provider | v2.5.3 | v2.5.4 | Moved to a different base image, version `102`, to reduce CVE footprint. Resolved [CVE-2022-0778](https://nvd.nist.gov/vuln/detail/CVE-2022-0778){: external}. |
| Kubernetes API server | v1.23.5 | v1.23.6 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.23.6){: external}. |
| Load balancer and Load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 1899 | 1916 | Updated the image to resolve CVEs. |
| Portieris admission controller | v0.12.3 | v0.12.4 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.12.4){: external}. |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.5_1525" caption-side="top"}



### Change log for worker node fix pack 1.23.6_1528, released 25 April 2022
{: #1236_1528}




| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 18.04 packages | 4.15.0-175-generic | 4.15.0-176-generic | Kernel and package updates for [CVE-2018-16301](https://nvd.nist.gov/vuln/detail/CVE-2018-16301){: external}, [CVE-2019-18276](https://nvd.nist.gov/vuln/detail/CVE-2019-18276){: external}, [CVE-2020-8037](https://nvd.nist.gov/vuln/detail/CVE-2020-8037){: external}, [CVE-2021-31870](https://nvd.nist.gov/vuln/detail/CVE-2021-31870){: external}, [CVE-2021-31871](https://nvd.nist.gov/vuln/detail/CVE-2021-31871){: external}, [CVE-2021-31872](https://nvd.nist.gov/vuln/detail/CVE-2021-31872){: external}, [CVE-2021-31873](https://nvd.nist.gov/vuln/detail/CVE-2021-31873){: external}, [CVE-2021-43975](https://nvd.nist.gov/vuln/detail/CVE-2021-43975){: external}, [CVE-2022-1271](https://nvd.nist.gov/vuln/detail/CVE-2022-1271){: external}, [CVE-2022-24765](https://nvd.nist.gov/vuln/detail/CVE-2022-24765){: external}. |
| Kubernetes | v1.23.5 | v1.23.6 | For more information, see the [change log](https://github.com/kubernetes/kubernetes/releases/tag/v1.23.6){: external}. |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.5_1526" caption-side="top"}





### Change log for worker node fix pack 1.23.5_1526, released 11 April 2022
{: #1235_1526}

The following table shows the changes that are in the worker node fix pack 1.23.5_1526. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Containerd | v1.6.1 | v1.6.2 | See the [change log](https://github.com/containerd/containerd/releases/tag/v1.6.2){: external} and the [security bulletin](https://www.ibm.com/support/pages/node/6572257){: external}. |
| Ubuntu 18.04 packages | 4.15.0-173-generic | 4.15.0-175-generic | Kernel and package updates for   [CVE-2018-25032](https://nvd.nist.gov/vuln/detail/CVE-2018-25032) [CVE-2021-3426](https://nvd.nist.gov/vuln/detail/CVE-2021-3426) [CVE-2021-4189](https://nvd.nist.gov/vuln/detail/CVE-2021-4189) [CVE-2022-0391](https://nvd.nist.gov/vuln/detail/CVE-2022-0391) [CVE-2022-21712](https://nvd.nist.gov/vuln/detail/CVE-2022-21712) [CVE-2022-21716](https://nvd.nist.gov/vuln/detail/CVE-2022-21716) [CVE-2022-25308](https://nvd.nist.gov/vuln/detail/CVE-2022-25308) [CVE-2022-25309](https://nvd.nist.gov/vuln/detail/CVE-2022-25309) [CVE-2022-25310](https://nvd.nist.gov/vuln/detail/CVE-2022-25310) [CVE-2022-27666](https://nvd.nist.gov/vuln/detail/CVE-2022-27666). |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.5_1524" caption-side="top"}






### Change log for master fix pack 1.23.5_1525, released 6 April 2022
{: #1223_1525}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 1865 | 1899 | Revert setting gratuitous arp on LBv1. |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.5_1523" caption-side="top"}







### Change log for master fix pack 1.23.5_1523, released 30 March 2022
{: #1235_1523}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.3.3 | v1.3.5 | Updated image to fix CVEs [CVE-2021-3999](https://nvd.nist.gov/vuln/detail/CVE-2021-3999){: external}, [CVE-2022-23218](https://nvd.nist.gov/vuln/detail/CVE-2022-23218){: external}, [CVE-2022-23219](https://nvd.nist.gov/vuln/detail/CVE-2022-23219){: external}.  Updated golang dependencies. |
| Gateway-enabled cluster controller | 1653 | 1669 | Updated to use `Go` version `1.17.8`. |
| GPU device plug-in and installer | d7daae6 | 13677d2 | Updated GPU images to resolve CVEs. |
| IBM Calico extension | 929 | 950 | Updated to use `Go` version `1.17.8`. Updated universal base image (UBI) to resolve CVEs. |
| IBM Cloud Controller Manager | v1.23.4-4 | v1.23.5-3 | Updated to support the `Kubernetes 1.23.5` release and to use `Go` version `1.17.8`. |
| IBM Cloud {{site.data.keyword.filestorage_short}} plug-in and monitor | 405 | 407 | Updated `Go` to version `1.16.14`.  Updated `UBI` image to version `8.5-240`. |
| IBM Cloud RBAC Operator | 0fc9949 | 6c43ef1 | Upgraded `Go` packages to resolve vulnerabilities |
| Key Management Service provider | v2.5.2 | v2.5.3 | Updated to use `Go` version `1.17.8`. Updated golang dependencies.  Fixed CVE [CVE-2022-24407](https://nvd.nist.gov/vuln/detail/CVE-2022-24407){: external} |
| Konnectivity agent | v0.0.27_a6b5248a_323_iks | v0.0.30_331_iks | See the [Konnectivity release notes](https://github.com/kubernetes-sigs/apiserver-network-proxy/releases/tag/v0.0.30){: external}.  Updated to use `Go` version `1.17.8`. |
| Konnectivity server | v0.0.27_a6b5248a_323_iks | v0.0.30_331_iks | See the [Konnectivity release notes](https://github.com/kubernetes-sigs/apiserver-network-proxy/releases/tag/v0.0.30){: external}.  Updated to use `Go` version `1.17.8`. |
| Kubernetes | v1.23.4 | v1.23.5 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.23.5){: external}. |
| Load balancer and Load balancer monitor for IBM Cloud Provider | 1747 | 1865 | Updated the image to resolve CVEs. Updated to use `Go` version `1.17.8`. Set gratuitous arp at the right time on LBv1. |
| Portieris admission controller | v0.12.2 | v0.12.3 | See the [Portieris admission controller release notes](https://github.com/IBM/portieris/releases/tag/v0.12.3){: external} |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.4_1520" caption-side="top"}





### Change log for worker node fix pack 1.23.5_1524, released 28 March 2022
{: #1235_1524}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 18.04 packages | 4.15.0-171-generic | 4.15.0-173-generic | Kernel and package updates for [CVE-2021-20193](https://nvd.nist.gov/vuln/detail/CVE-2021-20193){: external}, [CVE-2021-25220](https://nvd.nist.gov/vuln/detail/CVE-2021-25220){: external}, [CVE-2021-3506](https://nvd.nist.gov/vuln/detail/CVE-2021-3506){: external}, [CVE-2022-0435](https://nvd.nist.gov/vuln/detail/CVE-2022-0435){: external}, [CVE-2022-0492](https://nvd.nist.gov/vuln/detail/CVE-2022-0492){: external}, [CVE-2022-0778](https://nvd.nist.gov/vuln/detail/CVE-2022-0778){: external}, [CVE-2022-0847](https://nvd.nist.gov/vuln/detail/CVE-2022-0847){: external}, [CVE-2022-23308](https://nvd.nist.gov/vuln/detail/CVE-2022-23308){: external}. |
| HA proxy | 15198f | b40c07 | [CVE-2021-45960](https://nvd.nist.gov/vuln/detail/CVE-2021-45960){: external}, [CVE-2021-46143](https://nvd.nist.gov/vuln/detail/CVE-2021-46143){: external}, [CVE-2022-22822](https://nvd.nist.gov/vuln/detail/CVE-2022-22822){: external}, [CVE-2022-22823](https://nvd.nist.gov/vuln/detail/CVE-2022-22823){: external}, [CVE-2022-22824](https://nvd.nist.gov/vuln/detail/CVE-2022-22824){: external}, [CVE-2022-22825](https://nvd.nist.gov/vuln/detail/CVE-2022-22825){: external}, [CVE-2022-22826](https://nvd.nist.gov/vuln/detail/CVE-2022-22826){: external}, [CVE-2022-22827](https://nvd.nist.gov/vuln/detail/CVE-2022-22827){: external}, [CVE-2022-23852](https://nvd.nist.gov/vuln/detail/CVE-2022-23852){: external}, [CVE-2022-25235](https://nvd.nist.gov/vuln/detail/CVE-2022-25235){: external}, [CVE-2022-25236](https://nvd.nist.gov/vuln/detail/CVE-2022-25236){: external}, [CVE-2022-25315](https://nvd.nist.gov/vuln/detail/CVE-2022-25315){: external}, [CVE-2021-3999](https://nvd.nist.gov/vuln/detail/CVE-2021-3999){: external}, [CVE-2022-23218](https://nvd.nist.gov/vuln/detail/CVE-2022-23218){: external}, [CVE-2022-23219](https://nvd.nist.gov/vuln/detail/CVE-2022-23219){: external}, [CVE-2022-23308](https://nvd.nist.gov/vuln/detail/CVE-2022-23308){: external}, [CVE-2021-23177](https://nvd.nist.gov/vuln/detail/CVE-2021-23177){: external}, [CVE-2021-31566](https://nvd.nist.gov/vuln/detail/CVE-2021-31566){: external}. |
| Kubernetes | 1.23.4 | 1.23.5 | See [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.23.5){: external}. |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.4_1522" caption-side="top"}





### Change log for worker node fix pack 1.23.4_1522, released 14 March 2022
{: #1234_1522}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Containerd | v1.6.0 | v1.6.1 | See the [change log](https://github.com/containerd/containerd/releases/tag/v1.6.1){: external} and the [security bulletin](https://www.ibm.com/support/pages/node/6564653){: external}. |
| Ubuntu 18.04 packages | 4.15.0-169-generic | 4.15.0-171-generic | Kernel and package updates for [CVE-2016-10228](https://nvd.nist.gov/vuln/detail/CVE-2016-10228){: external}, [CVE-2019-25013](https://nvd.nist.gov/vuln/detail/CVE-2019-25013){: external}, [CVE-2020-27618](https://nvd.nist.gov/vuln/detail/CVE-2020-27618){: external}, [CVE-2020-29562](https://nvd.nist.gov/vuln/detail/CVE-2020-29562){: external}, [CVE-2020-6096](https://nvd.nist.gov/vuln/detail/CVE-2020-6096){: external}, [CVE-2021-3326](https://nvd.nist.gov/vuln/detail/CVE-2021-3326){: external}, [CVE-2021-35942](https://nvd.nist.gov/vuln/detail/CVE-2021-35942){: external}, [CVE-2021-3999](https://nvd.nist.gov/vuln/detail/CVE-2021-3999){: external}, [CVE-2022-0001](https://nvd.nist.gov/vuln/detail/CVE-2022-0001){: external}, [CVE-2022-23218](https://nvd.nist.gov/vuln/detail/CVE-2022-23218){: external}, [CVE-2022-23219](https://nvd.nist.gov/vuln/detail/CVE-2022-23219){: external}, [CVE-2022-25313](https://nvd.nist.gov/vuln/detail/CVE-2022-25313){: external}, [CVE-2022-25314](https://nvd.nist.gov/vuln/detail/CVE-2022-25314){: external}, [CVE-2022-25315](https://nvd.nist.gov/vuln/detail/CVE-2022-25315){: external}. |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.4_1521" caption-side="top"}





### Change log for master fix pack 1.23.4_1520, released 3 March 2022
{: #1234_1520}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.3.0 | v1.3.3 | Updated `golang.org/x/crypto` to `v0.0.0-20220214200702-86341886e292`. Adds fix for [CVE-2021-43565](https://www.mend.io/vulnerability-database/CVE-2021-43565){: external}. Adds Golang dependency updates. |
| Gateway-enabled cluster controller | 1586 | 1653 | Updated to use `Go` version `1.17.7` and updated `Go` modules to fix CVEs. |
| GPU device plug-in and installer | 4a174aa | d7daae6 | Updated GPU images to resolve CVEs. |
| IBM Calico extension | 923 | 929 | Updated universal base image (UBI) to the `8.5-230` version to resolve CVEs. Updated to use `Go` version `1.16.13`. |
| IBM Cloud Controller Manager | v1.23.3-4 | v1.23.4-4 | Updated to support the Kubernetes `1.23.4` release and to use `Go` version `1.17.7`. |
| IBM Cloud {{site.data.keyword.filestorage_short}} plug-in and monitor | 404 | 405 | Adds fix for [CVE-2021-3538](https://www.mend.io/vulnerability-database/CVE-2021-3538){: external} and adds dependency updates. |
| Key Management Service provider | v2.4.0 | v2.5.2 | Updated `golang.org/x/crypto` to `v0.0.0-20220214200702-86341886e292`. Adds fix for [CVE-2021-43565](https://www.mend.io/vulnerability-database/CVE-2021-43565){: external}. Adds Golang dependency updates. |
| Konnectivity agent | v0.0.27_309_iks | v0.0.27_a6b5248a_323_iks | See the [Konnectivity release notes](https://github.com/kubernetes-sigs/apiserver-network-proxy/releases/tag/v0.0.27){: external}.  Updated universal base image (UBI) to the `8.5-230` version to resolve CVEs. Updated to use `Go` version `1.17.5`. |
| Konnectivity server | v0.0.27_309_iks | v0.0.27_a6b5248a_323_iks | See the [Konnectivity release notes](https://github.com/kubernetes-sigs/apiserver-network-proxy/releases/tag/v0.0.27){: external}. Updated universal base image (UBI) to the `8.5-230` version to resolve CVEs. Updated to use `Go` version `1.17.5`. |
| Kubernetes | v1.23.3 | v1.23.4 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.23.4){: external}. |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.3_1518" caption-side="top"}





### Change log for worker node fix pack 1.23.4_1521, released 28 February 2022
{: #1234_1521}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 18.04 packages | 4.15.0-167-generic | 4.15.0-169-generic | Kernel and package updates for [CVE-2021-4083](https://nvd.nist.gov/vuln/detail/CVE-2021-4083){: external}, [CVE-2021-4155](https://nvd.nist.gov/vuln/detail/CVE-2021-4155){: external}, [CVE-2021-45960](https://nvd.nist.gov/vuln/detail/CVE-2021-45960){: external}, [CVE-2021-46143](https://nvd.nist.gov/vuln/detail/CVE-2021-46143){: external}, [CVE-2022-0330](https://nvd.nist.gov/vuln/detail/CVE-2022-0330){: external}, [CVE-2022-22822](https://nvd.nist.gov/vuln/detail/CVE-2022-22822){: external}, [CVE-2022-22823](https://nvd.nist.gov/vuln/detail/CVE-2022-22823){: external}, [CVE-2022-22824](https://nvd.nist.gov/vuln/detail/CVE-2022-22824){: external}, [CVE-2022-22825](https://nvd.nist.gov/vuln/detail/CVE-2022-22825){: external}, [CVE-2022-22826](https://nvd.nist.gov/vuln/detail/CVE-2022-22826){: external}, [CVE-2022-22827](https://nvd.nist.gov/vuln/detail/CVE-2022-22827){: external}, [CVE-2022-22942](https://nvd.nist.gov/vuln/detail/CVE-2022-22942){: external}, [CVE-2022-23852](https://nvd.nist.gov/vuln/detail/CVE-2022-23852){: external}, [CVE-2022-23990](https://nvd.nist.gov/vuln/detail/CVE-2022-23990){: external}, [CVE-2022-24407](https://nvd.nist.gov/vuln/detail/CVE-2022-24407){: external}, [CVE-2022-25235](https://nvd.nist.gov/vuln/detail/CVE-2022-25235){: external}, [CVE-2022-25236](https://nvd.nist.gov/vuln/detail/CVE-2022-25236){: external}. |
| Kubernetes | v1.23.3 | v1.23.4 | For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.23.4){: external}. | 
| HA proxy | f6a2b3 | 15198fb | Contains fixes for [CVE-2022-24407](https://nvd.nist.gov/vuln/detail/CVE-2022-24407){: external}. | 
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.3_1519" caption-side="top"}






### Change log for worker node fix pack 1.23.3_1519, released 14 February 2022
{: #1233_1519}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Kubernetes | N/A | 1.23.3 | For more information, see the [change log](https://github.com/kubernetes/kubernetes/releases/tag/v1.23.3){: external}. |
| HA proxy | d38fa1 | f6a2b3 | [CVE-2021-3521](https://nvd.nist.gov/vuln/detail/CVE-2021-3521){: external}   [CVE-2021-4122](https://nvd.nist.gov/vuln/detail/CVE-2021-4122){: external}. |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.23.2_1517" caption-side="top"}





### Change log for master fix pack 1.23.3_1518 and worker node fix pack 1.23.2_1517, released 9 February 2022
{: #1233_1518_and_1232_1517}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Calico | v3.20.3 | v3.21.4 | For more information, see the [Calico release notes](https://projectcalico.docs.tigera.io/releases){: external}. |
| Cluster health image | v1.2.21 | v1.3.0 | Added new health check for cluster autoscaler add-on. |
| CoreDNS | 1.8.6 | 1.8.7 | See the [CoreDNS release notes](https://coredns.io/2021/12/09/coredns-1.8.7-release/){: external}. |
| GPU device plug-in and installer | eefc4ae | 4a174aa | Updated image for [CVE-2020-26160](https://nvd.nist.gov/vuln/detail/CVE-2020-26160){: external} and [CVE-2021-3538](https://nvd.nist.gov/vuln/detail/CVE-2021-3538){: external}. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.22.6-1 | v1.23.3-4 | Updated to support the Kubernetes `1.23.3` release and to use `Go` version `1.17.6`.  Classic load balancers have been updated to improve availability during updates. In addition, creating a mixed protocol load balancer is not supported. |
| Kubernetes (master) | v1.22.6 | v1.23.3 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.23.3){: external}. |
| Kubernetes (worker node) | v1.22.6 | v1.23.2 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.23.2){: external}. |
| Kubernetes configuration | N/A | N/A | Updated the [feature gate configuration](/docs/containers?topic=containers-service-settings#feature-gates){: external}. |
| Kubernetes CSI snapshotter CRDs | v4.0.0 | v4.2.1 | See the [Kubernetes container storage interface (CSI) snapshotter release notes](https://github.com/kubernetes-csi/external-snapshotter/releases/tag/v4.2.1){: external}. |
| Kubernetes Dashboard | v2.3.1 | v2.4.0 | See the [Kubernetes Dashboard release notes](https://github.com/kubernetes/dashboard/releases/tag/v2.4.0){: external}. |
| Kubernetes Metrics Server | v0.5.2 | v0.6.0 | See the [Kubernetes Metrics Server release notes](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.6.0){: external}. |
| Kubernetes NodeLocal DNS cache | 1.21.3 | 1.21.4 | See the [Kubernetes NodeLocal DNS cache release notes](https://github.com/kubernetes/dns/releases/tag/1.21.4){: external}. |
| Operator Lifecycle Manager | 0.16.1-IKS-15 | None | Operator Lifecycle Manager is no longer installed nor managed by IBM. Existing installs are left as-is and no longer managed after an upgrade. |
| Operator Lifecycle Manager Catalog | v1.15.3 | None | Operator Lifecycle Manager is no longer installed nor managed by IBM. Existing installs are left as-is and no longer managed after an upgrade. |
| Pause container image | 3.5 | 3.6 | See the [pause container image release notes](https://github.com/kubernetes/kubernetes/blob/master/build/pause/CHANGELOG.md){: external}. |
{: summary="The rows are read from left to right. The first column is the changed component. The second column is the previous version number of the component. The third column is the current version number of the component. The fourth column contains a brief description of the change made to the component."}
{: caption="Changes since version 1.22.6_1537 (master) and 1.22.6_1538 (worker node)" caption-side="top"}
