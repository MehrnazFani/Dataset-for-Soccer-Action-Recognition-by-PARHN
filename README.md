# Pose-projected Action Recognition Hourglass Network (PARHN) in Soccer

This repository is related to a [CRV paper](https://ieeexplore.ieee.org/abstract/document/8781607) with the same title. The pose-projected action recognition hourglass network (PARHN) performs player-level action recognition in soccer. Four types of actions (i.e., Shooting, Giving pass, Recieving pass and (Goalkeeper) Diving) are recognized. As explained in the paper and summerazied here, PARHN inputs, a soccer video sequence of arbitrary length in conjunction with the player's body-center in each frame, and outputs action type of the player. PARHN is composed of four main components: 
+ Component 1. Stacked hourglass networks (or any arbitrary pose estimation network can be used as well) for estimating pose of the player in all the frames of the sequence.
+ Component 2. Pose transformer and pose projector for obtaining a robust representation of the player pose. The numerical range of the player’s pose vector are regularized through pose projection component, by applying (ZCA)-whitening. 
+ Component 3. Two LSTM layers that integrate the pose information throughout the input sequence are used. 
+ Component 4. A fully connected layer and a softmax classifier that perform the final action recognition.



<p align="center">
  <img width="400" src="https://github.com/MehrnazFani/Shot-Transition-Detection/blob/e4799ace3d68f7f4e7cc886e8d0e509ee83213f8/img-for-readme/CT-soccer.png" alt="PAHRN
</p>
