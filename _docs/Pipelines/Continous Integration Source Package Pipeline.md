---
title: Continous Integration Pipeline - Org Based
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

3. [Increment the version number](/Tasks/Packaging-Tasks/Increment%20Version%20number%20of%20a%20package/) ( optional step, if you want to increment the build number or any segment number)
4. [Create a new version of the source package](/Tasks/Packaging-Tasks/Create%20Source%20based%20Packaging/)