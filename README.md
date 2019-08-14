# Deecamp27
============
This is the Projet to generate the closed boundary of a image
      we have tried many difference methods to slove it
            we did not reach the point we except, but get some results.
            

HED:
------------
code:  https://github.com/s9xie/hed <br>
paper:  http://openaccess.thecvf.com/content_iccv_2015/html/Xie_Holistically-Nested_Edge_Detection_ICCV_2015_paper.html
     


we use the pretrained model directly to our project, we get excited at first, Because it gives us a lot of confidence, he has a much better effect than the traditional boundary detect operator(such as Canny, Sobel), and it is also firm that we use a learning-based approach to solve the problem.Results are as follows:


![Original image](https://github.com/USTCzzl/Deecamp27/blob/master/image/original/girl_origin.jpg){:height="100px" width="400px"}
![Edge image](https://github.com/USTCzzl/Deecamp27/blob/master/image/sketch/final.png){:height="100px" width="400px"}
![vector image](https://github.com/USTCzzl/Deecamp27/blob/master/image/vector/final_2.png){:height="100px" width="400px"}


Although it has achieved relatively good results, our project requires that the external wireframe be closed, or find a way to detect the unclosed point, which brings us some trouble, outside the wireframe based on the hed method. The border is very thick, we use the skeleton algorithm to thin the line, and then use the power-off detection algorithm, which can solve the problem better.



In order to prevent the outermost wireframe from closing, we also use an energy-based algorithm (snake, level set) to enclose the outer frame at the outermost layer, which also has a good effect.
