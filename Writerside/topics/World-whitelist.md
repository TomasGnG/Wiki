# World whitelist

> With the world whitelist you can specify worlds where the season effects should be applied.

## How to use it?

To **add** or **remove** a world, you have to change it directly in the `config.yml` file.

````yaml
# Specify the worlds where the seasons will work.
# A world not in this list will not be affected by any season changes.
worlds:
- world
````

## Examples

### Adding a world to the whitelist

Let's say you want to add your world `TestWorld` to the whitelist.<br />
To reach your goal, you just have to add the following line to you `worlds` section.

The section should look like this after adding the line:
```yaml
worlds:
  - world
  - TestWorld
```

### Removing a world from the whitelist

You previously added your `TestWorld` to the whitelist, and now you want to remove it.
To accomplish this, you have to remove the line with the world name (in this case: `TestWorld`)

```yaml
worlds:
  - world
  - TestWorld
```
{collapsible="true" collapsed-title="Section before removing"}

The section should look like this after removing the line:
```yaml
worlds:
  - world
```