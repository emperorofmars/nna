[Home](../../readme.md) 🔶 [NNA Core Spec](../../nna_spec.md) 🔶 [NNA Component Types](../../nna_component_types.md) 🔶 [Roadmap](../../roadmap.md)

# `ava.secondary_motion`
Specifies the root of a bone chain to be animated based on runtime physics.

**This component is incredibly rudimentary as of now and will be significantly reworked.**

This is supposed to be used as a universally compatible fallback component to specify bone physics.\
Components specific to target applications should be implemented, which can override this one.

## Name
| Name Part | Type | Description | Required | Default |
| --- | --- | --- | --- | --- |
| SecMo | literal | processor name | Y | - |
| `intensity` | float | Intensity | N | `0.3` |

**Example**
`Hair01SecMo0.36`

## Json
| Key | Type | Description | Required | Default |
| --- | --- | --- | --- | --- |
| `intensity` | float | Intensity | N | `0.3` |

**Example**
``` json
{
	"t": "ava.secondary_motion",
	"intensity": 0.36
}
```
