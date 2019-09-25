---
title: Continous Integration  ( Org  based)  Pipeline
category: Pipelines
order: 3
---

This pipeline demonstrates how you can build a&nbsp;continous integration pipeline for if you are using&nbsp; an [org model of development](https://trailhead.salesforce.com/en/content/learn/modules/org-development-model)&nbsp; . Here is a&nbsp;snapshot of the steps we have used to configure a&nbsp;pipeline. The pipeline mimics creating a version number as in [Continous Integration (Unlocked Packaging) pipeline](/Pipelines/Continous%20Integration%20Unlocked%20Package%20Pipeline/) to simulate version based deployment in the release pipelines and create meaninguful dashboards

This pipeline is triggered on every successfull completion of a&nbsp;feature branch into the develop/master branch. If the frequency is quite high, you can look into utilizing \\\[ci skip\\\] in front of the commit message to skip a&nbsp;trigger of this pipeline

**Pipeline Snapshot**

**![](/images/Org Development CI Pipeline.png){: width="506" height="259"}**

&nbsp;

You can import and modify this pipeline using the file provide in the [link](https://github.com/azlamsalam/sfpowerscripts/blob/master/SamplePipelines/Source%20Package%20Build%20using%20sfpowerscripts.json)

**Tasks Involved**

The steps that are part of this pipeline are (in the exact order)

1. [Install SFDX CLI](/Tasks/Common-Utility-Tasks/Install%20SFDX%20CLI/)
2. [Validate Unlocked Package](/Tasks/Common-Utility-Tasks/Validate%20Unlocked%20Package/) ( Only necessary if you are building an unlocked package)
3. [Authenticate an Org](/Tasks/Common-Utility-Tasks/Authenticate%20an%20Org/)( In this case, it is authenticating against DevHub)
4. [Create/Delete a scratch org](/Tasks/Common-Utility-Tasks/Create%20and%20Delete%20a%20Scratch%20Org/)( Action :Create)
5. [Deploy source to scratch org](/Tasks/Deployment-Tasks/Deploy%20Source%20to%20Org/) ( Deploy)
6. [Trigger Apex Tests in the scratch org](/Tasks/Testing%20Tasks/Trigger%20Apex%20Test/)
7. [Validate the apex test coverage in the org](/Tasks/Testing%20Tasks/Validate%20Apex%20Test/)
8. [Create/Delete a scratch org](/Tasks/Common-Utility-Tasks/Create%20and%20Delete%20a%20Scratch%20Org/)(Action :Delete)