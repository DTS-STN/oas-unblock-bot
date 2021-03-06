# oas-unblock-bot

## Summary

Bot Framework v4 application.

This bot has been created using [Bot Framework](https://dev.botframework.com). The project is building a chatbot to help OAS user to understand and know their pension information.

**Front-End app**: The [Virtual Assistant Web App code repo is located here](https://github.com/DTS-STN/Oas-Unblock-Web-App).
**Demo**: [OAS Unblock bot is online here](https://oas-unblock-web-app-main.bdm-dev.dts-stn.com/).

## Build Status

<a href="https://teamcity.dts-stn.com/viewType.html?buildTypeId=OasUnlockBot_DeployBdmDev&guest=1" >
<img src="https://teamcity.dts-stn.com/app/rest/builds/buildType:(id:5076)/statusIcon"/>
</a>

## Table of Contents

- [oas-unblock-Bot](#oas-unblock-bot)
  - [Summary](#summary)
  - [Build Status](#build-status)
  - [Table of Contents](#table-of-contents)
  - [Installation](#installation)
  - [Onboarding](#developer-onboarding)
  - [Pipeline Integration](#pipeline-integration)
  - [Config Changelog](#config-changelog)

## Installation

- Clone this bot's code repository to your local machine

```bash
git clone https://github.com/DTS-STN/oas-unblock-bot
```

or

```bash
git clone git@github.com:DTS-STN/oas-unblock-bot.git
```

## Developer Onboarding

See the Virtual Assistant Bot Framework [Onboarding wiki](https://github.com/DTS-STN/Virtual-Assistant-Bot-Framework/wiki/5.-Developer-Onboarding) for details on:

- [Getting started](https://github.com/DTS-STN/Virtual-Assistant-Bot-Framework/wiki/5.-Developer-Onboarding#getting-started)
- [Training LUIS](https://github.com/DTS-STN/Virtual-Assistant-Bot-Framework/wiki/6.-LUIS)
- [Adaptive Cards](https://github.com/DTS-STN/Virtual-Assistant-Bot-Framework/wiki/7.-Adaptive-Cards)
- [Testing](https://github.com/DTS-STN/Virtual-Assistant-Bot-Framework/wiki/5.-Developer-Onboarding#testing)
- [Pipeline integration](https://github.com/DTS-STN/Virtual-Assistant-Bot-Framework/wiki/8.-DevOps-&-Publishing)
- [Virtual Assistant Web Apps](https://github.com/DTS-STN/Virtual-Assistant-Bot-Framework/wiki/8.-Virtual-Assistant-Web-App)

## Pipeline Integration

### TeamCity

This application leverages GitHub actions and [TeamCity Pipelines](https://teamcity.dts-stn.com/ 'TeamCity Login') for performing pre-merge regression testing. On PR creation or update, the Pipelines will run the entire API test collection, as well as the integration tests. The GitHub action will run testing and build docker container for application.

#### Terraform

[Terraform](https://www.terraform.io/intro/index.html 'Terraform intro') is an infrastructure as code (IaC) tool that allows you to build, change, and version infrastructure safely and efficiently.

OAS Unblock bot [Terraform is configured here](https://teamcity.dts-stn.com/buildConfiguration/OasUnlockBot_Terraform_TerraformOasUnblockBot?#all-projects 'Unblock Bot Terraform profile').

## Config Changelog

- 2021/10/05: les.lakewood@hrsdc-rhdcc.gc.ca - Initial Draft based on ei-callback-bot
- 2021/10/09: les.lakewood@hrsdc-rhdcc.gc.ca - Confirm Home Address unblock flow added
- 2021/10/10: les.lakewood@hrsdc-rhdcc.gc.ca - Confirm Home Address unblock flow archived
- 2021/10/12: les.lakewood@hrsdc-rhdcc.gc.ca - Unblock Direct Deposit flow added
- 2021/10/17: les.lakewood@hrsdc-rhdcc.gc.ca - Adding adaptive cards
- 2021/10/17: les.lakewood@hrsdc-rhdcc.gc.ca - Created new LUIS apps for unblock bot
- 2021/12/21: les.lakewood@hrsdc-rhdcc.gc.ca - Consolidated LUIS apps across bots
