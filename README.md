# Pose-projected Action Recognition Hourglass Network (PARHN) in Soccer

This repository is related to a [CRV paper](https://ieeexplore.ieee.org/abstract/document/8781607) with the same title. The pose-projected action recognition hourglass network (PARHN) performs player action recognition in soccer.  PARHN inputs, a soccer video sequence of arbitrary length in conjunction with the player's body-center in each frame, and outputs action type of the player. It is composed of four main components: 
+ Component 1. Stacked hourglass networks (or any arbitrary pose estimation network can be used as well) for estimating pose of the player in all the frames of the sequence.
+ Component 2. Pose transformer and pose projector for obtaining a robust representation of the player pose. The numerical range of the player’s pose vector are regularized through pose projection component, by applying (ZCA)-whitening. 
+ Component 3. Two LSTM layers that integrate the pose information throughout the input sequence are used. 
+ Component 4. A fully connected layer and a softmax classifier that perform the final action recognition.



<p align="center">
  <img width="400" src=" alt="PAHRN
</p>

Four types of actions (i.e., Shooting, Giving pass, Recieving pass and (Goalkeeper) Diving) are recognized.
