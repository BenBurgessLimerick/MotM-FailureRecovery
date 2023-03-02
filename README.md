# Enabling Failure Recovery for *On-The-Move* Mobile Manipulation

In [our previous work](https://benburgesslimerick.github.io/ManipulationOnTheMove/) we developed an architecture for enabling mobile manipulators to perform tasks such as grasping and placing without ever coming to a stop. Performing tasks on-the-move introduces new challenges when something goes wrong. For example, if a grasp fails and more time is required for the robot to complete the task, the base should be controlled to keep the object within reach instead of driving off to the drop point without collecting the object. 

In this work we explore a reactive base control system that enables graceful recovery from unexpected delays during manipulation on-the-move tasks. The system continuously evaluates candidate base poses near the target and chooses a goal based on the current state of the robot, location of the immediate target, as well as the next target in a multi-step task. 

![Pick-and-Place Task with 6s Artificial Grasp Failure Delay](gifs/ObstructedTurn_Ours_6s.gif)