# modSim
Simulation for modular robots in Ignition Citadel, currently the spider-robot ROMERIN developed at UPM ETSIDI, gazebo simulation [here](https://github.com/aslab/rmsim).

The main objective of this package is to create an Ignition plugin to allow robot reconfiguration and self-assembly. As the control is made with ROS2 Foxy, it shall communicate with its interfaces through diagnostics messages to inform about the status of the link, if a link is feasible, if it requires to approach the modules, etc.

## Objective

The main objective of this work is to provide tools to test architectural changes at run-time to demonstrate reconfigurability and adaptation. Such adaptation at the moment is based on the structural components of the robots: legs, sensors, etc. but other components such as software strategies will be evaluated as well.

## Current status [19/05/21] 

Plugin created: __AttachableJoint.cc__
-	Creation/destruction of a certain link in a model
Creation/destruction of a link between two different models trough a string topic with the structure: **[parentModel]** **[ParentLink]** **[ChildModel]** **[ChildLink]** -DONE-
-	Coupling components: attachable joints to only allow the links between attachable components within a certain distance or in contact -IN PROGRESS-
- ROS2 topic to diagnose the link status and if the attach action has been successful -IN PROGRESS-
