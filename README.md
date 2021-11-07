# vr-game-checklist



## Introduction

So, you're making a Virtual Reality game -- that's great! This checklist will help you and your team deliver the best possible experience for your users. Just as it is a *sin* to release a non-VR FPS game without a FoV slider or mouse sensitivity options, there are many settings and options that most VR games should have.

The checklist below will make sure you don't miss any. The items are ordered from the most important to the least important. Not all items are applicable to every game, so please use your common sense.

*(Note: I am not saying that every single checkbox should be ticked, but you should at least evaluate all of them.)*



## Checklist

### Locomotion Options

#### Smooth Locomotion

- [ ] My game offers a smooth locomotion mode.

- [ ] Players can choose between head-based or controller-based movement. [^controller_head_based]

[^controller_head_based]: Some games also offer "hybrid" options where the movement vector is derived from an average between the head and the controller. Other games also can figure out the movement direction via additional hardware such as hip trackers or [DecaMove](https://www.deca.net/decamove/).

- [ ] Players can tweak the movement speed multiplier in the options.

- If my game has a sprint mechanic, players can choose how to activate it between the following modes:
  
  - [ ] By quickly tapping the same direction twice on the thumbstick. [^double_tap_sprint]

  [^double_tap_sprint]: Double-tap sprinting is especially important for Valve Index controller owners, as it has been widely reported that keeping the thumbstick pressed down can lead to thumbstick drift.

  - [ ] By keeping the thumbstick pressed.

  - [ ] By pressing the thumbstick once, then releasing it. (Sprinting will continue until the player stops moving.)

  - [ ] By keeping an arbitrary button (chosen by players) pressed.

  - [ ] By arm-swinging or putting the arms down to the sides.

- [ ] Players can fine-tune their in-game movement speed by controlling how far they push the thumbstick in one direction.

- My game offers different smooth locomotion visual effects to reduce motion sickness:

    - [ ] Artificially decrease FoV to a user-specified amount.
  
### Turning Options
  
#### Snap Turning

- [ ] My game offers snap turning.

- [ ] Players can tweak the angle of snap turning in the options.

    - [ ] I set no arbitrary restriction on the angle -- it can be fine-tuned to any value players desires.

- [ ] Players can choose between immediate turning or a very fast smooth transition between angles.

#### Smooth Turning

- [ ] My game offers smooth turning.

- [ ] Players can tweak the speed of smooth turning in the options.

    - [ ] I set no arbitrary restriction on the speed -- it can be fine-tuned to any value players desires.

- [ ] Players can fine-tune their in-game turning speed by controlling how far they push the thumbstick in one direction.

#### No Turning

- [ ] My game allows controller-based turning to be completely disabled for players desiring a more immersive room-scale experience and to prevent accidental thumbstick inputs.

#### Left-Handed Support

- [ ] My game allows switching the role of the left and right thumbsticks to support left-handed players.

#### Teleportation

- [ ] My game offers a teleportation locomotion mode. [^teleportation_bad]

[^teleportation_bad]: If you think that teleportation is an outdated locomotion technique or that it doesn't suit your game, please [read my comment regarding that on Reddit](https://old.reddit.com/r/virtualreality/comments/qothkl/i_made_a_checklist_of_features_that_vr_developers/hjpev21/).

- Players can choose between different teleportation visual effects to reduce motion sickness:

    - [ ] Instant teleportation.

    - [ ] Fade-to-black and fade-from-black teleportation.

    - [ ] Smooth teleportation (the in-game character very quickly dashes from location A to location B).

- [ ] Optionally, players can choose the direction they will face after teleporting by using the thumbstick (a-la Robo Recall). [^robo_recall_teleportation]

- [ ] Enabling teleportation is not mutually exclusive with enabling smooth locomotion. [^both_teleport_and_smooth_locomotion]

[^both_teleport_and_smooth_locomotion]: Some players who are in the process of getting their "VR legs" prefer moving large distances via teleportation, yet still having the ability to fine-tune their position and react more quickly to in-game events by (sparingly) using smooth locomotion. Allowing both locomotion to coexist is helpful for these players.

[^robo_recall_teleportation]: If you are not familiar with Robo Recall teleporation, [this video](https://youtu.be/gBZcN2NPLb8?t=188) shows exactly how it works. Note that this behavior should be optional, as some people might feel disoriented when the direction is changed after teleportation, and it might be easy to accidentally turn the thumbstick in the wrong direction during teleportation.

### Crouching

- [ ] My game allows players to physically crouch in real life, adjusting the in-game hitbox and movement speed accordingly.

- [ ] My game allows players to toggle crouching by pressing an arbitrary button (chosen by players).

- [ ] My game allows players to tweak their character's posture (from standing up to crouching) by using a thumbstick.

### Controller Angle Adjustments

- [ ] My game allows players to finely tweak the in-game pitch of held objects and weapons. [^controller_pitch_adjustment]

[^controller_pitch_adjustment]: This is massively important to guarantee that a weapon will point in the exact direction player expect it to, and to ensure consistent aiming between games. Some games, for example "Stride", aim the weapon too low (towards the ground) when using Valve Index controllers compared to Oculus Rift controllers. Providing an adjustable pitch allows players to decide where they want their weapon to aim. 

    Frankly, this should be something supported by the runtime (e.g. SteamVR). However, [they do not seem to care](https://github.com/ValveSoftware/openvr/issues/1262).

- [ ] My game allows players to finely tweak the in-game yaw and roll of held objects and weapons. [^controller_yaw_roll_adjustment]

[^controller_yaw_roll_adjustment]: This issue is less common than the pitch one, but some games have incorrect yaw/roll rotation of a held weapon in respect to the controller. "Crisis VRigade 2", for example, points the weapon a few extra degrees towards the left with Valve Index controllers, forcing players to uncomfortably aim in the wrong direction to hit the target. Providing an adjustable yaw/roll allows players to decide where they want their weapon to aim.

### Height Adjustment

- [ ] My game allows players to calibrate their character's height to their real-life height.

    - [ ] The automatically chosen height can be manually tweaked by the player in the options.

### World Scale Adjustment

- [ ] My game allows players to scale the game world by an arbitrary factor in the options. [^why_world_scale]

[^why_world_scale]: People come in all sizes and shapes. As a developer, you design the scale of the world to suit your size and shape. Your players might be "giants" compared to you, or "tiny" compared to you. If you are worried about the balance of the game or worried about unfair advantages, use common sense. If the game is single-player, then it doesn't really matter -- the goal is for players to have fun and feel comfortable. If the game is multi-player, either limit the scaling factor to a narrow range, or do not introduce it at all.

    A reasonable way of implementing world scale is by simply scaling the player and related values, rather than scaling the world.

### Player Profile Management

- [ ] My game allows different players to store their settings and tweaks in profiles.

    - [ ] Profiles can be changed on the fly to make it easier for multiple people to swap in and out of gameplay.

    - [ ] There is no limit to how many profiles can be saved and loaded.

### Controller Offset Adjustments

- [ ] My game allows players to specify arbitrary X, Y, and Z offsets for the controller positions. [^controller_offset_adjustment]

[^controller_offset_adjustment]: This issue is way less common than controller angle issues, but it still possible to encounter it with games that were tested on only a specific set of controllers. Sometimes the in-game hands' positions do not match the controller positions in the real world. Rather than hardcoding offsets for each possible VR setup in existence, let players specify them in the options.

### Weapon Handling

- [ ] My game allows players to hold/use/drop weapons with any hand. [^any_hand_weapon_handling]

[^any_hand_weapon_handling]: Some games, such as "Half-Life: Alyx", arbitrarily decide to glue a weapon to one of the player's hands, preventing them from performing many interesting and immersive actions (e.g. dual-wielding, temporarily holding the weapon with the non-dominant hand, corner-peeking from the non-dominant hand side, temporarily dropping the weapon to do something else, throwing the weapon as a last resort or as a stylish move, etc.). While an option to glue a weapon to the player's hand might be a good idea as an accessibility option, it should not be the default.

    If your game doesn't support dropping weapons, it is still a good idea to let players hold them and de-spawn them (or automatically return them to holsters/inventory) when they are not being held. Examples of games doing this are "Until You Fall" and "Resident Evil 4 VR". 
    
- [ ] For accessibility reasons, my game allows to keep holding a weapon even if the controller is not being held (e.g. not pressing the side button on Oculus controllers or not physically grabbing the Valve Index controller).

- If my game ends up with a system where the current weapon is glued to the player's hand: 
    
    - [ ] Left-handed players will be able to switch the default hand.

### Performance

- [ ] My game reuses the right/left eye render for the PC monitor instead of rendering a third time.

### UI 

- [ ] UI elements in my game are drawn at an appropriate distance, in order to be in focus. [^ui_focus_distance]

[^ui_focus_distance]: Different HMDs have different in-game distances from the player camera at which the image will appear in focus. Your UI should be drawn at those distances to ensure readability.



## Extras and Nice-To-Haves

### Computer Interaction

- [ ] My game allows settings to be configured on the computer via mouse/keyboard on the fly, while the game is running.

- [ ] Spectators can interact on the computer while players are in VR, for example by changing or restarting levels, or tweaking options.



## Contributing

Is something missing from the checklist? Create an [issue](https://github.com/SuperV1234/vr-game-checklist/issues) to discuss it, or directly contribute something new by opening a [pull request](https://github.com/SuperV1234/vr-game-checklist/pulls).



## Self-Promotion

Check out [**Quake VR**](https://www.youtube.com/watch?v=MBoI16z8Nxg), my free and open-source Quake mod that turns the 1996 classic into a first-class PCVR experience!

<p align="center">
  <a href="https://www.youtube.com/watch?v=MBoI16z8Nxg"><img src="https://img.youtube.com/vi/MBoI16z8Nxg/0.jpg"></img></a>
</p>
