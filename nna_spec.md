[Home](readme.md) 🔶 NNA Core Spec 🔶 [NNA Component Types](nna_component_types.md) 🔶 [Roadmap](roadmap.md)

# NNA Specification (v0.0.x)
NNA is a system to store data in a 3d models hierarchy.

For simpler definitions, information can be encoded into a node name directly.\
For more complex components, you can serialize JSON into an array of child-nodes. The Blender extension will help you work with that.

A file with NNA definitions must have `.nna` in its name before its file format suffix.\
An FBX file with NNA definitions would be named for example `Superawesomemodel.nna.fbx`.

On import into a game-engine with an NNA implementation, these definitions will be parsed into the game-engines own constructs.

[Find a list of all available component types here.](nna_component_types.md)

## Name Definitions
Name definitions must fit inside a single node-name.
Their format is different for each definition but follows the following general syntax:

**Syntax:** `Actual Node Name` `NNA Processor Name` `Optional Parameters` `Optional Symmetry Suffix`

*Example:* `UpperLegTwistHips0.5.R`

`UpperLeg` is the actual node name.
`Twist` is the NNA type name.
`Hips` is a parameter for the definition.
`0.5` is a parameter for the definition.
`.R` signifies the right side of the model.

## Json Definitions
Json definitions are of arbitrary length, as they are spread over multiple nodes.\
They are an array of objects, all of which must have a `t` property. It specifies the 'type' of the component, based upon which it will be processed.

As node-names can be only 63 bytes long in Blender, the Json array gets split into 'lines'. That's an array of nodes. The lines must start with `$`, a line-number, and another `$`. A line does contain raw Json text and does not have to parse into valid Json, only the total combined string.

Since many tools, including Blender, require for node-names to be unique, the line-number can have an optional 'salt'. Before the second `$` add a `.` followed by a number, making the node-name unique.

In order to not clutter the main model's hierarchy with Json 'lines', they can be contained in a 'targeting-node' which is parented to a node named `$nna`, which should be parented to the root. The targeting-node's name must start with `$target:` followed by the unique name of the targeted node. The root of the hierarchy can be targeted with `$root`.

*Example*:\
`$nna`\
→ `$target:Hair01`\
→ → `$0$[{"t":"ava.secondary_motion","id":"0","intensity":0.4},{"t`\
→ → `$1$":"vrc.physbone", "overrides":["0"],"pull":0.15,"spring":0`\
→ → `$2$.3,"limit_type":"angle","max_angle":60}]`

Json components can have optional `id` and `overrides` properties.\
An `id` is a string that must be unique within the model, and can be used to reference other components.\
`overrides` is an array of ID's. The overridden components will not be processed.

On import into a game-engine NNA Json definitions will be removed from the hierarchy by default.\
