# Skill Tree Power Data

Skillful makes some additions to apoli powers. This is done in the `skill` field.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`background` | [Identifier](data_types/identifier.md) | _optional_ | The ID of the texture that will be the background of the skill tree.
`power` | [Identifier](data_types/identifier.md) | _optional_ | IDs of the power this tree will grant.
`powers` | [Array](data_types/array.md) of [Identifiers](data_types/identifier.md) | _optional_ | IDs of the powers this tree will grant.
`default_powers` | [Array](data_types/array.md) of [Identifiers](data_types/identifier.md) | _optional_ | IDs of the powers this tree will grant when the player joins the game. Will not be read if a `parent` exists.
`icon` | [Identifier](data_types/identifier.md) | _optional_ | The item which is displayed as the icon for the skill widget.
`cost` | [Integer](data_types/integer.md) | _optional_ | The amount of points that the player needs in order to purchase this skill.
`parent` | [Identifier](data_types/identifier.md) | _optional_ | The skill identifier that will be the parent of this widget.

### Example

```json
{
	"icon": "minecraft:stick",
	"name": "Parkour Skills",
	"description": "A skill tree that lets you earn parkour skills",
	"power": "example_pack:gain_points",
	"default_powers": [
		"example_pack:gain_points"
	],
	"cost": 0
}

```
This example skill will grant the `example_pack:gain_points` power to players on join. This is a root of a skill tree.
