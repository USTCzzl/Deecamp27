# Deecamp32
============
.<img src="https://github.com/USTCzzl/Deecamp27/deecamp_poster 32.pdf"/>

This is the Projet to generate the closed boundary of a image
      we have tried many difference methods to slove it
            we did not reach the point we except, but get some results.
            

HED:
--------
code:  https://github.com/s9xie/hed <br>
paper:  http://openaccess.thecvf.com/content_iccv_2015/html/Xie_Holistically-Nested_Edge_Detection_ICCV_2015_paper.html
     


we use the pretrained model directly to our project, we get excited at first, Because it gives us a lot of confidence, he has a much better effect than the traditional boundary detect operator(such as Canny, Sobel), and it is also firm that we use a learning-based approach to solve the problem.Results are as follows:

.<img src="https://github.com/USTCzzl/Deecamp27/blob/master/image/original/girl_origin.jpg" width="200" height="300"/>
.<img src="https://github.com/USTCzzl/Deecamp27/blob/master/image/sketch/final.png" width="200" height="300"/>
.<img src="https://github.com/USTCzzl/Deecamp27/blob/master/image/vector/final_2.png" width="200" height="300"/>


Although it has achieved relatively good results, our project requires that the external wireframe be closed, or find a way to detect the unclosed point, which brings us some trouble, outside the wireframe based on the hed method. The border is very thick, we use the skeleton algorithm to thin the line, and then use the power-off detection algorithm, which can solve the problem better.





In order to prevent the outermost wireframe from closing, we also use an energy-based algorithm (snake, level set) to enclose the outer frame at the outermost layer, which also has a good effect.
![](https://github.com/USTCzzl/Deecamp27/blob/master/image/levelset/level_set.png)<br>
code:https://github.com/USTCzzl/Deecamp27/blob/master/image/levelset/level_set.cpp






















RCF
-----------

code:https://github.com/yun-liu/rcf<br>
paper: http://openaccess.thecvf.com/content_cvpr_2017/html/Liu_Richer_Convolutional_Features_CVPR_2017_paper.html 




BDCN
------------
code:https://github.com/pkuCactus/BDCN<br>
paper:https://arxiv.org/pdf/1902.10903.pdf


Both of the methods we have tried, we retrained the model, but the results is not satisfied, there are some enhance but not enough, the three method almost some, only some difference in network structure,i will put my code in github.now let me show some difference way to thinking the problem.



Pip2Pix & Cycle Gan
---------

this is a method from Gan, but someone has used it to do the edge search problem
      the paper is here: https://arxiv.org/abs/1901.00542<br>
      code: https://github.com/mtli/PhotoSketch
      it indeed get progress in BSDS500, but it lack of generalization in our datasets, the result is very abstract.but style transfer can work in this problem, our group member use cycle gan train the dataset about 4 days get wonderful results, i will show some picture in the future..
     
     
     
     
code
--------
if you want to test in your own image, you can download the test document(only HED && RCF),there are three different methods.
      

