# dockutil

> Utility to manage macOS dock

- List all items of the dock 

`dockutil --list`

- Add TextEdit.app to the end of the current user's dock:

`dockutil --add {{/Applications/TextEdit.app}}`

- Repalce Time Machine with TextEdit.app in the current user's dock:

`dockutil --add {{/Applications/TextEdit.app}} --replacing {{'Time Machine'}}`

- Add TextEdit.app after the item Time Machine in every user's dock on that machine: 

`dockutil --add {{/Applications/TextEdit.app}} --after {{'Time Machine'}} --allhomes`
 
 - Add ~/Downloads as a grid stack displayed as a folder for every user's dock:

`dockutil --add {{'~/Downloads'}} --view {{grid}} --display {{folder}} --allhomes`

- Add a url dock item with a label after the Downloads dock item for every user's dock on that machine: 

`dockutil --add {{vnc://miniserver.local}} --label {{'Mini VNC'}} --after {{Downloads}} --allhomes`

- Remove System Preferences from every user's dock on that machine: 

`dockutil --remove {{'System Preferences'}} --allhomes`

- Move System Preferences to the second on every user's dock on that machine:

`dockutil --move {{'System Preferences'}} --position {{2}} --allhomes`

- Finds any insgtance of iTunes in the specified home directory's dock:

`dockutil --find {{iTunes}} {{/Users/jsmith}}`

- Add Firefox after Safari in the Default User Template without restarting the dock 

`dockutil --add {{/Applications/Firefox.app}} --after {{Safari}} --no-restart {{'/System/Library/User Template/English.lproj'}}`

- Add a spacer tile in the apps section after Mail 

`dockutil --add {{''}} --type {{spacer}} --section {{apps}} --after {{Mail}}`

- Remove all spacer tiles 

`dockutil --remove {{spacer-tiles}}`