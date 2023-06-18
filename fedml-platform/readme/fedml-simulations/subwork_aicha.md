* 12/4

Deepened my knowledge about algorithm design more spceifically FedAvg. I looked for papers about this algorithm and chose to start with this one: https://arxiv.org/pdf/1602.05629.pdf 

Currently trying to understand the math behind this algorithm by reading lectures about it. For example:
https://www.stat.cmu.edu/~ryantibs/convexopt-F18/scribes/Lecture_9.pdf;
https://openlearninglibrary.mit.edu/courses/course-v1:MITx+6.036+1T2019/courseware/Week4/gradient_descent/?activate_block_id=block-v1%3AMITx%2B6.036%2B1T2019%2Btype%40sequential%2Bblock%40gradient_descent


## Summer

ToDo Week of 22/5
- refine my knowledge in Deep Learning: finish this class  http://introtodeeplearning.com/
- test and run simulations on Setven's work

ToDo Week of 29/5
- FL tasks : Select sleep tracking and implement it on FL simulation. 
- details to be added later as I read papers and learn about this task
-> chosed paper: FedMCRNN: Federated Learning using Multiple Convolutional Recurrent Neural Networks for Sleep Quality Prediction
https://dl.acm.org/doi/10.1145/3512731.3534207
used data: https://datasets.simula.no/pmdata/; paper: https://dl.acm.org/doi/10.1145/3339825.3394926



ToDo Week 6/5
- Finish the implemention of sleep tracking. Simulate the paper mentioned above.
- Use other algorithms.

Implementation details: 
  Data Preparation: Accodring to the paper, only six important activity categories were used to assess sleep quality effectively: calories, distance, sedentary minutes, lightly activity minutes, moderately active minutes, and very active minutes. _I still need to research the reason behind this choice_
  The used files are .json. So far, I've completed 70% of the cleaning of the data (remove duplicates, modify empty values) of one participant out of 16. The cleaning of the data of all participants are similar. Two participants have incomplete data, so they'll not be considered in the study. After cleaning all the data, the originally sepearte json data files will be merged into a single file for easier manipulation later.


ToDo Week 6/12
- Timeseries analysis of the data set/work on data windowing
- Application of MLP, CNN, and LSTM

- Data Windowing: function that can generate any form of a window by selecting the input width, shift, and output width
- Data preparation: (70%, 20%, 10%) split for the training, validation, and test sets
  data is not randomly shuffled before training to ensure that chopping the data into windows of consecutive samples is still possible, and to ensure that the 
  validation/test results are more realistic, being evaluated on the data collected after the model was trained.
- Normalization: subtract the mean and divide by the standard deviation of each feature

- Applying MLP, CNN, and LSTM, however, the accuracies are very low.

ToDo Week 6/18
- Achieve the best accuracy for training

