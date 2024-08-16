# BossSpawning

Spawn creatures as bosses.

## How to use it?

In all your season configs, you can find this section:

```yaml
bossSpawning:
  enabled: true
  entityEntries:
    EasyZombie:
      enabled: true
      mobType: zombie
      displayname: <green>E-Tier BOSS <gray>| <green>%health%<gray>/<red>%maxhealth%
      spawnChance: 80
      itemInHand:
        enabled: true
        material: IRON_SWORD
        displayname: <green>E-Tier Sword
        dropChance: 70
        lore:
        - <gray>The sword of a fallen E-Tier boss.
        enchantments:
          sharpness: 1
          unbreaking: 1
      attributes:
        generic_max_health: 30
        generic_attack_damage: 3
      lootDrops:
        enabled: true
        entityEntries:
          ExampleItem:
            material: golden_apple
            displayname: <green>Golden Apple
            dropChance: 60
            amount: 1
            lore:
            - <gray>Dropped by <green>E-Tier bosses
            enchantments:
              mending: 1
```

**You might be thinking**: "There are so many options!"
but I just wanted to make sure that you can customize almost everything
to your needs. :)

### EntityEntries

Here you put all the new bosses.

> Copy & paste the existing example and adjust to your needs.

{title="Recommendation" style="note"}

### EasyZombie

This is the **internal** name for the boss. (**NOT** the displayname!)
This name is used for the `/dynamicseasons spawnboss` command.

> Make sure you don't use the same name twice!

{style="warning"}

### EasyZombie.enabled

If you set this option to false, then the boss won't spawn naturally.

### EasyZombie.displayname

Here you can set the displayname of the boss.

You can use **2 placeholders**:

1. `%health%` which will display the creatures' current health.
2. `%maxhealth%` which will display the creatures' max health. (set by `EasyZombie.attributes`)

### EasyZombie.itemInHand

In this section, you can change the item that will be in the hand of the creature.

### EasyZombie.attributes

Check out the [`CreatureAttributes`](CreatureAttributes.md) page.

### EasyZombie.lootDrops

Check out the [`LootDrops`](LootDrops.md) page.

## Examples

### Adding an extra skeleton boss

{collapsible="true"}

As **recommended** above, you can just **copy & paste** the existing
boss and adjust every to your needs, what I will just do.

So in this example, I want to spawn a skeleton
boss with **100 hearts** and I want it to drop
a good **diamond sword** with a **20% drop chance**. 
I want this skeleton to spawn with a **15% spawn chance**.
Let's name it **`RareSkeleton`**.

After copying & pasting and adjusting the options, 
your `bossSpawning` section should look like this:

```yaml
bossSpawning:
  enabled: true
  entityEntries:
    EasyZombie:
      enabled: true
      mobType: zombie
      displayname: <green>E-Tier BOSS <gray>| <green>%health%<gray>/<red>%maxhealth%
      spawnChance: 80
      itemInHand:
        enabled: true
        material: IRON_SWORD
        displayname: <green>E-Tier Sword
        dropChance: 70
        lore:
        - <gray>The sword of a fallen E-Tier boss.
        enchantments:
          sharpness: 1
          unbreaking: 1
      attributes:
        generic_max_health: 30
        generic_attack_damage: 3
      lootDrops:
        enabled: true
        entityEntries:
          ExampleItem:
            material: golden_apple
            displayname: <green>Golden Apple
            dropChance: 60
            amount: 1
            lore:
            - <gray>Dropped by <green>E-Tier bosses
            enchantments:
              mending: 1
    RareSkeleton:
      enabled: true
      mobType: skeleton
      displayname: <green>C-Tier BOSS <gray>| <green>%health%<gray>/<red>%maxhealth%
      spawnChance: 15
      itemInHand:
        enabled: false
        material: IRON_SWORD
        displayname: <green>E-Tier Sword
        dropChance: 70
        lore:
        - <gray>The sword of a fallen E-Tier boss.
        enchantments:
          sharpness: 1
          unbreaking: 1
      attributes:
        generic_max_health: 200
        generic_attack_damage: 7
      lootDrops:
        enabled: true
        entityEntries:
          GoodDiamondSword:
            material: diamond_sword
            displayname: <gold>A good diamond sword
            dropChance: 20
            amount: 1
            lore:
            - <gray>Dropped by <green>E-Tier bosses
            enchantments:
              sharpness: 1
```

> You're probably wondering why I set the `generic_max_health` attribute to **200** instead of **100**.
> It's straightforward! 1 heart is equal to 2 heart points and 100 hearts are 200 heart points.

{style="note"}

Here is a list of all options I changed in this example.
1. `mobType`
2. `displayname`
3. `spawnChance`
4. `itemInHand.enabled`
5. `attributes.generic_max_health`
6. `attributes.generic_attack_damage`
7. `lootDrops.entityEntries`