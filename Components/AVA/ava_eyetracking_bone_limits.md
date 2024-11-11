[Home](../../readme.md) 🔶 [NNA Core Spec](../../nna_spec.md) 🔶 [NNA Component Types](../../nna_component_types.md) 🔶 [Roadmap](../../roadmap.md)

# `ava.eyetracking_bone_limits`
Eye bone rotation limits.

## Name
Float values are separated by `,` character.

| Name Part | Type | Description | Required | Default |
| --- | --- | --- | --- | --- |
| EyeBoneLimits | literal | processor name | Y | - |
| `up` | float | Rotation limit in degrees | Y | - |
| `down` | float | Rotation limit in degrees | Y | - |
| `in` | float | Rotation limit in degrees | Y | - |
| `out` | float | Rotation limit in degrees | Y | - |
| `symmetry` | symmetry suffix | Specifies whether the left or right eye is targeted.<br>If omitted, values are applied to both eyes. | N | both |

**Example**
`EyeEyeBoneLimits15.0,12.0,15.0,16.0.L`

## Json
| Key | Type | Description | Required | Default |
| --- | --- | --- | --- | --- |
| `linked` | bool | Values symmetrical | N | `true` |
| `left_up` | float | Rotation limit in degrees | N | 15.0 |
| `left_down` | float | Rotation limit in degrees | N | 12.0 |
| `left_in` | float | Rotation limit in degrees | N | 15.0 |
| `left_out` | float | Rotation limit in degrees | N | 16.0 |
| `right_up` | float | Rotation limit in degrees | N | 15.0 |
| `right_down` | float | Rotation limit in degrees | N | 12.0 |
| `right_in` | float | Rotation limit in degrees | N | 15.0 |
| `right_out` | float | Rotation limit in degrees | N | 16.0 |

**Example**
```
{
	"t": "ava.eyetracking_bone_limits",
	"left_up": 15.0,
	"left_down": 12.0
}
```
