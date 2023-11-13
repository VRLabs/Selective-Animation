<div align="center">

# Selective Animation

[![Generic badge](https://img.shields.io/github/downloads/VRLabs/Selective-Animation/total?label=Downloads)](https://github.com/VRLabs/Selective-Animation/releases/latest)
[![Generic badge](https://img.shields.io/badge/License-MIT-informational.svg)](https://github.com/VRLabs/Selective-Animation/blob/main/LICENSE)
[![Generic badge](https://img.shields.io/badge/Unity-2019.4.31f1-lightblue.svg)](https://unity3d.com/unity/whats-new/2019.4.31)
[![Generic badge](https://img.shields.io/badge/SDK-AvatarSDK3-lightblue.svg)](https://vrchat.com/home/download)

[![Generic badge](https://img.shields.io/discord/706913824607043605?color=%237289da&label=DISCORD&logo=Discord&style=for-the-badge)](https://discord.vrlabs.dev/)
[![Generic badge](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Fshieldsio-patreon.vercel.app%2Fapi%3Fusername%3Dvrlabs%26type%3Dpatrons&style=for-the-badge)](https://patreon.vrlabs.dev/)

System for playing animations for only a single player in an instance

![SelectiveAnimation](https://github.com/VRLabs/Selective-Animation/assets/76777936/7c51b935-5937-42ef-b645-3781e64d38ef)

### ⬇️ [Download Latest Version](https://github.com/VRLabs/Selective-Animation/releases/latest)

<!-- 
### 📦 [Add to VRChat Creator Companion]() -->

</div>

---

## How it works

* The system is built using two [Raycasts](https://github.com/VRLabs/Raycast-Prefab).
* The two raycasts are slightly offset from each other, and one has a contact sender on it, while the other a contact receiver on it.
* When pointed at a player, both raycasts will collide with the player only on their screen, because the PlayerLocal collider only exists on their side. This means the Contact Sender and Receiver will only make contact for the player the system is pointing at.

## Install guide

https://github.com/VRLabs/Selective-Animation/assets/76777936/3dc5d6d8-8855-4bef-9398-62fd3522a69e


* If you dont already have [Final IK](https://assetstore.unity.com/packages/tools/animation/final-ik-14290) installed, download and install the [Final IK Stub](https://github.com/VRLabs/Final-IK-Stub).
  * Note: Testing in Unity is not possible when using the Final IK Stub!
* Drag & drop the ``Selective Animation`` prefab into the base of your Hierarchy.
* Right click and unpack the prefab, then drag & drop it onto your avatar.
* Expand the prefab hierarchy and find ``Selective Animation Target``
* Move ``Selective Animation Target`` outside of ``Selective Animation`` and place it anywhere in your avatars hierarchy as needed.
* Adjust the rotation so the laser points in the desired direction.
* The laser can be disabled or deleted.

## How to use

* Add the bool ``SelectiveAnimation/IsSelected`` to your FX controller.
* When the system is pointing at a player, the bool will be ``True`` only for the player it is pointing at.
* Use the bool as a transition condition to make animations visible to only the one player.

## Additional notes

* VRChat uses Final IK v1.9. If you are using a different version you may experience differences in behavior when testing with Final IK.

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
|  |-PlayerLocal Raycast Sender
|  |  |-LimbIK
|  |  |  |-Grounder
|  |  |  |  |-Offset
|  |  |  |  |  |-End
|  |-PlayerLocal Raycast Receiver
|  |  |-LimbIK
|  |  |  |-Grounder
|  |  |  |  |-Offset
|  |  |  |  |  |-End
|  |-Sender
|  |-Receiver
|  |-Laser
|-Selective Animation Target
```

## Contributors

* [hfcRed](https://hfcred.carrd.co/)
* [jellejurre](https://github.com/jellejurre)
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
