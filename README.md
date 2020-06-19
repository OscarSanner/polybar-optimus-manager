# Script: info-optimus-manager

This is a script that shows information about which GPU is currently in use, given that the GPUs are managed by optimus manager. The script also lets you switch GPUs in one click, if this functionality is desired. 

![info-optimus-manager](screenshots/1.png)


## Dependencies

```
Optimus-manager
```

## Configuration



## Module

```ini
[module/{ name }]
type = custom/script
exec = ~/polybar-scripts/{ name }.sh
interval =
...
```

