[Home](../../readme.md) 🔶 [NNA Core Spec](../../nna_spec.md) 🔶 [NNA Component Types](../../nna_component_types.md) 🔶 [Roadmap](../../roadmap.md)

# `vrc.controller_mapping`
Voice viseme blendshape mappings.
This component is optional, the blendshapes will be automapped if the model conforms to blendshape naming conventions.

**Manual mapping not yet implemented.**

## Json
| Key | Type | Description | Required | Default |
| --- | --- | --- | --- | --- |
| `base` | string | VRChat Base Animation Layer Mapping | N | - |
| `additive` | string | VRChat Additive Animation Layer Mapping | N | - |
| `gesture` | string | VRChat Gesture Animation Layer Mapping | N | - |
| `action` | string | VRChat Action Animation Layer Mapping | N | - |
| `FX` | string | VRChat FX Animation Layer Mapping | N | - |
| `sitting` | string | VRChat Sitting Special Animation Layer Mapping | N | - |
| `tpose` | string | VRChat TPose Special Animation Layer Mapping | N | - |
| `ikpose` | string | VRChat IKPose Special Animation Layer Mapping | N | - |
| `parameters` | string | VRChat Expression Parameters Mapping | N | - |
| `menu` | string | VRChat Expression Menu Mapping | N | - |

**Example**
```
{
	"t": "vrc.controller_mapping",
	"gesture": "SuperawesomeAvatar_Gesture",
	"fx": "SuperawesomeAvatar_FX",
	"parameters": "SuperawesomeAvatar_Parameters",
	"menu": "SuperawesomeAvatar_Menu",
}
```
