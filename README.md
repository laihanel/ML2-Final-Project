# ML2-Final-Project
This is a repository for the Final Project of Machine Learning 2 (Deep Learning) 

## DATASET
Data based on the UCF101 - Action Recognition Data Set https://www.crcv.ucf.edu/data/UCF101.php. UCF101 is an action recognition data set of realistic action videos, collected from YouTube, having 101 action categories. This data set is an extension of UCF50 data set which has 50 action categories.

We focus on the playing Musical Instruments group. They have 1268 clips in total, and each of them contains 4-7 videos, and the videos from the same group have some similar characteristics, such as background, characters, etc. This dataset is large enough to train a deep network.

## FRAMEWORK
Since we want to customize the network ourselves, PyTorch is the best option for debugging and changing network architectures.

## NETWORK
The network we used is based on CNN3D. The 3D convolution kernel is more efficient for spatiotemporal feature learning. Tran et. (2015) proposes a network called C3D, and we will customize it with different kernel size or neural size to learn this architecture more clearly.
![Architecture of VC3D Network](image/vc3d.png)

## RESULT
In this project, we implemented a modified version of the C3D network, VC3D to better deal with the video classification task. While it achieved 100% accuracy in the Playing Instruments group for a random heldout test set that consisted of 15% of the full data, robustness issues were exposed when inference on videos collected from external sources.
![Results](image/output.png)

## Reference
Tran, D., Bourdev, L., Fergus, R., Torresani, L., & Paluri, M. (2015). Learning spatiotemporal features with 3d convolutional networks. In Proceedings of the IEEE international conference on computer vision (pp. 4489-4497).



