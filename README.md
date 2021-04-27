# finalyearprojectmodels
pynb files used to create models 

Plant disease detection 
<br>

<h1 style="text-decoration: underline;"><b>DATA</b></h1>
<br>
we used the kaggle dataset 
<br>
<a> https://www.kaggle.com/vipoooool/new-plant-diseases-dataset</a> 
which has plant leaf images divided into 38 classes 
<br>
Each class represents a disease.
<br>
The dataset is split into training and validation set .
<br>
The train set has about 70K images and the validation set has about 17.5 k images. 
<br>
Its  80:20 split where 80 percent goes to the training set and 20 percent goes to the validation set.
<hr>
<h1><b>MODELS</b></h1>
We started with a simple model which doesn't use transfer learning and that  gave us 94 percent accuracy.
<br>
We tried transfer learning with mobilenet which gave us an accuracy of 98 percent.
<br>
we froze all the non batch normalization layers of mobilenet and added some batch normalization and dense layers at the end.
<br>
Mobilenet is light weight as compared to Resnet50.

We tried transfer learning with Resnet50 which gave us an accuracy of 99.8 percent 
we froze all the non batch normalization 
layers of Resnet50 and added batch normalization ,global pooling and dense layers at the end . 
This gave us an accuracy of 99.8 percent .

<hr>
<h3 style="text-decoration: underline;"><b>WHERE ARE THE MODELS USED</b></h3>

We went ahead with Resnet50 model and made a tflite model out of it . 

The Resnet50 model we trained wil be used in the webapp.
The tflite model will be used in Android app. 

we are also planning to make an API by using the Resnet50 model , which takes the picture and gives the disease.
