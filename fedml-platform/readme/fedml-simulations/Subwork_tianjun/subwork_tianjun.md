Subwork_Tianjun
===============

### To 7/7

- Finish re-split data. Now data are separated by labels.
- Finish FedRS. 
- Finish LSTM on Data.
- Detail result: please see June evaluation.

### To 6/28

- Begin to implement FedRS.

  - It is a straight forward algorithm. When we want to deal with non-iid problem. Suppose each client only has several label types but not all, this softmax builds on decreasing the predicting score for unallocated label types in softmax regression. 

    ```
    scores[i] *= alpha 
    	i not in types
      0 <= alpha <= 1
    ```

  - The challenges are:

    - Re-split the data. This time, data will be splitted according to labels ?. 
    - Seems directly `fit`  does not work.

- See the Flwr tutorial, already watched that vedio, will try apply this.

- More models to be applied

  - LSTM

### To 6/26

- **Fix two curcial bugs for 6/21's work !!!**

  - Shallow Copy v.s. Deep Copy

    - Find the accuracy keeps increasing across clients.

      - Ideal:

        - ```
          client0:
          	ac epoch 0: 0.88
          	ac epoch 1: 0.93
          client1:
          	ac epoch 0: 0.87
          	ac epoch 1: 0.92
          Average ...
          ```

      - Real:

        - ```
          client0:
          	ac epoch 0: 0.88
          	ac epoch 1: 0.93
          client1:
          	ac epoch 0: 0.92
          	ac epoch 1: 0.98
          Average ...		
          ```

  - tf.keras.models.clone_model does not restore the weights!!

    - Set `learning_rate = 0` to debug

- More functions:

  - Weight averaging
  - FedAvg with MLP

- Discussion of 'W' Function

  - Real Function might have more “hole” , local minimum.

  - Real test on FedAvg MLP.

    - ```
      model = Sequential()
      model.add(Dense(128, input_dim=input_size, activation='relu'))
      model.add(Dense(128, activation='relu'))
      model.add(Dense(128, activation='relu'))
      model.add(Dense(128, activation='relu'))
      model.add(Dense(128, activation='relu'))
      model.add(Dense(64, activation='relu'))
      model.add(Dense(output_size, activation='softmax'))
      ```

    - The first round, each client got 0.98 acc, while averaging got 0.80 acc. 
    - The second round, each client got 0.98 acc, averaging got 0.99 acc, which becomes nice acc.

- Two questions:

  - Running the simple MLP model on GPU RTX Titan (from DKU) is much slower than my Computer CPU
  - Do I need to seperate the validation_data in each client?

### To 6/7

-   Record fundamental dp method.

### To 6/6

-   Read and record [*Communication-Efficient Learning of Deep Networks from Decentralized Data*](Paper\_notes/Notes\_0.md)

### To 6/4

#### Progress

-   Meet with Prof. Luo, Jiaqi & Aicha, Steven & Johnny, Beilong.

-   Briefly read two papers

    -   *FedStack: Personalized activity monitoring*

        -   This paper does not have the code, so I currently do not use it.

    -   *PerFedRec: Personalized Federated Recommendation*

        -   This paper has its code on github.

        -   However, this paper requires knowledge for GNN (Graph Nerual
            Network), and other algorithms / tricks. These ML knowledge is now a
            little difficult for me, so I might use it in the future.

#### Next Week's Plan

-   Read the projects Jiaqi gave me.

    -   I will open up new `md` files to record my notes/understanding for those
        projects/papers.

-   Start to implement code.

-   Continue learning ml/dl.

    -   Prof. Luo suggests me to spend some of my time on it.

### To 4/14

Briefly Read scaffold (non IID) (Will add to this point)

#### Next Plan:

-   Run more simulations on Flower/FedML, Read the code

-   Record progress more concisely

-   See how to handle NON-iid data

-   Learn other federated learning algorithm (Now I know
    Fedavg/Fedprox/something about scaffold)

-   See how privacy algorithm be used in Federated Learning

### To 4/10

-   Read many codes in FedML. Now figure out
    `FedML/python/examples/centralized/main.py` is the core code to `load train`
    , `FedML/python/fedml/cli/` has main codes of communicate and aggregate.

-   Read about FedProx (*Heterogeneous*?).

**FedProx**

Different epochs

With limit local updates, it does not need to manually set the epochs

$$3.$$ Rebuild the anaconda, now FedML simulations can be run on my own
computer; Flower installed (Spend some time on it)

### To 4/6

-   Read the code in `FedML/python/fedml/distributed/FedAvg`, which is the core
    of FedAvg  
    
-   Watched a movie Tutorial of FedML, Link:
    https://www.bilibili.com/video/BV1jK411N7gS?vd_source=9ebbad46fdc1ff2caa82dc1a6ae88e96  
    

### To 4/3

-   Successfully run simulations and programs in `python/app` , and handled the
    issue with open-mpi. I open a Ubuntu 22.04 vcm on the dku platform to handle
    this. (It seems my arm Mac cannot run open-mpi successfully, might be
    affected by mpich contradiction).  
    
-   Also trying to test this subwork_template  
