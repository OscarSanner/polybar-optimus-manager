# polybar-optimus-manager

##### This script has been pulled into the repository [Polybar-Scripts](https://github.com/polybar/polybar-scripts) and the version found there is more up to date.

A script that shows the current GPU in use, given that the GPUs are managed by optimus-manager. The script also allows for switching in one click. 

![polybar-optimus-manager](screenshots/1.png)

## Configuration

1. Make sure you have `enable-ipc=true` in the polybar config file.
2. Paste the content of the module section below into the polybar config file.
3. Place the script in ~/.config/polybar/ or change the path in the module to point at your prefered directory for polybar scripts
4. Navigate to the folder containing the script and run `chmod +x info-optimus-manager.sh` to make it executable.
5. Edit the script and change the "Configuration" part to your liking. This is not necessary if you don't use the "Hybrid" mode and are happy with the default outputs. 

6. **Please understand that this step is optional. Enabling this will let you switch GPU (and thus abruptly log out) in one click.** If you want to enable switching when the module is pressed, uncomment the line `;click-left = polybar-msg hook info-optimus-manager-ipc 2`. In other words remove the ";" sign.


## Module

```ini
[module/info-optimus-manager-ipc]
type = custom/ipc
hook-0 = ~/.config/polybar/info-optimus-manager.sh
hook-1 = ~/.config/polybar/info-optimus-manager.sh --switch
initial = 1
;click-left = polybar-msg hook info-optimus-manager-ipc 2
```
