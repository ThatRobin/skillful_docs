# Keybinding JSON Format

This is the format of a JSON file describing a keybinding. They need to be placed inside the `keybinds` folder within your namespace. Keybinds are used to activate active power types, and toggles.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`key` | [Key](data_types/key.md) | | A string that defines what key this binding will use.
`category` | [String](data_types/string.md) | | The category this key will fall under.

### Example

```json
{
    "key": "key.keyboard.h",
    "category": "key.category.test_category"
}
```
This example keybind will create a keybind bound to the "h" key, in the category called `key.category.test_category`.