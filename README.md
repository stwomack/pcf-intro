# Introduction to PCF
Provides a half day of lecture and hands-on experience to familiarize attendees with cloud-native, microservices, Pivotal Cloud Foundry (PCF), and interacting with PCF through the command line interface (`cf`) and web UI (Apps Manager).


## Agenda (_roughly_)
1. Intro to Cloud Native (30 mins)
2. PCF Architecture (30 mins)
3. Hands On Workshop (1.5 hours)
4. Solace on PCF Demo (1 hour)
5. Platform Dojo Scoping (3 hours)

## Getting started

**Prerequisites**

Start by downloading and installing the appropriate prerequisite tools.
- [Cloud Foundry CLI](https://goo.gl/M0pH4i) to interact with a cloud foundry instance
- [Apache Maven](http://info.pivotal.io/HI002010A6ZlRJR1NeU00eC) to build labs using Maven
- [Gradle](https://services.gradle.org/distributions/gradle-3.1-all.zip) to build labs using Gradle
- [Git Client](https://git-scm.com/downloads) to clone Github repo or download and unzip
- An IDE, like [Spring Tool Suite](https://spring.io/tools/sts/all) or [IntelliJ IDEA](https://www.jetbrains.com/idea/download/)
- [Java SE Development Kit](http://info.pivotal.io/n0I60i3021AN0JU0le10CRR)

**Download materials**

Next, download the course materials.  This can be accomplished either through the GitHub website by downloading a repository zip and unzipping locally, or if you have Git installed, use the following commands:

```
$ git clone https://github.com/stwomack/pcf-intro
$ cd pcf-intro/
```

**PCF Environments**

In order to perform the labs, you must be connected or logged into a live PCF environment. Initially you were asked to create a Pivotal Web Services (PWS) account for use in labs and afterwards. One other environment hazs also been made available for use. Please see the [Pivotal Cloud Foundry Environment document](Common/env_info.md) for details. You should have been assigned a student number and PCF instance at registration. Otherwise the instructors will provide that information for your use.

## Course Materials

#### _Session 1: Cloud Native Architectures & Frameworks_ [(Slides)](session_01/Session_01-Cloud_Native_Architectures_and_Frameworks.pdf)

#### _Session 2: Pivotal Cloud Foundry Overview_ [(Slides)](session_02/Session_02-Pivotal_Cloud_Foundry-The_Cloud_Native_Platform.pdf)
  - [Lab 1 - From Zero to Pushing Your First Application](session_02/lab_01/lab_01.adoc)
  - [Lab 2 - Binding to Cloud Foundry Services](session_02/lab_02/lab_02.adoc)
  - [Lab 3 - Scaling Applications](session_02/lab_03/lab_03.adoc)
  - [Lab 4 - Monitoring Applications](session_02/lab_04/lab_04.adoc)

## Pivotal team
- Steve Womack, Pivotal Platform Architect, swomack@pivotal.io
