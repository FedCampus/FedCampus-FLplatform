---
description: The remaining work, ongoing work, and finished work
---

# Project Overview

## Project Introduction

Federated learning is a machine learning technique that trains a model across multiple decentralized edge devices or servers holding local data samples without sharing data, thus allowing it to address critical issues such as data privacy, security, access rights, and access to heterogeneous data. Its applications are spread over several industries.&#x20;

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

One related area with FL is edge computing, where the parties are edge devices. Many studies try to integrate FL with mobile edge systems. The clients (e.g., an app running on mobile phones) store the necessary training data locally (with limited time and quantity). In many cases, the app will already have stored this data (e.g., a text messaging app must store text messages, and a photo management app already stores photos). However, in some cases, additional data or metadata might need to be maintained, e.g., user interaction data, to provide labels for a supervised learning task.

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption><p>The comparison among some existing FL platforms</p></figcaption></figure>

This project is to build an FL platform with FedML. This platform involves wireless networks (e.g., 5G, WIFI), edge devices (e.g., mobile phones, wearable devices, and IoTs), and benchmark algorithms implementation. Future work will be conducted based on this platform, e.g., experiment/analysis on statistical/system heterogeneity, more benchmark implementation, and privacy/security techniques.

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption><p>FedML Structure</p></figcaption></figure>

## Process Overview&#x20;

| Timeline            | Subworks                                                                                 | Contributors | Progress |
| ------------------- | ---------------------------------------------------------------------------------------- | ------------ | -------- |
|                     | [Subwork Template](fedml-platform/project-overview/subwork-template.md)                  |              | 100/100  |
| During Semester     | Pre-requisite: [FedML simulations](fedml-platform/project-overview/fedml-simulations.md) | All          | --       |
| During Semester     | Pre-requisite: Simulation Implementation with Different Experimental Settings            | All          | 0/100    |
| 1st month (Summer)  | Deployment on Android (data access, platform management and training stability)          | Liu Rongfan  | 0/100    |
| 1 month (Summer)    | Implementation of Additional algorithms (Simulation)                                     | Wang Yike    | 0/100    |
| 1\~2 month (Summer) | On-device algorithms implementation, analysis                                            | Sun Tianxuan |          |
| Before summer ends  | Test platform, on-device FL applications                                                 |              | 0/100    |

## Conclusion
