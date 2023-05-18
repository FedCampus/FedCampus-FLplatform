---
description: The remaining work, ongoing work, and finished work
---

# Project Overview

## Project Introduction

Federated learning is a machine learning technique that trains a model across multiple decentralized edge devices or servers holding local data samples without sharing data, thus allowing it to address critical issues such as data privacy, security, access rights, and access to heterogeneous data. Its applications are spread over several industries.

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

One related area with FL is edge computing, where the parties are edge devices. Many studies try to integrate FL with mobile edge systems. The clients (e.g., an app running on mobile phones) store the necessary training data locally (with limited time and quantity). In many cases, the app will already have stored this data (e.g., a text messaging app must store text messages, and a photo management app already stores photos). However, in some cases, additional data or metadata might need to be maintained, e.g., user interaction data, to provide labels for a supervised learning task.

## FL Tasks in FedCampus (Model Training & Deployment)

* **Sleep tracking:** track sleep patterns (FL prediction on next days), **s**_**leep quality prediction**_ (other labelled data, and FL model deployment)_._
* **Track physical activity:** Federated learning to track physical activity, such as _**steps taken, distance traveled, and calories burned.**_ This information can be used to improve fitness and reduce the risk of obesity and other chronic diseases.
* **Personalize recommendations:** Federated learning to _**personalize recommendations**_ for physical activity, such as suggested workouts or goals. This information can help users stay motivated and reach their fitness goals.
*
* ....

These are just a few examples of the many ways that federated learning can be used on wearable devices' data. As federated learning technology continues to develop, we can expect to see even more innovative applications of this technology in the future.

These are just a few examples of the many ways that federated learning can be used on step counts and other data from wearable devices. As federated learning technology continues to develop, we can expect to see even more innovative applications of this technology in the future.

## Process Overview

| Person              | Work                                                                                                                                                     | Time Due                                           |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- |
| Steven              | Platform setup, handling FL system setup on Flower                                                                                                       | By the End of May                                  |
| Johnny              | Manage Devices All in one, IoTs, wearable devices, Mobile phones, etc.                                                                                   | By the End of May                                  |
| Steven, Johnny      | <p>Design for Cost-efficiency FL Platform<br>Scalability<br>Reliability [FL pipeline]<br>Evaluation and Testing: Experiments on platform performance</p> | By the End of Summer                               |
| Aicha, Yuan Tianjun | Select an FL task and implement it on FL simulation                                                                                                      | By the Mid of June (FL task)                       |
| Aicha, Yuan Tianjun | Model training & deployment \[Experiment Analysis: evaluate on-device training with system heterogeneity]                                                | By the End of Summer (Model training & deployment) |

### Timelines & Plans -- System

* Steven: Platform setup, handling FL system setup on Flower... (By the End of May)
* Steven & Johnny _(By the End of Summer)_
  * Design for **Cost-efficiency FL Platform** & Manage Devices
    * Other devices, all in one platform, e.g. IoT devices, etc.
  * (Scalability) e.g. increasing amount of data and traffic.
  * (Reliability) e.g. train and deploy models quickly and efficiently. \[_FL pipeline_]
  * Evaluation and Testing: Experiments on platform performance, e.g. latency, scalability, reliability, etc.

### Timelines & Plans -- Algorithms

* Aicha & Yuan Tianjun:
  * FL tasks -- Select a task, e.g. sleep tracking, etc., and implement it on FL simulation. _(By the Mid of June)_
  * Model training & deployment... (**Experiment Analysis**: evaluate on-device training with system heterogeneity ) _(By the End of Summer)_
* Tang Beilong
  * Privacy techniques: e.g. differential privacy, etc. _(By the End of Summer)_

## Evaluation

* Completeness
* Publications

## Conclusion
