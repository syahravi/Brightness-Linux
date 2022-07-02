# Brightness Linux
Aw for you.

## Solution
1. Search filename `20-intel.conf`
```sh
ls /usr/share/X11/xorg.conf.d/
```
2. Create filename `20-intel.conf` in `/usr/share/X11/xorg.conf.d/`
```sh
Section “Device”
        Identifier  “card0”
        Driver      “intel”
        Option      “Backlight”  “intel_backlight”
        BusID       “PCI:0:2:0”
EndSection
```

## Extras
### Setup Openbox
1. Openbox users - open `~/.config/openbox/rc.xml`
```xml
<keybind key="XF86MonBrightnessUp">
    <action name="Execute">
        <command>xbacklight +10</command>
    </action>
</keybind>
<keybind key="XF86MonBrightnessDown">
    <action name="Execute">
        <command>xbacklight -10</command>
    </action>
</keybind>
```
