---
title: Overview
---

SFPowerscripts is an Azure Pipelines Extension that converts Azure Pipelines into a CI/CD platform for Salesforce. The extension features the following tasks

Please note this extension only works with the newer source format based repositories only.

## Authentication/Org Related Tasks

- Authenticate a DevHub using JWT
- Authenticate a Sandbox using JWT
- Authenticate an Org using Username/Password/Security Token
- Create/Delete a Scratch Org

## Build/ Deployment Related Tasks

- Deploy a source format based repo to an org (scratch org/sandbox/prod)
- Create an unlocked package
- Deploy an unlocked package to an org
- Trigger Apex Test
- Validate Apex Test Coverge of an org
- Validate a Unlocked package for metadata coverage
- Install all package dependencies of an unlocked package

## Generic Utilities

 
 - Install SFDX along with SFPowerkit Plugin
 - Increment Project Version Number similar to npm version patch, which can be utilized before an unlocked / source based packaging
 - Create a build artifact for unlocked/source based packaging, which can be utilized in Release Pipelines
 - Checkout a source based artifact from Git using PAT


## What is it?

- The extension is designed with tasks which are granular,  which means all the above tasks has to be orchestrated in a valid order required to reach the required objective.  This allows one to utilise other commands or extensions between the tasks and be highly effective rather than getting tied to a single task. This ensures maximum flexiblity while building the pipeline.

For eg: a Pull Request validation for an unlocked package  should feature the tasks in this order

![PR Pipeline](https://user-images.githubusercontent.com/15088656/64956434-e990ff80-d8cd-11e9-98fd-44847dc29c42.png)

 1. Install the SFDX CLI
 2. Validate the unlocked package for metadata coverage
 3. Authenticate DevHub
 4. Create a Scratch Org
 5. Install Package Dependencies in the target scratch org
 6. Deploy source to the target scratch org
 7. Delete the scratch org

- Most of the tasks are very thin wrappers aroud the equivalent sfdx cli commands or the open source sfpowerkit (SFDX CLI extension). Almost all parameters that are requred during a CI run is exposed. If you feel that is not enough for the task at hand, one can quickly fall back to command line parameterized just for the task

- Though the tasks can all be utilized fully in build pipeline. It is recommended to utilize the Release Pipeline to deploy the artifats to make the full use of Azure Pipelines Capability.

## Why do I have to use this? Can't I script it out?

Of course you can, here are some advantages

1. Save time from writing bash scripts in hooking all these tasks, such as ensuring you get the result values from the json output and parsing it to the next command
2. Eliminate waste, multiple hours are spend on creating these scripts across multiple projects
3. Open Source, so fork it and contribute it back

## What if there is an issue with the plugin?

Please create an issue, and I will try to rectify as soon as possible. Wile it being fixed, you can omit the particular task from the extension and resort to command line using simple scripts

