# Pose-projected Action Recognition Hourglass Network (PARHN) in Soccer

This repository introduces PARHN and is linked with a [CRV paper](https://ieeexplore.ieee.org/abstract/document/8781607). PARHN is a network that performs player action recognition in soccer. It inputs, a soccer video sequence of arbitrary length, and outputs action type of the player. It comprises four main components: 
+ Comp. 1 Stacked hourglass networks (or any state-of-the-art pose estimation network) for estimating pose of the player in all the frames of the sequence.
+ Comp. 2 Pose transformer and pose projector for obtaining a robust representation of the player pose. 
+ Comp. 3 Two LSTM layers that integrate the pose information throughout the input sequence are used. 
+ Comp. 4 A fully connected layer and a softmax classifier that perform the final action recognition.



<p align="center">
  <img width="800" src="https://github.com/MehrnazFani/Action-Recognition-in-Soccer/blob/81e0e43bbb4e4442ec2360f0ba23272c7bdacfb7/images/PARHN.jpg" alt="PAHRN"
       
</p>

Four types of actions (i.e., Shooting, Giving pass, Recieving pass and (Goalkeeper) Diving) are recognized.

<p float="center">
    <img width="200" src="https://github.com/MehrnazFani/Action-Recognition-in-Soccer/blob/4486b7463c1589ba7b525b08abb449b473190739/images/RecievePass_sideView.gif"/>
   <img width="200" src="https://github.com/MehrnazFani/Action-Recognition-in-Soccer/blob/7aeb5d9eab6175e4e98d2cee9f8763070837d7b3/images/RecievePass_backView.gif"/>   
</p>
