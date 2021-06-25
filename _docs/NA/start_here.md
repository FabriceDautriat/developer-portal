---
title: Developing a nano app
subtitle: Find the necessary instructions to develop an app for Ledger devices

tags: []
toc: true
toc_sticky: true
author:
layout: doc_na
---

#### Sections in this article
{:.no_toc}
* TOC
{:toc}


## Get in touch with the Ledger developer community

If you’re already signed up to the Ledger Devs Slack workspace, introduce yourself to the developer community in the **#introductions** channel and get help in the **#support** and **ledgerjs** channels. Otherwise, send us a request by filling [this contact form](../../../contact).

## Start coding

Nano applications are developed in C on the Blockchain Open Ledger Operating System (BOLOS).

To develop a Nano Application you will need to:
- Use Linux or a VM with Linux installed
- Set up the BOLOS environment (consisting of the Nano S or X SDK, and two compilers)
- Use the [Python Loader](../../PL/01_readme/) to communicate with the device

<!--  -->
{% include alert.html style="primary" text="If you need to emulate a device, you can use <a href='https://developers.ledger.com/docs/SP/index/'>Speculos</a>, an emulator developed by Ledger." %}
<!--  -->

#### Familiarize yourself with the BOLOS platform

BOLOS is the operating system behind all Ledger personal security devices. It provides a lightweight, open-source framework for developers to build source code portable applications that run in a secure environment.

[Learn about the BOLOS platform](../b_overview)

#### Set up the BOLOS development environment
In order to build or compile BOLOS applications for Ledger devices, the appropriate environment must be set up. This environment consists in an SDK and two compilers. [Quickstart](../u_quickstart) with our script and/or go into [more details](../u_deepdive) about the script.

## Contribute
If you want to improve the documentation you can [use the contribution form](https://developers.ledger.com/contribution/) or make suggestions on the [Ledger's Developer Slack](https://ledger-dev.slack.com)

## Submit your app for the Ledger Live manager
Make sure that your app is ready before submitting it for review and that you have followed instructions from our documentation.

#### Design guidelines
The design of your device app will be added to our website to inform that your app is available. You must provide two icons that are compliant with the criteria established by our team.
See the [design guidelines here](../a_publishing_an_app/#design-guidelines).

#### Internal process
When an app is submitted it will go through 3 main steps which are the functional review, the security review and the documentation review.

Click the links to see [security requirements](../a_security_guidelines), [documentation requirements](../a_documentation_requirements), and [functional requirements](../u_display_management).

#### Submission
Once your app is ready and you have made sure it follows our guidelines, you can submit it by completing a form. Make sure you thoroughly complete it as it will impact the speed of the release process.

Go to the submission form [here](https://docs.google.com/forms/d/1Akhm7wWVISRxH4s9yScGdnuSsfRxSxg27yuIp4ufCts/viewform?edit_requested=true).


