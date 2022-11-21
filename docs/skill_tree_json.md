# Skill Tree JSON Format

This is the format of a JSON file describing a skill. They need to be placed inside the `skill_trees` folder within your namespace. `default_powers` are used to create a way to earn points on your skill tree that you can implement yourself.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`name` | [Text](data_types/text_component.md) | | The display name of the skill widget.
`description` | [Text](data_types/text_component.md) | | The description of the skill widget.
`icon` | [Item Stack](data_types/item_stack.md) | {"item": "minecraft:grass_block"} | The item which is displayed as the icon for the skill widget.
`power` | [Identifier](data_types/identifier.md) | _optional_ | IDs of the power this skill will grant.
`powers` | [Array](data_types/array.md) of [Identifiers](data_types/identifier.md) | _optional_ | IDs of the powers this skill will grant.
`parent` | [Identifier](data_types/identifier.md) | _optional_ | The skill identifier that will be the parent of this widget.
`default_powers` | [Array](data_types/array.md) of [Identifiers](data_types/identifier.md) | _optional_ | IDs of the powers this tree will grant when the player joins the game. Will not be read if a `parent` exists.
`background` | [Identifier](data_types/identifier.md) | _optional_ | The ID of the texture that will be the background of the skill tree.
`condition` | [Condition](https://origins.readthedocs.io/en/latest/types/entity_condition_types/) | _optional_ | Makes it so that the player can only buy the skill if they meet this condition.
`cost` | [Integer](data_types/integer.md) | _optional_ | The amount of points that the player needs in order to purchase this skill.

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