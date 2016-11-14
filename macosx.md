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