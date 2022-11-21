# Skill Tree Power Data

Skillful makes some additions to apoli powers. This is done in the `skill` field.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`icon` | [Identifier](data_types/identifier.md) | _optional_ | The item which is displayed as the icon for the skill widget.
`parent` | [Identifier](data_types/identifier.md) | _optional_ | The skill identifier that will be the parent of this widget.
`background` | [Identifier](data_types/identifier.md) | _optional_ | The ID of the texture that will be the background of the skill tree.
`condition` | [Condition](https://origins.readthedocs.io/en/latest/types/entity_condition_types/) | _optional_ | Makes it so that the player can only buy the skill if they meet this condition.
`cost` | [Integer](data_types/integer.md) | _optional_ | The amount of points that the player needs in order to purchase this skill.

### Example

```json
{
	"skill": {
        "icon": {
            "item": "minecraft:feather"
        },
        "parent": "example_pack:skill_tree",
        "cost": 1
    }
}
```
This example in-power skill will create a skill widget that when purchased, grants the power it is in.