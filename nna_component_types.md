[Home](readme.md) 🔶 [NNA Core Spec](nna_spec.md) 🔶 NNA Component Types 🔶 [Roadmap](roadmap.md)

# Component Types
Component type names are namespaced. Namespaces are separated with a `.` character.

## `nna`
Components in the `nna` namespace provide common functionality.

| Type | Description | Specification | Name | Json |
| --- | --- | --- | --- | --- |
| `nna.twist` | Twist bone constraint | [Link](Components/NNA/nna_twist.md) | Y | Y |
| `nna.humanoid` | Humanoid rig definition | [Link](Components/NNA/nna_humanoid.md) | Y | Y |
| `nna.material_mapping` | Map material resources on import by name | [Link](Components/NNA/nna_material_mapping.md) | N | Y |

## `ava`
AVA Components specify functionality for VR and V-Tubing avatars.

| Type | Description | Specification | Name | Json |
| --- | --- | --- | --- | --- |
| `ava.avatar` | Main avatar component | [Link](Components/AVA/ava_avatar.md) | N | Y |
| `ava.eyetracking_bone_limits` | Eye-bone rotation limits | [Link](Components/AVA/ava_eyetracking_bone_limits.md) | Y | Y |
| `ava.eyelidtracking_blendshape` | Eyelid blendshape mappings | [Link](Components/AVA/ava_eyelidtracking_blendshape.md) | N | Y |
| `ava.voice_visemes_blendshape` | Viseme blendshape mappings | <!--[Link](Components/AVA/ava_voice_visemes_blendshape.md)-->TODO  | N | Y |
| `ava.secondary_motion` | Basic bone physics | <!--[Link](Components/AVA/ava_secondary_motion.md)-->TODO  | N | Y |

## `vrc`
VRChat specific avatar components.

| Type | Description | Specification | Name | Json |
| --- | --- | --- | --- | --- |
| `vrc.avatar_colliders` | Collider definitions for the VRChat avatar descriptor. | <!--[Link](Components/VRC/vrc_avatar_colliders.md)-->TODO  | N | Y |
| `vrc.controller_mapping` | Map animator controllers from the Unity project. | <!--[Link](Components/VRC/vrc_controller_mapping.md)-->TODO  | N | Y |
| `vrc.physbone` | VRChat Physbone definition | <!--[Link](Components/VRC/vrc_physbone.md)-->TODO  | N | Y |
| `vrc.physbone_collider` | VRChat Physbone collider definition | <!--[Link](Components/VRC/vrc_physbone_collider.md)-->TODO  | N | Y |

## `vrm0`
VRM 0 specific avatar components.

| Type | Description | Specification | Name | Json |
| --- | --- | --- | --- | --- |
| `vrm0.spring_bone` | Spring bone definition | [Link](Components/VRM0/vrm0_spring_bone.md) | N | Y |
