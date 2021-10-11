# Video Shopper App


<h1>Content:</h1>
<a href="#obj" >1. Problem Statement</a><br>
<a href="#sol" >2. Solution </a><br>
<a href="#pre" >3. Preprocessing </a><br>
<a href="#model" >4. Model</a><br>
<a href="#res" >5. Result</a><br>
<a href="#team" >6. Team Members</a><br>
<hr>
<h1 id="obj">1. Problem Statement</h1>

<strong>
  Celebrities are the biggest influencer on the fashion trends. While watching a movie or a favorite web series on any of the OTT platform, have you ever liked the outfit or shoe wore by actors/actresses so much that you also wanted to buy it. But even after spending hours on e-commerce websites, you could not find the similar outfit or fashion accessory. Everyone wants to be stylist and dressed up like a celebrity, but it is very hard to find similar clothing on internet. To develop an app against this that will scan and give similar images compared to the actor and actresses' clothes.
</strong>
<br>

<h1 id="sol">2. Solution:</h1>

We developed an AI-based API, which can be integrated with various OTT platforms. 
It will automatically take the screenshot of the screen and give suggestions to buy similar products, based on our ML model's prediction when clicked on Find Similar button. 
So while watching a video/movie, pause it, click on the button, and we will provide you with links of similar products for shopping.



<h1 id="pre">3. Preprocessing:</h1>
We use this python script for preprocessing our data as per our needs.

import os
path = "/home/prince/Documents/Rough/"
for filename in os. listdir(path):
    print(filename)
    filename_without_ext = filename.split("_")[0]
    extension = ".jpg"
    new_file_name = filename_without_ext+extension
    os.rename(path+filename,path+new_file_name)

<h1 id="model">4. Model:</h1>

To classify the images, we used Xception model from Google and used it’s global average pooling layer(second last layer) to extract the feature vector and apply Knn to predict top-k similar feature vector in our database. (In our case we k=30). 

<h1 id="res">5. Result:</h1>
<img src="img/Screenshot from 2021-05-30 15-56-53.png">
<img src="img/Screenshot from 2021-05-30 15-57-11.png">
<img src="img/Screenshot from 2021-05-30 15-57-20.png">
<img src="img/Screenshot from 2021-05-30 15-57-24.png">
<img src="img/Screenshot from 2021-05-30 15-57-55.png">
<img src="img/Screenshot from 2021-05-30 15-58-09.png">
<img src="img/Screenshot from 2021-05-30 15-58-28.png">
<img src="img/Screenshot from 2021-05-30 15-58-35.png">

<h1 id="team">6. Team Members</h1>
<strong>1. Harshit Jain</strong><br>
<strong>2. Aryan Garg</strong><br>
<strong>3. Sameer Jain</strong><br>
<strong>4. Prince Arya</strong><br>
