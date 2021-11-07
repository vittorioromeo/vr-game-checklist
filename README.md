# vr-game-checklist

## Introduction

So, you're making a Virtual Reality game -- that's great! This checklist will help you and your team deliver the best possible experience for your users. Just as it is a sin to release a non-VR FPS game without a FoV slider or mouse sensitivity options, there are many settings and options that any VR game should have.

The checklist below will make sure you don't miss any. The items are ordered from the most important to the least important. Not all items are applicable to every game, so please use your common sense.

*(Note: I am not saying that every single checkbox should be ticked, but rather you should at least go though and evaluate all of them.)*

## Checklist

### Locomotion Options

#### Teleportation

- [ ] My game offers a teleportation locomotion mode.

- Players can choose between different teleportation visual effects to reduce motion sickness:

    - [ ] Instant teleportation.

    - [ ] Fade-to-black and fade-from-black teleportation.

    - [ ] Smooth teleportation (the in-game character very quickly dashes from location A to location B).

- [ ] Optionally, players can choose the direction they will face after teleporting by using the thumbstick (a-la Robo Recall). [^robo_recall_teleportation]

[^robo_recall_teleportation]: If you are not familiar with Robo Recall teleporation, [this video](https://youtu.be/gBZcN2NPLb8?t=188) shows exactly how it works. Note that this behavior should be optional, as some people might feel disoriented when the direction is changed after teleportation, and it might be easy to accidentally turn the thumbstick in the wrong direction during teleportation.

#### Smooth Locomotion

- [ ] My game offers a smooth locomotion mode.

- [ ] Players can tweak the movement speed multiplier in the options.

- If my game has a sprint mechanic, players can choose how to activate it between the following modes:
  
  - [ ] By quickly tapping the same direction twice on the thumbstick. [^double_tap_sprint]

  [^double_tap_sprint]: Double-tap sprinting is especially important for Valve Index controller owners, as it has been widely reported that keeping the thumbstick pressed down can lead to thumbstick drift.

  - [ ] By keeping the thumbstick pressed.

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

- [ ] My game allows controller-based turning to be completely disabled for players desiring a more immersive room-scale experience and to avoid accidental thumbstick presses.

### Crouching

- [ ] My game allows players to physically crouch in real life, adjusting the in-game hitbox and movement speed accordingly.

- [ ] My game allows players to toggle crouching by pressing an arbitrary button (chosen by players).

- [ ] My game allows players to tweak their character's posture (from standing up to crouching) by using a thumbstick.

### Controller Angle Adjustments

- [ ] My game allows players to finely tweak the in-game pitch of held objects and weapons. [^controller_pitch_adjustment]

[^controller_pitch_adjustment]: This is massively important to guarantee that a weapon will point in the exact direction player expect it to, and to ensure consistent aiming between games. Some games, for example "Stride", aim the weapon too low (towards the ground) when using Valve Index controllers compared to Oculus Rift controllers. Providing an adjustable pitch allows players to decide where they want their weapon to aim.

- [ ] My game allows players to finely tweak the in-game yaw and roll of held objects and weapons. [^controller_yaw_roll_adjustment]

[^controller_yaw_roll_adjustment]: This issue is less common than the pitch one, but some games have incorrect yaw/roll rotation of a held weapon in respect to the controller. "Crisis VRigade 2", for example, points the weapon a few extra degrees towards the left with Valve Index controllers, forcing players to uncomfortably aim in the wrong direction to hit the target. Providing an adjustable yaw/roll allows players to decide where they want their weapon to aim.

### Height Adjustment

- [ ] My game allows players to calibrate their character's height to their real-life height.

    - [ ] The automatically chosen height can be manually tweaked by the player in the options.

### World Scale Adjustment

- [ ] My game allows players to scale the game world by an arbitrary factor in the options. [^why_world_scale]

[^why_world_scale]: People come in all sizes and shapes. As a developer, you design the scale of the world to suit your size and shape. Your players might be "giants" compared to you, or "tiny" compared to you. If you are worried about the balance of the game or worried about unfair advantages, use common sense. If the game is single-player, then it doesn't really matter -- the goal is for players to have fun and feel comfortable. If the game is multi-player, either limit the scaling factor to a narrow range, or do not introduce it at all.

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

## Contributing

Is something missing from the checklist? Create an [issue](https://github.com/SuperV1234/vr-game-checklist/issues) to discuss it, or directly contribute something new by opening a [pull request](https://github.com/SuperV1234/vr-game-checklist/pulls).

## Self-Promotion

Check out [Quake VR](https://www.youtube.com/watch?v=MBoI16z8Nxg) my PCVR mod for Quake that turns it into a first-class VR experience!
