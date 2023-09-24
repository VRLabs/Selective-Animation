<div align="center">

# Selective Animation

[![Generic badge](https://img.shields.io/github/downloads/VRLabs/Selective-Animation/total?label=Downloads)](https://github.com/VRLabs/Selective-Animation/releases/latest)
[![Generic badge](https://img.shields.io/badge/License-MIT-informational.svg)](https://github.com/VRLabs/Selective-Animation/blob/main/LICENSE)
[![Generic badge](https://img.shields.io/badge/Unity-2019.4.31f1-lightblue.svg)](https://unity3d.com/unity/whats-new/2019.4.31)
[![Generic badge](https://img.shields.io/badge/SDK-AvatarSDK3-lightblue.svg)](https://vrchat.com/home/download)

[![Generic badge](https://img.shields.io/discord/706913824607043605?color=%237289da&label=DISCORD&logo=Discord&style=for-the-badge)](https://discord.vrlabs.dev/)
[![Generic badge](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Fshieldsio-patreon.vercel.app%2Fapi%3Fusername%3Dvrlabs%26type%3Dpatrons&style=for-the-badge)](https://patreon.vrlabs.dev/)

System for playing animations for only a single player in an instance.

![Alt text]()

### ⬇️ [Download latest Unitypackage](https://github.com/VRLabs/Selective-Animation/releases/latest)

<!-- 
### 📦 [Add to VRChat Creator Companion]() -->

</div>

---

## How it works

* The system is built using two [raycasts](https://github.com/VRLabs/Raycast-Prefab).
* The first raycast collides with the world, remote players and the local player and has a Contact Sender attached to it. The second raycast collides only with the local player and has a Contact Receiver attached to it.
* When pointed at a player, both raycasts will collide with the player only on their screen, because the PlayerLocal collider only exists on their side. This means the Contact Sender and Receiver will only make contact for the player the system is pointing at.

## Install guide

* If you dont already have FinalIK installed, download and install the [FinalIK Stub](https://github.com/VRLabs/Final-IK-Stub).
  * Note: Testing in Unity is not possible when using the FinalIK Stub!
* Drag & drop the ``Selective Animation`` prefab into the base of your Hierarchy.
* Right click and unpack the prefab, then drag & drop it onto your avatar.
* Expand the prefab and locate ``Selective Animation Target``. Move this object to anywhere on your avatar and adjust the rotation so the arrow points in the desired direction.
* The arrow can be disabled or deleted.

## How to use

* Add the bool ``SelectiveAnimation/IsSelected`` to your FX controller.
* When the system is pointing at a player, the bool will be ``True`` only for the player it is pointing at.
* Use the bool as a transition condition to make animations visible to only the one player.

## Performance stats

```c++
Constraints:        3
Contact Receivers:  1
Contact Senders:    1
```

## Hierarchy layout

```html
Selective Animation
|-Raycast Container
|  |-World Raycast
|  |  |-LimbIK
|  |  |  |-Grounder
|  |  |  |  |-Offset
|  |  |  |  |  |-End
|  |-Player Raycast
|  |  |-LimbIK
|  |  |  |-Grounder
|  |  |  |  |-Offset
|  |  |  |  |  |-End
|  |-Sender
|  |  |-Sphere
|  |-Receiver
|  |-Forward
|-Selective Animation Target
```

## Contributors

* Wakam

## License

Selective Animation is available as-is under MIT. For more information see [LICENSE](https://github.com/VRLabs/Selective-Animation/blob/main/LICENSE)

​

<div align="center">

[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/VRLabs.png" width="50" height="50">](https://vrlabs.dev "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Discord.png" width="50" height="50">](https://discord.vrlabs.dev/ "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Patreon.png" width="50" height="50">](https://patreon.vrlabs.dev/ "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Twitter.png" width="50" height="50">](https://twitter.com/vrlabsdev "VRLabs")

</div>

---
