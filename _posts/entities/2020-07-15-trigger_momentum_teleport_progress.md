---
title: trigger_momentum_teleport_progress
category: entity
tags:
 - trigger
 - map
 - track
 - teleport
---

----  
Trigger that teleports the player to their last touched `trigger_momentum_progress`.


## Keyvalues

>**Remote Destination** (target&lt;**target_destination**&gt;)  

Ignored for this trigger.

>**Local Destination Landmark** (landmark&lt;**target_destination**&gt;)  

When "Teleport mode" is "Landmark teleport", teleported entities are offset from the target by their initial offset from the landmark (this entity). 

>**Velocity Scale Factor (X Y Z)** (velocityscale&lt;**vector**&gt;)

Scale the player's velocity per-axis.
Default is "1 1 1".

>**Teleport mode** (mode&lt;**choices**&gt;)
  
Mode of teleportation.

 - **0**: Default (do nothing, just teleport)
 - **1**: Reset velocity
 - **2**: Keep negative Z (downwards) velocity
 - **3**: Redirect velocity to destination angles
 - **4**: Landmark teleport

Defaults to 1; reset velocity.

>**Reorient Landmark** (reorient_landmark&lt;**choices**&gt;) 
 - **0**: No
 - **1**: Yes

When "Teleport mode" is "Landmark teleport", this will reorient the origin, angles and velocity from the landmark's local space to the destination's.
This means the destination room does not have to face the same way.
Default is No; 0.

>**Reset the player angles on teleport** (resetang&lt;**choices**&gt;)
 - **0**: False
 - **1**: True

Resets the view angles of the player after being teleported to the Remote Destination. Default is True; 1.

>**Fail Teleport** (fail&lt;**choices**&gt;)
 - **0**: False
 - **1**: True

Indicates whether this teleport is for failing a level. 
Default is False; 0.

## Flags

>**Teleport the player on EndTouch() instead of StartTouch() (8388608)**  
Teleports the user to the Remote Destination when the player leaves the trigger instead of when they first touch it.
