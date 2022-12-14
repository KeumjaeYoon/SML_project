# SML_Team project

Team Project in Statistical machine learning 


## Intro

All students collect 200 photos of their classes.

After training a model with CIFAR10, we test the model with a dataset we collected.


## Models

We trained a few models, but we selected models have a good performance as final models.

- ### EfficientNet

  - [Efficientnet: Rethinking model scaling for convolutional neural networks](http://proceedings.mlr.press/v97/tan19a.html)

<p align="center"><img width="1200" alt="image" src="https://user-images.githubusercontent.com/76990589/206531307-b4da829c-5b7c-4d75-b798-fc4dd6ed6326.png">

_____________________
  
  
- ### EfficientNetV2

  - [Efficientnetv2: Smaller models and faster training](http://proceedings.mlr.press/v139/tan21a.html)

<p align="center"><img width="1200" alt="image" src="https://user-images.githubusercontent.com/76990589/206532134-a11ba31c-5d6b-4f93-8fcb-8690a978a5e8.png">

_____________________

- ### ResNet
  
  - [Deep residual learning for image recognition](https://openaccess.thecvf.com/content_cvpr_2016/html/He_Deep_Residual_Learning_CVPR_2016_paper.html)

It is a model used as a baseline in many studies.

<p align="center"><img width="1000" alt="image" src="https://user-images.githubusercontent.com/76990589/206531713-d06be0a9-1e95-4c96-8c89-eed657ccade0.png">

_____________________

- ### ResNext & Res2Net

  - [Aggregated Residual Transformations for Deep Neural Networks](https://arxiv.org/abs/1611.05431)
  - [Res2net: A new multi-scale backbone architecture](https://ieeexplore.ieee.org/abstract/document/8821313)  
  
<p align="center"><img width="1200" alt="image" src="https://user-images.githubusercontent.com/76990589/206532661-8eda6a12-5856-4947-beff-9c88db7cd3a3.png">

_____________________

- ### SEResNet

  - [Squeeze-and-Excitation Networks](https://arxiv.org/abs/1709.01507)
  
<p align="center"><img width="1200" alt="image" src="https://user-images.githubusercontent.com/76990589/206532809-cac890d6-fe44-498f-a516-c9c9b4d4f8bd.png">

_____________________

## Loss
We believed that the **how to train the model** is as important as determining which the model to use.

So, we try to apply various loss functions about a multi-class classification.

- ### CrossEntropyLoss
  
  - <p align="center"><img width="755" alt="image" src="https://user-images.githubusercontent.com/76990589/206486514-d089d623-23fc-4991-bbcf-99cf129e060b.png">

_____________________

- ### LabelSmoothing

  - [When does label smoothing help?](https://proceedings.neurips.cc/paper/2019/hash/f1748d6b0fd9d439f71450117eba2725-Abstract.html)
  
<p align="center"><img width="768" alt="image" src="https://user-images.githubusercontent.com/76990589/206486463-29cb0848-36a9-462e-ae91-73b032f4bf91.png">

_____________________

- ### ElasticLoss

  - [ElasticFace: Elastic Margin Loss for Deep Face Recognition](https://openaccess.thecvf.com/content/CVPR2022W/Biometrics/html/Boutros_ElasticFace_Elastic_Margin_Loss_for_Deep_Face_Recognition_CVPRW_2022_paper.html)
  
<p align="center"><img width="720" alt="image" src="https://user-images.githubusercontent.com/76990589/206460495-4c710f51-7d25-41de-ae16-57c457e2cd7d.png">

_____________________

The plot below shows the difference in performance according to the loss function

<p align="center"><img width="500" height="500" alt="image" src="https://user-images.githubusercontent.com/76990589/206478140-ab5813b5-074f-473d-a4e8-a58c985b720c.png">


## Ensemble

The results of a single model are as follows:

<p align="center"><img width="500" height="500" alt="image" src="https://user-images.githubusercontent.com/76990589/206517124-5c8ac9b8-8d55-4817-9561-b3976072710d.png">

Next, we check confusion matrixs of a single model, respectively.

<p align="center"><img width="700" height="700" alt="image" src="https://user-images.githubusercontent.com/76990589/206514125-71f0dcf2-3fdb-468a-b7c0-ee4c9f65715b.png">

We find that models have each power for classes, respectively.

For example, there are models A and B have a similar performance.
However, model A has a good performance for class "dog", but model B does not. 
On the contrary,  model B has a good performance for class "cat", but model A does not.

**Considering the characteristics of each model**, we decided to make an ensemble model using soft voting.
We try to **find an optimal combination** for the selected models.

<p align="center"><img width="500" height="500" alt="image" src="https://user-images.githubusercontent.com/76990589/206524443-59ff9b98-fa5b-4ba3-a09d-7648d5851b6d.png">

The Confusion matrix for the ensemble model is as follows:

<p align="center"><img width="500" height="500" alt="image" src="https://user-images.githubusercontent.com/76990589/206525302-ca73f102-6b11-4dfe-8f58-02cd76afc32b.png">

**Visualization with Grad-CAM**

<p align="center"><img width="664" alt="image" src="https://user-images.githubusercontent.com/76990589/206525516-540aaec2-a034-453e-a6db-24c737d5079c.png">


## Result

As mentioned at the beginning, we used the 2400 data we collected as a test dataset to verify the performance.

<p align="center"><img width="1400" height="700" alt="image" src="https://user-images.githubusercontent.com/76990589/206528158-0dd359ac-8d5c-4906-b670-0d8f1832b6f4.png">

Although the performance of a single model was poor, we show robustness in overall performance **because we implemented an ensemble.**
