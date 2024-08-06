# PreventCropGrowing

> With this config, you can disable the growing of trees and crops.

## How to use it?

In all the season configs, you can find this section:

```yaml
preventCropGrowing:
  enabled: true
  entityEntries:
  - wheat
  - birch
```

Every crop or tree listed under `entityEntries` will be **prevented from growing**.

> If you want to add a **tree** to the list, you have to get the correct name [here](https://jd.papermc.io/paper/1.20.6/org/bukkit/TreeType.html#enum-constant-summary)

{style="note"}

## Examples

### Adding the oak tree to the list

{collapsible="true"}

You want to prevent the **`oak tree`** from spawning.
For that, you have to get the **correct name** from this [website](https://jd.papermc.io/paper/1.20.6/org/bukkit/TreeType.html#enum-constant-summary).

After you get the correct name (in this case it's called `tree`), you have to
write it to the `entityEntries` list.

After adding the oak tree to the list, your section should look like this:

```yaml
preventCropGrowing:
  enabled: true
  entityEntries:
  - wheat
  - birch
  - tree
```

You successfully prevented the oak tree from growing.