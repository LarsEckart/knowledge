# Mac OS X

## Disable unread message counter from skype/slack dock icon

Goto System Preferences -> Notifications -> Slack/Skype and uncheck *Badge app icon*

## Show hidden (=everything) in file selection dialogs

&#8984; + Shift + .

## Disable ctrl+cmd+D key binding

I wanted to use this keybind in intellij but couldn't assign it. To disable this behaviour, just enter to the console

```
defaults write com.apple.symbolichotkeys AppleSymbolicHotKeys -dict-add 70 '<dict><key>enabled</key><false/></dict>'
```

and restart.

## Switch between desktops

Crtl + left/right arrow

## symlink log file to /tmp

```
cd /
sudo mkdir logs
cd logs/
sudo ln -s /tmp/dev.log service.log
```

Now if any app is configured to log to /logs/service.log, it will write to my
tmp folder which will be deleted on reboot :)
