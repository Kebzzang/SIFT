# SIFT
Feature Matching-SIFT

This code is for SIFT. Put your two images in the correct folder, and then choose the options. 
Keypoints between two images are matched by NNM(Nearest Neighbor Matching). With 
given descriptor fi for image1 and descriptor gj for image2, minimum distance between 
points is chosen as k and it is smaller than certain threshold T. But the problem is caused 
when the distinction of distances doesn’t seem that clear. For example, any kind of noise 
can disturb the feature matching and also, in case 1, d11=1.2, d12=1.23, d13=5 and in case 
2, d11=1.2, d12=5.2, d13=7.1. It is obvious that what we call as ‘feature’ would stick out in 
case of case 2. Therefore ratio based threshold method is used. Suppose that there is 
minimum distance as k1 second minimum distance as k2 and given ratio threshold as t. 
Only points that k1/k2 <= t would be survived. The other way to filter unreliable points is 
cross-checking. Only points that in image1->image2 and image2->image1

Case 1 is that performs the feature matching using NN without ratio based threshold T. It includes all the 
unreliable matching points so that the result is not that good. Set the both variables crossCheck and 
ratio_threshold as false.

Case 2 is using NN and refining result with cross-checking. Set the var crossCheck as true and ratio_threshold
as false. The result is better than Case 1.

Case 3 is the best option to perform the feature matching using both cross-checking and ratio based thresholding. 
Almost over 90 percent of keypoints will be filtered and the only reliable keypoints are shown in the final image. 

You can set the ratio threshold value by correcting the variable RATIO_THR between 0~1. 

![Matching_CCflase_RTfalse2623](https://user-images.githubusercontent.com/44967760/106306860-f5524b80-62a1-11eb-9af4-10d0d4232a5e.png)

![Matching_CCTrue_RTfalse1050](https://user-images.githubusercontent.com/44967760/106307052-35193300-62a2-11eb-8b05-724de1914b9c.png)

![Matching_CCTrue_RTTrue16](https://user-images.githubusercontent.com/44967760/106307064-377b8d00-62a2-11eb-955b-d38ebca2ce7d.png)
