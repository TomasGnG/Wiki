# CommandExecution

Execute player and console commands on a season change or after the season change.

## How to use?

In all your season configs, you can find this section:

```yaml
commandExecution:
  enabled: true
  events:
    onSeasonChange:
      p:
      - say Im %player%
      - say this is the second command
      c:
      - say Im the console
      - say this is the second command
    afterSeasonChange:
      group1:
        enabled: true
        runAfter:
          min: 5
          max: 10
        commands:
          p:
          - say Im %player%
          - say this is the second command
          c:
          - say Im the console
          - say this is the second command
```
{collapsible="true"}

In this section, you can find 2 events:
- `onSeasonChange`: All commands will be executed on a season change.
- `afterSeasonChange`: All commands will be executed after a specific time.

### Player and Console commands

You are able to specify if you want your command to be executed as **a player** or as **the console**.

#### p
`p` stands for **player** and all commands will be executed by the **online player**.

<note><code>%player%</code> will be replaced with the players' name.</note>

#### c
`c` stands for **console** and all commands will be executed by the **console**.

<note>If <code>%player%</code> is used in a command, then the command will be executed
for every online player. (Not <b>BY</b> the player!)</note>

#### Disabling either the player or the console commands

If you don't want any command to be executed by the player, you can just set the `p:` value to this `[]`.

So your section looks like this:
```yaml
onSeasonChange:
  p: []
  c:
  - say Im the console
  - say this is the second command
```

You can do this with the console commands as well.

### afterSeasonChange Groups
You can **create unlimited** groups under this section with their own ``runAfter`` delay.
The delay will be **generated** by the **two numbers** from the `runAfter` subsection.

Let me explain all the details to you by using this example section:
```yaml
afterSeasonChange:
  group1:
    enabled: true
    runAfter:
      min: 5
      max: 10
    commands:
      p:
      - say Im %player%
      - say this is the second command
      c:
      - say Im the console
      - say this is the second command
```

- `group1`: The name of your group. You can name your group whatever you want.
- `enabled`: If this is set to `true` then the commands will be executed.
- `runAfter.min`: This is the minimum value of the delay.
- `runAfter.max`: This is the maximum value of the delay.
- `commands`: The commands you want to be executed. The Explanation is [here](#player-and-console-commands).