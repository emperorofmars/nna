[Home](../../readme.md) 🔶 [NNA Core Spec](../../nna_spec.md) 🔶 [NNA Component Types](../../nna_component_types.md) 🔶 [Roadmap](../../roadmap.md)

# `ava.voice_visemes_blendshape`
Voice viseme blendshape mappings.
This component is optional, the blendshapes will be automapped if the model conforms to blendshape naming conventions.

**Manual mapping not yet implemented.**

## Json
| Key | Type | Description | Required | Default |
| --- | --- | --- | --- | --- |
| `meshinstance` | string/node-path | Target mesh instance | N | Automatically determined |

**Example**
```
{
	"t": "ava.voice_visemes_blendshape",
	"meshinstance": "ArmatureHumanoidDigiNoJaw&Body"
}
```
