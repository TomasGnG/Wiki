# AnimalSpawning

> This feature controls the spawn chance of animals.

## How to use it?

In all the seasons configs, you can find the following section:

```yaml
animalSpawning:
  enabled: true
  entityEntries:
    cow: 75
    chicken: 25
```

To add an animal to the list, you have to extend the `entityEntries` list.<br />
The format to add an animal is like this: `<name>: <spawn chance>`.

> The spawn chance is in percentage. (0 to 100)
 
### Demonstration

In the following GIF you can see me spawning 5 cows.
But because I set the spawn chance of cows to 50, there will
only spawn 3 out of 5 cows.

![AnimalSpawning Cow 50 Percent example.gif](AnimalSpawning Cow 50 Percent example.gif)

## Examples

### Adding sheep to the list
{collapsible="true"}

Let's say you want to have a 25% spawn chance for the sheep.
Just like I mentioned in the [](#how-to-use-it)section, you have
to add an animal in this format `<name>: <spawn chance>` to the
`entityEntries` list.

Your final section should look like this:

```yaml
animalSpawning:
  enabled: true
  entityEntries:
    cow: 75
    chicken: 25
    sheep: 25
```
