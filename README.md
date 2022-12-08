# SML_project
Team Project in Statistical machine learning 


## Intro
All students collect 200 photos of their classes.

After training a model with CIFAR10, we test the model with a dataset we collected.


## Models

We trained a few models, but we selected models have a good performance as final models.

- Res2Net50
- SEResNext101
- EfficientNet_b0
- EfficientNet_lite2
- EfficientNet
- ResNet50

## Loss
We believed that the how to train the model is as important as determining which the model to use.

So, we try to apply various loss functions about a multi-class classification.

1. CrossEntropyLoss
<img width="755" alt="image" src="https://user-images.githubusercontent.com/76990589/206486514-d089d623-23fc-4991-bbcf-99cf129e060b.png">


2. LabelSmoothing
<img width="768" alt="image" src="https://user-images.githubusercontent.com/76990589/206486463-29cb0848-36a9-462e-ae91-73b032f4bf91.png">


3. ElasticLoss
<img width="720" alt="image" src="https://user-images.githubusercontent.com/76990589/206460495-4c710f51-7d25-41de-ae16-57c457e2cd7d.png">

- The plot below shows the difference in performance according to the loss function

<img width="322" alt="image" src="https://user-images.githubusercontent.com/76990589/206478140-ab5813b5-074f-473d-a4e8-a58c985b720c.png">


## Ensemble
The results of a single model are as follows:

<img width="367" alt="image" src="https://user-images.githubusercontent.com/76990589/206517124-5c8ac9b8-8d55-4817-9561-b3976072710d.png">

Next, we check confusion matrixs of a single model, respectively.

<img width="297" alt="image" src="https://user-images.githubusercontent.com/76990589/206514125-71f0dcf2-3fdb-468a-b7c0-ee4c9f65715b.png">

we find that model has each power for classes, respectively.

For example, 



## Result

