# AnimalGrowing

> This feature controls the growing time of baby animals, such as cows, sheeps, etc.
 
## How to use it?

In all the season configs, you can find this following section.

```yaml
animalGrowing:
  enabled: true
  entityEntries:
    cow: 120
    sheep: 120
```

### Adding format

To add a new entry to the `entityEntries` list, you have to follow this format:<br />
`<animal type>: <value>`.

The value is in seconds. If you, as an example, set the value to 5, then
the baby animal will grow in 5 seconds. Just like this GIF.

![AnimalGrowing Cow 5 Seconds.gif](AnimalGrowing Cow 5 Seconds.gif)

> The default growing time is about 24 minutes.

## Examples

### Adding baby chicken to the list
{collapsible="true"}

So if you want the baby chicken to grow in 15 seconds, you have to add this line
`chicken: 15` to the `entityEntries` list.

The section should look like this:

```yaml
animalGrowing:
  enabled: true
  entityEntries:
    cow: 120
    sheep: 120
    chicken: 15
```