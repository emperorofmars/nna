[Home](readme.md) 🔶 [NNA Core Spec](nna_spec.md) 🔶 [NNA Component Types](nna_component_types.md) 🔶 Roadmap

## NNA Roadmap

### Current Status
The structure is pretty much there, and specific functionality is being worked on.

### Stage 1: MVP
Parse decently featured VR avatars from `*.nna.fbx` files in Unity. Some resources like animator controllers or materials will be mapped by name from the Unity project.

Have a decent Blender extension to create NNA definitions with a GUI.

The 'export from Blender, drag into Unity, and get a ready to upload VR avatar' experience is generally there, but the file depends on resources in the Unity project.

#### TODO
* NNA Format:
	* More VR & V-tubing avatar components & features.
		* Bone based eyelid animation.
		* Bone physics libraries, at least partially implemented: VRC Physbones & VRM Springbones.
* Blender:
	* Handle name definition removal with an existing targeting node.

### Stage 2: All In One
An `*.nna.fbx` file no longer needs external dependencies, other than NNA itself, in order to be parsed into a fully featured VR avatar in a game-engine.

A lot of these features are blocked by Blender's (lack of an) animation system. Will be fixed once Blender 4.4 is released with 'slotted actions'.

#### TODO
* NNA Format:
	* More constraint types.
	* Unity humanoid muscle settings.
	* Animations, including being able to target NNA properties. (Blocked until Blender 4.4)
	* Implement [MTF](https://github.com/emperorofmars/stf-unity/tree/master/MTF) to fully encode shader & game engine agnostic materials.
* More VR & V-tubing avatar components & features.
	* Bone physics (ava.secondary_motion as universal fallback, VRC Physbones & colliders & contacts, VRM spring bones & colliders, maybe DynamicBones & MagickaCloth)
	* Automatic animator controller generation (Partially blocked until Blender 4.4)
		* Face Tracking
		* Hand gestures (additionally: fallback VRM blendshape pose nonsense)
		* Toggles
		* Joystick puppets
		* Custom application & game engine agnostic animation logic
* A fully featured Blender extension.

### Stage 3: Overlord
Go beyond what VR & V-Tubing applications support out of the box.

#### TODO
* Template system. (To apply user modifications. This would be the basis of a 'character editor' system, so end users could adapt their avatars easier.)
	* Gesture rebinding!
* Asset-Addon system. (To apply a piece of clothing from a separate file to a base body for example. This should be deeply integrated with the avatar components and the template system.)
* IDK, suggest me more!
