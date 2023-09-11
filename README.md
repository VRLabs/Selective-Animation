# Exclusive Animation

[![Generic badge](https://img.shields.io/badge/Unity-2019.4.31f1-informational.svg)](https://unity3d.com/unity/whats-new/2019.4.31)
[![Generic badge](https://img.shields.io/badge/SDK-AvatarSDK3-informational.svg)](https://vrchat.com/home/download)
[![Generic badge](https://img.shields.io/badge/License-MIT-informational.svg)](https://github.com/VRLabs/Exclusive-Animation/blob/main/LICENSE)
[![Generic badge](https://img.shields.io/github/downloads/VRLabs/Exclusive-Animation/total?label=Downloads)](https://github.com/VRLabs/Exclusive-Animation/releases/latest)

System for playing animations for only a single player in an instance.

## How it works

The system is built using two [raycasts](https://github.com/VRLabs/Raycast-Prefab).

The first raycast collides with the world, remote players and the local player and has a Contact Sender attached to it. The second raycast collides only with the local player and has a Contact Receiver attached to it.

When pointed at a player, both raycasts will collide with the player only on their screen, because the PlayerLocal collider only exists on their side. This means the Contact Sender and Receiver will only make contact for the player the system is pointing at.

## Install guide

If you dont already have FinalIK installed, download and install the [FinalIK Stub](https://github.com/VRLabs/Final-IK-Stub).

**Note: Testing in Unity is not possible when using the FinalIK Stub!**

Merge the FX controller to your own FX controller using the [Avatar 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) tool.

Put ``Exclusive Animation.prefab`` at the base of your Unity scene, which will give it base Unity scaling.

Unpack the prefab by right clicking it and move the prefab onto the base of your avatar.

Expand the prefab and locate ``Exclusive Animation Target``. Move this object to anywhere on your avatar and adjust the rotation so the arrow points in the desired direction.

The arrow can be disabled or deleted.

## How to use

Add the bool ``ExclusiveAnimation/Ready`` to your FX controller.

When the system is pointing at a player, the bool will be ``True`` only for the player it is pointing at.

Use the bool as a transition condition to make animations visible to only the one player.

## Credit

Wakam

## Downloads

You can grab the latest version of the Exclusive Animation in [Releases](https://github.com/VRLabs/Exclusive-Animation/releases/latest).

## License

Exclusive Animation is available as-is under MIT. For more information see [LICENSE](https://github.com/VRLabs/Exclusive-Animation/blob/main/LICENSE)

## Contact us

If you need any help, our support channel is on [Discord](https://discord.vrlabs.dev/)
