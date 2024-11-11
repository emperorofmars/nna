
# `nna.twist` - Twist Constraint
Creates a `RotationConstraint` component with one source limited to the Y axis.

## Name
| Name Part | Type | Description | Required | Default |
| --- | --- | --- | --- | --- |
| Twist | literal | processor name | Y | - |
| Source | string | Source node | N | grandparent of the twist node |
| Weight | float | Weight of the sourcee | N | `0.5` |

**Example**
`LowerArmTwistHand.L0.66.L`

## Json
| Key | Type | Description | Required | Default |
| --- | --- | --- | --- | --- |
| `s` | string/path | Source node path | N | grandparent of the twist node |
| `w` | float | Weight of the source | N | `0.5` |

**Example**
```
{
	"t": "c-twist",
	"w": 0.66,
	"s": "Handl.L"
}
```
