# Particles

Show many season-specific particles with this feature.

## How to use it?

In all your season configs, you can find this section:

```yaml
particles:
  enabled: true
  offset:
    x: 5.0
    y: 10.0
    z: 5.0
  spawnTime: 5
  speed: 0.0
  entityEntries:
    snowflake:
      minSpawnAmount: 10
      maxSpawnAmount: 50
```

At first, it might look complicated, but you won't feel
like this after reading through this. ;)

### Offset

The **offset** tells the plugin to **spread out** the **spawned particles** in all directions.

You can imagine a box with the size of the values in the offset section, 
and in that box the particles will spawn.

### SpawnTime

The **spawnTime** specifies the delay cycle of the spawning.

It's given in ticks, which means **20 ticks** is equal to **1 second**.

Let's say you set the spawnTime to 10 ticks. With this value, 
all the particles will spawn every 0.5 seconds.

### Speed

The **speed** is for the spawned particles.

With a lower value, the particles will fly slower.

> **`0.0`** is the slowest and **`1.0`** is the fastest.

### EntityEntries

This is the list where you put all the particles
that you want to show in the current season.

Check out the [``Spawning 'cherry_leaves' particles``](#example spawn cherry_leaves particles) example to see how to add more particles.

#### Format

The plugin generates a random number between the `minSpawnAmount` and the `maxSpawnAmount`,
that will be used as the spawn amount for the particle.

```yaml
  entityEntries: # The section
    snowflake: # This is the name of the particle. 
      minSpawnAmount: 10 # The minimum amount to be spawned. 
      maxSpawnAmount: 50 # The maximum amount that can be spawned
```

> [Here](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Particle.html#enum-constant-summary) is a list of all available particles.

{style="note"}

## Examples

### Spawning 'cherry_leaves' particles

{collapsible="true" id="example spawn cherry_leaves particles"}

You're in your `spring_config.yml` file, and you want to spawn
the particle `cherry_leaves`.

The first step is to choose the correct particle name from the
[given website](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Particle.html#enum-constant-summary).

In this case it's `cherry_leaves`.

Now you want to specify the `minSpawnAmount` and the `maxSpawnAmount`.
We will use a minimum of `20` and a maximum of `40`.

> I recommend you to just copy & paste the existing particle
> and adjust it.

Your final section should look like this:

```yaml
particles:
  enabled: true
  offset:
    x: 5.0
    y: 10.0
    z: 5.0
  spawnTime: 5
  speed: 0.0
  entityEntries:
    snowflake:
      minSpawnAmount: 10
      maxSpawnAmount: 50
    cherry_leaves:
      minSpawnAmount: 20
      maxSpawnAmount: 40
```