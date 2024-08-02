# Weather

> This feature lets you control the weather in the current season.

## How to use it?

You can disable this feature by setting the `enabled` option to `false` in your `config.yml` file.

```yaml
weather:
  enabled: false
```

In your config.yml you have 3 types that you can disable or enable:

```yaml
weather:
  weatherType:
    clear: true
    storm: true
    thunder: true
```

By setting a weather type to false, this plugin will consider it and cancel the weather change to that type.

> By disabling the type `storm`, the type `thunder` will also be disabled.

{style="warning"}