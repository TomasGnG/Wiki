# CreatureAttributes

> This feature manages the attributes of a creature.

## How to use it?

In all season configs, you can find the following section:

```yaml
creatureAttributes:
  enabled: true
  entityEntries:
    zombie:
      generic_max_health: 40.0
```

The default section already has an entry for zombies.

> [Here](https://jd.papermc.io/paper/1.21/org/bukkit/attribute/Attribute.html#enum-constant-summary) is a list of all attributes that you can use.

{style="note"}

> If you need more explanation about the specific attributes, you can check [this](https://minecraft.fandom.com/wiki/Attribute#Attributes_available_on_all_living_entities) website.

{style="note"}

## Examples

> There is no limit of how many attributes you can apply to the creature.
> The only thing you might consider: a creature might not take every attribute.

### Adding an attribute for skeletons
{collapsible="true"}

That's simple!

Under the `entityEntries` section you have to add a new entry with the type of the creature, in this case `skeleton`.

But that's not all. You have to add an attribute to the skeleton, so it can work properly.
It's done by writing the attribute in this format `<attribute name>: <value>`.
We will take the `generic_movement_speed` attribute as an example, and we set it to `0.5`.

After all changes, your section should look like this:

```yaml
creatureAttributes:
  enabled: true
  entityEntries:
    skeleton:
      generic_movement_speed: 0.5
    zombie:
      generic_max_health: 40.0
```