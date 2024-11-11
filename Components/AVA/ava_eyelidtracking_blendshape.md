[Home](../../readme.md) 🔶 [NNA Core Spec](../../nna_spec.md) 🔶 [NNA Component Types](../../nna_component_types.md) 🔶 [Roadmap](../../roadmap.md)

# `ava.eyelidtracking_blendshape`
Eyelid Blendshape Mappings

## Json
| Key | Type | Description | Required | Default |
| --- | --- | --- | --- | --- |
| `meshinstance` | string/node-path | Target mesh instance | N | Automatically determined |
| `eye_closed` | string | Blendshape Name | N | Automapped |
| `eye_closed_left` | string | Blendshape Name | N | Automapped |
| `eye_closed_right` | string | Blendshape Name | N | Automapped |
| `look_up` | string | Blendshape Name | N | Automapped |
| `look_down` | string | Blendshape Name | N | Automapped |

**Example**
```
{
	"t": "ava.eyelidtracking_blendshape",
	"meshinstance": "Body",
	"eye_closed": "ft_close_eyes",
	"eye_closed_left": "ft_close_eyes_left",
	"eye_closed_right": "ft_close_eyes_right",
	"look_up": "ft_eyes_up",
	"look_down": "ft_eyes_down"
}
```
