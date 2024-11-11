[Home](../../readme.md) 🔶 [NNA Core Spec](../../nna_spec.md) 🔶 [NNA Component Types](../../nna_component_types.md) 🔶 [Roadmap](../../roadmap.md)

# `nna.material_mapping` - Map Materials On Import
Maps materials onto a mesh-instance on import into a game-engine by name.

## Json
| Key | Type | Description | Required | Default |
| --- | --- | --- | --- | --- |
| `slots` | list of strings | The index of a slot corresponds to the material index on the mesh-instance. | Y | - |

**Example**
```
{
	"t": "nna.material_mapping",
	"slots": [
		"Body_MainCharacter","Tshirt_Dirty"
	]
}
```
