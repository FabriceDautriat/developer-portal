---
title: Introduction
subtitle: A bird's eye view
tags: []
toc: true
toc_sticky: true
author:
layout: doc_na
---


These pages contain detailed documentation about the core features offered by BOLOS, and how they can be utilized by BOLOS applications and end-users. We'll discuss how BOLOS manages the master device seed and the device private key, and how it can be used for attestation purposes. We'll also describe the hardware architecture that is common between all BOLOS devices.

The operating system behind all Ledger personal security devices is called the Blockchain Open Ledger Operating System, or BOLOS for short. BOLOS provides a lightweight, open-source framework for developers to build source code portable applications that run in a secure environment. BOLOS is a way of turning hardware wallets into fully-fledged [personal security devices](../psd-introduction).

BOLOS allows users to review and install applications that let them do more with their cryptographic secrets, while protecting the device and other applications from malicious code. The key to BOLOS's open-source friendliness and ability to limit the exposure of user's cryptographic secrets to their apps is its [application isolation](../psd-application-isolation) technology.

BOLOS is organized into the following modules:

-   An input / output module which allows applications executing in a secure environment to communicate with the outside world and third party peripherals
-   A cryptography module that implements low level cryptographic primitives and provides access to hardware acceleration where available
-   A persistent storage module that lets applications store data securely on the device
-   A personalization module for interfacing with the device master seed
-   An endorsement & application attestation module allowing BOLOS applications to provide proof of execution
-   A user interface module for rendering the GUI and handling user input (eg. via buttons on the device)

### The Dashboard

All BOLOS devices have a special app installed that runs on the OS with certain special privileges called the Dashboard application or the PSD Content Manager. The dashboard app contains the main GUI that the user sees when they aren't in any other app. This is what the users use to enter their master seed, and its what they use to launch other applications. The dashboard application is also what the host computer communicates with when loading or deleting apps off of the device.

An important component of the dashboard is the [BOLOS UX](../low-level-display-management#bolos-ux), which is the implementation of the device-wide user interface that all applications need to interface with for certain device-wide UI features (like screen locking). The UI of the default dashboard app that is built into the firmware for the Nano S is also available as an external application that can be loaded onto the device [on GitHub](https://github.com/LedgerHQ/nanos-ui).

