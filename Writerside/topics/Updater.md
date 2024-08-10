# Updater

> With the updater feature you are able to update 
> the plugin to the latest version without downloading 
> it manually from the SpigotMC website.

{title="Introduction"}


## How to use it?

If there is an update available, you will see a message in your console:
![](Message_In_Console.png)

To update the plugin you have to use the ``/dynamicseasons update`` command.
And if the update was successful you will see the following message:
![](Update_Successful.png)

However, if you're using the latest version then you will see this message:
![Message_Latest_Version.png](Message_Latest_Version.png)

## Other remarks

There are also some messages that you can change in the `messages.yml` file.

```yaml
command:
  update:
    noUpdatesAvailable: '%prefix% <green>There are no updates available.'
    started: '%prefix% <green>Updating...'
    success: '%prefix% <green>Update was successful. Restart server to use the update.'
    failure: '%prefix% <red>Update failed. See console for the detailed error.'
```
{collapsible="true" collapsed-title="messages.yml"}