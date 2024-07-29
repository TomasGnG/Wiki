# PlaceholderAPI Support

> This plugin has a PlaceholderAPI support. Which means you can use the two placeholders
> from this plugin.

> If [PlaceholderAPI](https://www.spigotmc.org/resources/6245) is not installed, then this feature will be disabled.

## How to use it?

This plugin offers you two placeholder that you can use ingame:
- **duration**: This shows how much time is left for the next season change.
- **currentseason**: This shows the current season.

### Duration

In your `config.yml` file you can find the following section, where you can edit the
name and the output of this placeholder.

<code-block ignore-vars="true" lang="yaml" collapsible="true" collapsed-title="duration section">
placeholders:
  duration:
    placeholderName: duration
    format: HH:mm:ss
</code-block>

#### Placeholdername

With this option you can change the name of the `duration` placeholder.
Let's say you want it to be `testduration` so you have to change it like this:
```yaml
placeholderName: testduration
```

#### Format

Now this is a bit complicated, but dont worry I will explain it to you.
The duration placeholders output is in seconds and with the format you can
convert the seconds into hours, minutes and seconds. 

#### Examples
{collapsible="true"}

> Click [here](https://help.gooddata.com/cloudconnect/manual/date-and-time-format.html#:~:text=Table%C2%A028.3.%C2%A0Date%20Format%20Pattern%20Syntax%20(Java)) to see all letters for formatting the seconds.

##### Default format

We have 3600 seconds left which is equally to 1 hour.
The format `HH:mm:ss` will turn the seconds into this: `01:00:00`.

##### Text between format

In case you find the format of the `Default format` boring and want something else, you can also do this:

You can write something between the hours, minutes and seconds by using this character `'`.
The `'` character acts like a switch which tells the program to use the next characters as a
format or as a normal text.

This format `HH\' hours \'mm\' minutes \'ss\' seconds\'` will turn the seconds to this: `01 hours 00 minutes 00 seconds`
> Remember that you have to put the `'` character at the end as well.

> The `\` character is **really important**. If you don't use this character, you will see a large yaml error.
> That is not related to my plugin. It's just a parsing error, which was caused by you.

### CurrentSeason

In your config.yml file you can find the following section, where you can edit the name and the out of this placeholder.

```yaml
placeholders:
  currenseason:
    placeholderName: currentseason
    text:
      spring: Spring
      summer: Summer
      fall: Fall
      winter: Winter
```
{collapsible="true"}

#### Placeholdername {id="placeholdername_1"}

With this option you can change the name of the `currentseason` placeholder.
Let's say you want it to be `testcurrentseason` so you have to change it like this:
```yaml
placeholderName: testcurrentseason
```

#### Text replacement

There are 4 seasons. `Spring`, `Summer`, `Fall` and `Winter`.
For each of these seasons you can change the output.

Let's say, you want to show `Springfield` for the `Spring` season.
The section would look like this:
```yaml
placeholders:
  currenseason:
    placeholderName: currentseason
    text:
      spring: Springfield
      summer: Summer
      fall: Fall
      winter: Winter
```
{collapsible="true" collapsed-title="Updated section"}

> The text replacement does not take any color codes. It's just a plain text replacement without any formatting.