```yaml
init_item: stone
item_name: name
namespace:default # (minecraft)
name: default # (item_name)
description: default
nbt: {nbt} 
```

```yaml
init_item: blaze_rod
item_name: wand
namespace: frostcraft
name: &r&7**Wand**
lore: &r&b**A &3Magical &bWand**
nbt: {
  frostcraft: { wand: true }
} # excluding name and lore.
```
Now it can be used in commands such as 
/summon frostcraft:wand
or in crafting recipies, etc..
When giving or writing etc.., it should (by default) automatically add a tag to the item that makes it different from other items, and easy to select.
Probably a nbt tag
```yaml
nbt:
  {{plugin_name}}:
    {{namespace}}:
      name: {{name}}
      id: {{id}} # [optional]
```
The generated wand nbt would be
```yaml
nbt:
  extra_recipies:
    frostcraft:
      name: wand
```