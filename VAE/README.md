# Variational AutoEncoder (VAE)
In the project, we construct a VAE network to re-generate the animation images. First, we inputs the dataset of the animation images and prprocess the images. Second, we construct the VAE network including setting the hyper-parameters of number of layers, kernels of the convolution layer... . Then, we train the network and show re-generated images and generated images. Otherwise, we adjust the loss function by mutiply the KL term by 10 and 0, and compare the results of re-generated images and generated images between different KL term 
coefficients.

### 1. Data
The raw data contains 21551 anime images. [Here](https://drive.google.com/drive/folders/1940Je8vFA8zeTcwcAYXsyTbJSwEJxz8m?usp=sharing) is the images I used. The dataset is collected from [kaggle](https://www.kaggle.com/soumikrakshit/anime-faces).

### 2. Results
We train the network and show the results. The results include four parts：learning curve, re-generated images, generated images, and the change between two images. First, we use the loss tracked during the training phase to show the learning curve plot. Second, we choose some images randomly and show the original images and the re-gerated images. Then, we randomly generate some value of z to gernerate the images. Finally, we random generate two value of z and generate other value of z by interpolation between them. Show the change of the images because of the change of z.  

* Learning curve  
&emsp;
<div align="center">
<img src="https://github.com/sumiianng/image_storage/blob/main/VAE/loss.png" height="200px">
</div>

&emsp;
* Re-generated images  
&emsp;
<div align="center">
<img src="https://github.com/sumiianng/image_storage/blob/main/VAE/original_img2.png" height="200px">
<img src="https://github.com/sumiianng/image_storage/blob/main/VAE/regenerate_img2.png" height="200px">
</div>

&emsp;
* Generated images  
&emsp;
<div align="center">
<img src="https://github.com/sumiianng/image_storage/blob/main/VAE/generate_img2.png" height="200px">
</div>

&emsp;
* Change between two images  
&emsp;
<div align="center">
<img src="https://github.com/sumiianng/image_storage/blob/main/VAE/images_change2.png" width="200px">
</div>

### 3. Comparison
We mutiply the KL term by 100 and 0 in loss function. Show the reults of re-generated images and generated images and observe the effect of it.

* Mutiply the KL term by 100  
&emsp;
<div align="center">
<img src="https://github.com/sumiianng/image_storage/blob/main/VAE/original_img_100_2.png" height="200px">
<img src="https://github.com/sumiianng/image_storage/blob/main/VAE/regenerate_img_100_2.png" height="200px">
</div>
&emsp;
<div align="center">
<img src="https://github.com/sumiianng/image_storage/blob/main/VAE/generate_img_100_2.png" height="200px">
</div>
&emsp;
<div align="center">
<img src="https://github.com/sumiianng/image_storage/blob/main/VAE/images_change_100_2.png" width="200px">
</div>

&emsp;
*  Mutiply the KL term by 0  
&emsp;
<div align="center">
<img src="https://github.com/sumiianng/image_storage/blob/main/VAE/original_img_0_2.png" height="200px">
<img src="https://github.com/sumiianng/image_storage/blob/main/VAE/regenerate_img_0_2.png" height="200px">
</div>
&emsp;
<div align="center">
<img src="https://github.com/sumiianng/image_storage/blob/main/VAE/generate_img_0_2.png" height="200px">
</div>
&emsp;
<div align="center">
<img src="https://github.com/sumiianng/image_storage/blob/main/VAE/images_change_0_2.png" width="200px">
</div>
