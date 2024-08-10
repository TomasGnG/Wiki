# RandomTickSpeed

> This feature manipulates the growth of several plants. As an example trees.
 
## How to use it?

In all your season configs you can find a section where you can enable or disable the feature
and change the value of it.

```yaml
randomTickSpeed:
  enabled: true
  value: 10
```

> RandomTickSpeed is an existing gamerule which you can set by yourself.
> However, this [plugin](DynamicSeasons.topic) only sets it for the [whitelisted worlds](World-whitelist.md).

### What does the value say?

The higher the value, the faster is the growth process of plants.

> Be careful with high values as it can lag your server.

{style="warning"}

## Examples


### Value 1000
{collapsible="true"}

> Remember that I set the value this high for demonstration purposes only!
> High values can cause lags on your server
 
{style="warning"}

The plants, crops, etc. will spawn a lot faster than usual.
Here is a demonstration gif:

![RandomTickSpeed 1000.gif](RandomTickSpeed 1000.gif)

As you can see, the tree grew almost instantly.
And this applies for crops as well.
As a reference the tree would take like 10 minutes to grow with the
default value of 3.