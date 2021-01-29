# SIFT
Feature Matching-SIFT

This code is for SIFT. Put your two images in the correct folder, and then choose the options.

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
