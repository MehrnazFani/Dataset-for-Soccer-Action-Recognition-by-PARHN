# Pose-projected Action Recognition Hourglass Network (PARHN) in Soccer

This repository is related to a [CRV paper](https://ieeexplore.ieee.org/abstract/document/8781607) with the same title. The pose-projected action recognition hourglass network (PARHN) performs player action recognition in soccer.  PARHN inputs, a soccer video sequence of arbitrary length in conjunction with the player's body-center in each frame, and outputs action type of the player. It is composed of four main components: 
+ Comp. 1 Stacked hourglass networks (or any state-of-the-art pose estimation network) for estimating pose of the player in all the frames of the sequence.
+ Comp. 2 Pose transformer and pose projector for obtaining a robust representation of the player pose. 
+ Comp. 3 Two LSTM layers that integrate the pose information throughout the input sequence are used. 
+ Comp. 4 A fully connected layer and a softmax classifier that perform the final action recognition.



<p align="center">
  <img width="800" src="https://github.com/MehrnazFani/Action-Recognition-in-Soccer/blob/81e0e43bbb4e4442ec2360f0ba23272c7bdacfb7/images/PARHN.jpg" alt="PAHRN"
</p>

Four types of actions (i.e., Shooting, Giving pass, Recieving pass and (Goalkeeper) Diving) are recognized.
