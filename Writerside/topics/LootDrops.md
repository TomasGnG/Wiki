# LootDrops

Add custom loot for creatures and blocks.

## How to use it?

In all season configs, you can find this section:

```yaml
lootDrops:
  enabled: true
  entityEntries:
    zombie:
      ExampleSword:
        material: diamond_sword
        displayname: <yellow>Tomas' Legendary Sword
        lore:
        - <gray>This sword
        - <gray>is <red>dangerous</red>!
        amount: 1
        dropChance: 10
        enchantments:
          sharpness: 3
          unbreaking: 5
```

In the beginning it might be complicated, but don't worry it's not that
complicated after reading this page! :)

### Understanding the format of the section

This is the base part of this feature:

```yaml
lootDrops:
  enabled: true
  entityEntries:
```

Here is a detailed explanation about the further options and values in this section:

<procedure>
    <step><code>zombie</code>: A <a href="https://jd.papermc.io/paper/1.20.6/org/bukkit/entity/EntityType.html#enum-constant-summary">creature</a> or a <a href="https://jd.papermc.io/paper/1.20.6/org/bukkit/Material.html#enum-constant-summary">block</a> which you want to add custom loot for</step>
    <step><code>ExampleSword</code>: A name for this item entry (doesn't matter what you put here if it's <b>unique</b>)</step>
    <step><code>material</code>: The <a href="https://jd.papermc.io/paper/1.20.6/org/bukkit/Material.html#enum-constant-summary">material</a> of the item.</step>
    <step><code>displayname</code>: The displayname of the item in <a href="https://docs.advntr.dev/minimessage/format.html">MiniMessage</a> format</step>
    <step><code>lore</code>: The lore of the item as a list. Also in MiniMessage format.</step>
    <step><code>amount</code>: The amount of the dropped item.</step>
    <step><code>dropChance</code>: The dropchance of the item. Range: 0 - 100</step>
    <step><code>enchantments</code>: The enchantments for the item. Format: <code>{enchantment}: {level}</code></step>
</procedure>

<tip>
If you don't want any enchantments or lore for the item, you can do this:
<code-block lang="yaml">
lore: []
enchantments: []
</code-block>
</tip>

<note>
There is no limit for loot entries. Which means you could
theoretically add unlimited items to a creature or a block.
</note>

## Examples

### Adding 2 items to a diamond ore

{collapsible="true"}

Alright, you want to add **a golden hoe** and **4 iron ingots** to **diamond ores**.

This means we have to add a new entry to the `entityEntries` list.
The name for the diamond ore is `diamond_ore`, which we need for the entry.
Let's start with the golden hoe. I will name it `GoldHoe`.
For the other options given, I will just put something random.

> I recommend you to copy & paste the existing `zombie` entry.

Your section should look like this:

```yaml
lootDrops:
  enabled: true
  entityEntries:
    diamond_ore:
      GoldHoe:
        material: golden_hoe
        displayname: <yellow>A golden hoe
        lore:
        - <gold>golden!
        amount: 1
        dropChance: 20
        enchantments: []
```

If your section looks like this, then you did everything correct.

Now with that, we will just repeat it for the `4 iron ingots`.

> Avoid duplicate creatures / blocks in the `entityEntries` list!

{style="warning"}

After the copy & paste and customizations, your final section should
look like this:

```yaml
lootDrops:
  enabled: true
  entityEntries:
    diamond_ore:
      GoldHoe:
        material: golden_hoe
        displayname: <yellow>A golden hoe
        lore:
        - <gold>golden!
        amount: 1
        dropChance: 20
        enchantments: []
      RandomAssIron:
        material: iron_ingot
        displayname: <gray>Iron INGOTS
        lore: []
        amount: 4
        dropChance: 80
        enchantments: []
```