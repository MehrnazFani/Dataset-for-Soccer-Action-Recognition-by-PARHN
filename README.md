# Pose-projected Action Recognition Hourglass Network (PARHN) in Soccer

This repository introduces PARHN and is linked with a [CRV paper](https://ieeexplore.ieee.org/abstract/document/8781607). PARHN is a network that performs player action recognition in soccer. It inputs, a soccer video sequence of arbitrary length, and outputs action type of the player. It comprises four main components: 
+ Comp. 1 Stacked hourglass networks (or any state-of-the-art pose estimation network) for estimating pose of the player in all the frames of the sequence.
+ Comp. 2 Pose transformer and pose projector for obtaining a robust representation of the player pose. 
+ Comp. 3 Two LSTM layers that integrate the pose information throughout the input sequence are used. 
+ Comp. 4 A fully connected layer and a softmax classifier that perform the final action recognition.



<p align="center">
  <img width="800" src="https://github.com/MehrnazFani/Action-Recognition-in-Soccer/blob/81e0e43bbb4e4442ec2360f0ba23272c7bdacfb7/images/PARHN.jpg" alt="PAHRN"
       
</p>

Four types of actions (i.e., Giving pass, Recieving pass, Shooting and (Goalkeeper) Diving)  with articulated pose Using Stacked Hourglass Network:

<p align="center">
    <img width="150" src="https://github.com/MehrnazFani/Action-Recognition-in-Soccer/blob/ba2d9632e1a907cbac9000a3ea11cb07290c881b/images/GivingPass-sideView.gif"/>
   <img width="150" src="https://github.com/MehrnazFani/Action-Recognition-in-Soccer/blob/ba2d9632e1a907cbac9000a3ea11cb07290c881b/images/GivingPass-backView.gif"/> 
  &nbsp; &nbsp; &nbsp; &nbsp;
  <img width="150" src="https://github.com/MehrnazFani/Action-Recognition-in-Soccer/blob/febbe9d928b1d16448a425d0bceacf54ed86c958/images/RecievePass_sideView.gif"/>
  <img width="150" src="https://github.com/MehrnazFani/Action-Recognition-in-Soccer/blob/febbe9d928b1d16448a425d0bceacf54ed86c958/images/RecievePass_backView.gif"/>
</p>
 <p align="center">  Giveing pass: a)Side view&nbsp; &nbsp; b)Back view&nbsp; &nbsp; &nbsp; &nbsp; Receiving pass: a)Side view&nbsp; &nbsp;b)Back view  </p>
 
 
<p align="center">
    <img width="150" src="https://github.com/MehrnazFani/Action-Recognition-in-Soccer/blob/77be9f3bbd07653f222d76780348cc8cab757c91/images/Shooting_frontView.gif"/>
   <img width="150" src="https://github.com/MehrnazFani/Action-Recognition-in-Soccer/blob/77be9f3bbd07653f222d76780348cc8cab757c91/images/Shooting-backView.gif"/> 
  &nbsp; &nbsp; &nbsp; &nbsp;
      <img width="150" src="https://github.com/MehrnazFani/Action-Recognition-in-Soccer/blob/77be9f3bbd07653f222d76780348cc8cab757c91/images/Diving-FrontView.gif"/>
   <img width="150" src="https://github.com/MehrnazFani/Action-Recognition-in-Soccer/blob/77be9f3bbd07653f222d76780348cc8cab757c91/images/Diving_sideView.gif"/> 
</p>
 <p align="center">  Shooting: a)Front view&nbsp; &nbsp; b)Back view &nbsp; &nbsp; &nbsp; &nbsp; Diving: a)Front view&nbsp; &nbsp;b)Side view
  </p>
  
# Dataset: Soccer action recognition 4 classes(SAR4)
SAR4 is a dataset generated for action recognition of individual soccer players from videos. It is composed of 1292 sequences of soccer videos with various lengths changing in the range of 5 to 59 frames per sequence. The SAR4 dataset is generated following the below steps:
+ The YouTube videos are collected for four action types in soccer, i.e., goal-keeper diving, player shooting, receiving pass and giving pass.  
+ The videos are trimmed by removing the extra frames from start and end of the sequences, which were not related to the action.
+ The target player is manually tracked in all frames of the sequence and his body-center is determined in each frame.
+ To increase number of video sequences in SAR4, data augmentation has been performed by: Scaling the frames, temporally changing lengths of sequences (by cutting few first/and last frames of the sequence, or by omitting odd/even frames of the sequence), rotating the frames with a random angle in the interval of $$[-10^O  10^O]$$




