
# `nna.humanoid` - Humanoid Mappings
Generates a humanoid `Avatar`. Creates an `Animator` component on the root node if not present and sets the avatar.
Currently, only automatic mapping of bones is supported. Explicit mapping may be added in the future.

## Name
| Name Part | Type | Description | Required | Default |
| --- | --- | --- | --- | --- |
| Humanoid | literal | processor name | Y | - |
| Digi | literal | Indicate digitigrade locomotion. | N | `planti` |
| NoJaw | literal | Flag to not map the jaw. | N | `false` |

**Example**
`ArmatureHumanoidDigiNoJaw`

## Json
| Key | Type | Description | Required | Default |
| --- | --- | --- | --- | --- |
| `lt` | string | Locomotion type. Supported values are `planti` & `digi`. | N | `planti` |
| `nj` | boolean | Option to not map the jaw. Supported values are `nj` & `no_jaw`. | N | `false` |

**Example**
```
{
	"t": "humanoid",
	"lt": "digi",
	"nj": true
}
```
