# polybar-optimus-manager

A script that shows the current GPU in use, given that the GPUs are managed by optimus-manager. The script also allows for switching in one click.

## Configuration

1. Make sure you have `enable-ipc=true` in the polybar config file.
2. Paste the content of the module section below into the polybar config file.
3. Edit the script and change the "Configuration" part to your liking.

4. **Please understand that this step is optional. Enabling this will let you switch GPU (and thus abruptly log out) in one click. There's not guarantee that your session will be saved.** If you want to enable switching when the module is pressed, uncomment the line `;click-left = polybar-msg hook info-optimus-manager-ipc 2`. In other words remove the ";" sign.


## Module

```ini
[module/info-optimus-manager-ipc]
type = custom/ipc
hook-0 = ~/.config/polybar/info-optimus-manager.sh
hook-1 = ~/.config/polybar/info-optimus-manager.sh --switch
initial = 1
;click-left = polybar-msg hook info-optimus-manager-ipc 2
```
