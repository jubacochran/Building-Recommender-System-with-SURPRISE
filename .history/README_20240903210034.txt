Dataset:
MovieLensLinks to an external site.

I'm using the smaller dataset. I attempted to use the larger dataset of 3M rows and also tried to sample this dataset by the order of .5,.3 and .1 but my knn_basic model kept crashing my python kernel. So I was forced to just use the 100k row dataset. Also when I modeled using the sample size approach most of the models were very overfit. It wasn't until I used the smaller set that I scored with better variance in my model. Also the 3M approach and .5 sample approach provided great scores but like I said Knn kept crashing my box. 

Model Selection:

I believe all of these models performed well except for the obvious, 'slopeOne'. The predictions seems to hype up the ratings a bit, HAHA. I suppose we all that one friend that thinks everything is just so amazing. But the scores were at least within reasonable range. I wouldn't throw out slope one but I'd use the surprise gridSearch to improve it's score. After looking over the clustering predictions I noticed that some of the estimates were also a bit high relative to the user rating but again, nothing that can't be fixed given more time. 

output-4.png

 

{'slopeOne': 1.3592529296875, 'knn_basic': 0.956397703965189, 'nmf': 0.9267144428647812, 'clustering': 0.9639395000566386, 'svd': 0.8744009718782094}
slopeOne predictions slice:

[Prediction(uid=1, iid='Toy Story (1995)', r_ui=4.0, est=4.711895386434586, details={'was_impossible': False}), Prediction(uid=1, iid='Grumpier Old Men (1995)', r_ui=4.0, est=3.922677009784783, details={'was_impossible': False}), Prediction(uid=1, iid='Heat (1995)', r_ui=4.0, est=4.602541510092789, details={'was_impossible': False})]
Model Selection:
KNN- this model has reasonable accuracy and variance. I'd put this one into production. 
