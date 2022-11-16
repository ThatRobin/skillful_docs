### Add Skill Points

Adds skill points to a players tree, allowing the developer to allocate points for certain actions.

Type ID: `skillful:add_skill_points`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`skill_tree` | [Identifier](../data_types/identifier.md) | | ID of the skill tree that the point will be given to (MUST BE THE ROOT OF THE SKILL TREE)

### Example
```json
{
    "entity_action": {
        "type": "skillful:add_skill_points",
        "skill_tree": "example_pack:skill_tree",
        "points": 1
    }
}
```

This example will add 1 point to the `example_pack:skill_tree` tree.
