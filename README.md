# Question Answering System using End to End Memory Networks

This project is the implementation of End to End Memory Networks to build Question Answering System. It takes small story and query as an input and predicts a possibe answer to the query. Here we have used Facebook Babi Dataset to train the model. After training, user can give similar stories and query as input and it would give you accurate results.

## Dependencies

* tensorflow
* keras
* functools
* tarfile
* re

## Architecture of End to End Memory Networks
![alt text](https://github.com/prashil2792/Question-Answering-System-Deep-Learning/blob/master/images/architecture.png)

## Results/Observations

|Layers 						|Dropouts			|Batch-size	| Epochs 	|Results	|
| ----------------------------- | ----------------- | --------- | --------- | --------- |
|LSTM(32)						|(0.3)				|32			|100		|94.6%		|
|LSTM(64)						|(0.3)				|32			|100		|96.5%		|
|LSTM(32), LSTM(32)				|(0.5, 0.5)			|32			|100		|92.4%		|
|LSTM(32), LSTM(32)				|(0.5, 0.5)			|32			|200		|96.9%		|
|GRU(32)						|(0.3)				|32			|100		|86.4%		|
|GRU(64)						|(0.3)				|32			|100		|87.4%		|
|GRU(32), GRU(32)				|(0.5, 0.5)			|64			|100		|52.6%		|

* The models with two or more layers required more training since there are more parameters that need to be set, but then have greater accuracies than the other models once trained completely.
* Overall, LSTM based models performed better than GRU based models for this task.

## References

- Jason Weston, Antoine Bordes, Sumit Chopra, Tomas Mikolov, Alexander M. Rush,
  "Towards AI-Complete Question Answering: A Set of Prerequisite Toy Tasks",
  (http://arxiv.org/abs/1502.05698)
- Sainbayar Sukhbaatar, Arthur Szlam, Jason Weston, Rob Fergus,
  "End-To-End Memory Networks",
  (http://arxiv.org/abs/1503.08895)
