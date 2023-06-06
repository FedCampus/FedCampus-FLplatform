# Subwork\_Tianjun



### To 6/4

#### Progress

- Meet with Prof. Luo, Jiaqi & Aicha, Steven & Johnny.
- Briefly read two papers
    - *FedStack: Personalized activity monitoring*
        - This paper does not have the code, so I currently do not use it.
    
    - *PerFedRec: Personalized Federated Recommendation*
        - This paper has its code on github.
        - However, this paper requires knowledge for GNN (Graph Nerual Network), and other algorithms / tricks. These ML knowledge is now a little difficult for me, so I might use it in the future.
    

#### Next Week's Plan

- Read the projects Jiaqi gave me. 
  - I will open up new `md` files to record my notes/understanding for those projects/papers.

- Continue learning ml/dl.
  - Prof. Luo suggests me to spend some of my time on it.
- Start to implement code.

### To 4/14

Briefly Read scaffold (non IID) (Will add to this point)

#### Next Plan:

- Run more simulations on Flower/FedML, Read the code

- Record progress more concisely

- See how to handle NON-iid data

- Learn other federated learning algorithm (Now I know Fedavg/Fedprox/something about scaffold)

- See how privacy algorithm be used in Federated Learning

### To 4/10

- Read many codes in FedML. Now figure out `FedML/python/examples/centralized/main.py` is the core code to `load` `train` , `FedML/python/fedml/cli/` has main codes of communicate and aggregate.

- Read about FedProx (_Heterogeneous_?).

**FedProx**

Different epochs

With limit local updates, it does not need to manually set the epochs

$3.$ Rebuild the anaconda, now FedML simulations can be run on my own computer; Flower installed (Spend some time on it)

### To 4/6

- Read the code in `FedML/python/fedml/distributed/FedAvg`, which is the core of FedAvg\

- Watched a movie Tutorial of FedML, Link: https://www.bilibili.com/video/BV1jK411N7gS?vd\_source=9ebbad46fdc1ff2caa82dc1a6ae88e96\

### To 4/3

- Successfully run simulations and programs in `python/app` , and handled the issue with open-mpi. I open a Ubuntu 22.04 vcm on the dku platform to handle this. (It seems my arm Mac cannot run open-mpi successfully, might be affected by mpich contradiction).\

- Also trying to test this subwork\_template\
