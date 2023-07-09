# June Evaluation

## Goal attainment

- Finish most part of the reproduction. *CloudyFL: A Cloudlet-Based Federated Learning Framework for Sensing User Behavior Using Wearable Devices*
  - Do experiments on IID data.
    - Centralized softmax regression + MLP($84\%$, $98\%$)
    - FedAvg softmax regression + MLP ($82\%$, $98\%$)
  - non-IID data (give each clients different labels, $40$ rounds)
    - FedAvg + softmax ($52\%$)
    - FedAvg + MLP ($60\%$)
    - FedAvg + LSTM ($79\%$)
    - FedRS + LSTM (also around $79\%$)
  - Write $3$ simulation files:
    - First one: Do centralized and FedAvg, just mainly follow how the Author write, but convert torch to tensorflow
    - Second one: Rewrite getData function, which becomes time series and can apply LSTM/RNN
    - Third one: Rewrite all codes, re-split the data, rewrite softmax to be a restrict softmax in the last layer. In this stage, ML-models are easy to apply.
- Read some papers.
  - CloudyFL: A Cloudlet-Based Federated Learning Framework for Sensing User Behavior Using Wearable Devices
  - Personalized Federated Recommendation via Joint Representation Learning, User Clustering, and Model Adaptation
  - Communication-Efficient Learning of Deep Networks from Decentralized Data
  - FedStack: Personalized activity monitoring using stacked federated learning

## Skills development

- Learned ML models
  - LR(softmax R) + SVM + MLP + CNN + RNN + LSTM
  - Knowledges are learned from
    - Dive into Deep Learning (https://d2l.ai)
    - CS231N
    - A book
    - Ask others
- Learned Federated Learning
  - FedAvg
  - FedRS
- Learned DP (here means differential privacy)
