# PotionEffects

> With this feature, you can give all players potion effects during the season.

## How to use it?

In all your season configs, you can find this section:

```yaml
potionEffects:
  enabled: true
  entityEntries:
    regeneration: 1
    speed: 1
```

Every potion listed under `entityEntries` will be applied to all players.

> [Here](https://jd.papermc.io/paper/1.20.6/org/bukkit/potion/PotionEffectType.html#field-summary) is a list of all potion effects.

{style="note"}

## Examples

### Adding "strength 3" to the list
{collapsible="true"}

Let's say you want to give all players **strength 3**.
To achieve this, you have to add this line to the `entityEntries`.
```yaml
strength: 3
```

Your **final section** should look like this:

```yaml
potionEffects:
  enabled: true
  entityEntries:
    regeneration: 1
    speed: 1
    strength: 3
```