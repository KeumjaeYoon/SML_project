# SML_project
Team Project in Statistical machine learning 


## Intro
All students collect 200 photos of their classes.

After training a model with CIFAR10, we test the model with a dataset we collected.


## Models
- Res2Net50
- SEResNext101
- EfficientNet_b0
- EfficientNet_lite2
- EfficientNet

## Loss
We believed that the how to train the model is as important as determining which the model to use.

So, we try to adapt various loss functions.

1. CrossEntropyLoss
<img width="775" alt="image" src="https://user-images.githubusercontent.com/76990589/206486186-12247539-ff9a-481c-bc02-0ca31c2c5665.png">

2. LabelSmoothing
<img width="787" alt="image" src="https://user-images.githubusercontent.com/76990589/206486229-b2379182-b7da-4a74-a5ac-b8c905455155.png">

3. ElasticLoss
<img width="720" alt="image" src="https://user-images.githubusercontent.com/76990589/206460495-4c710f51-7d25-41de-ae16-57c457e2cd7d.png">

- The plot below shows the difference in performance according to the loss function

<img width="322" alt="image" src="https://user-images.githubusercontent.com/76990589/206478140-ab5813b5-074f-473d-a4e8-a58c985b720c.png">


## Ensemble


## Result

