---
title: Continous Integration Pipeline - Unlocked Package
category: Pipelines
order: 2
---

This pipeline demonstrates how you can build a continous integration pipeline for an unlocked package. Here is a snapshot of the steps we have used to configure a pipeline.

This pipeline is triggered on every successfull completion of a feature branch into the develop/master branch. If the frequency is quite high, you can look into utilizing \[ci skip\] in front of the commit message to skip a trigger of this pipeline

**Pipeline Snapshot**

**![](/images/Unlocked Package CI Pipeline.png){: width="510" height="320"}**

&nbsp;

You can import and modify this pipeline using the file provide in the [link](https://raw.githubusercontent.com/azlamsalam/sfpowerscripts/master/SamplePipelines/Unlocked%20Package%20Build%20using%20sfpowerscript.json)

**Tasks Involved**

The steps that are part of this pipeline are (in the exact order)

1. [Install SFDX CLI](/Tasks/Common-Utility-Tasks/Install%20SFDX%20CLI/)
2. [Authenticate an Org](/Tasks/Common-Utility-Tasks/Authenticate%20an%20Org/)( In this case, it is authenticating against DevHub)
3. [Increment the version number](/Tasks/Packaging-Tasks/Increment%20Version%20number%20of%20a%20package/) ( optional step, if you want to increment the build number or any segment number)
4. [Create a new version of the unlocked package](/Tasks/Packaging-Tasks/Create%20Source%20based%20Packaging/)