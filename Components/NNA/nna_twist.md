[Home](../../readme.md) 🔶 [NNA Core Spec](../../nna_spec.md) 🔶 [NNA Component Types](../../nna_component_types.md) 🔶 [Roadmap](../../roadmap.md)

# `nna.twist`
Specifies a twist bone. If both `Source` and `Weight` are specified, they must be separated by `,`.

## Name
| Name Part | Type | Description | Required | Default |
| --- | --- | --- | --- | --- |
| $Twist | literal | processor name | Y | - |
| Source | string | Source node | N | grandparent of the twist node |
| Weight | float | Weight of the sourcee | N | `0.5` |

**Example**
`LowerArmTwistHand.L,0.66.L`

## Json
| Key | Type | Description | Required | Default |
| --- | --- | --- | --- | --- |
| `s` | string/path | Source node path | N | grandparent of the twist node |
| `w` | float | Weight of the source | N | `0.5` |

**Example**
``` json
{
	"t": "nna.twist",
	"w": 0.66,
	"s": "Handl.L"
}
```
