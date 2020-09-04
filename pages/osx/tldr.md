# tldr

> A collection of community-maintained help pages for command-line tools, that aims to be a simpler, more approachable complement to traditional man pages.

- The following adds TextEdit.app to the end of the current user's dock:
`dockutil --add /Applications/TextEdit.app

- The following replaces Time Machine with TextEdit.app in the current user's dock:
`dockutil --add /Applications/TextEdit.app --replacing 'Time Machine'

- The following adds TextEdit.app after the item Time Machine in every user's dock on that machine:
`dockutil --add /Applications/TextEdit.app --after 'Time Machine' --allhomes

- The following adds ~/Downloads as a grid stack displayed as a folder for every user's dock on that machine:
`dockutil --add '~/Downloads' --view grid --display folder --allhomes

- The following adds a url dock item after the Downloads dock item for every user's dock on that machine:
`dockutil --add vnc://miniserver.local --label 'Mini VNC' --after Downloads --allhomes

- The following removes System Preferences from every user's dock on that machine:
`dockutil --remove 'System Preferences' --allhomes

- The following moves System Preferences to the second slot on every user's dock on that machine:
`dockutil --move 'System Preferences' --position 2 --allhomes

 - The following finds any instance of iTunes in the specified home directory's dock:
 `dockutil --find iTunes /Users/jsmith

 - The following lists all dock items for all home directories at homeloc in the form: item<tab>path<tab><section>tab<plist>
`dockutil --list --homeloc /Volumes/RAID/Homes --allhomes

- The following adds Firefox after Safari in the Default User Template without restarting the Dock
`dockutil --add /Applications/Firefox.app --after Safari --no-restart '/System/Library/User Template/English.lproj'

- The following adds a spacer tile in the apps section after Mail
`dockutil --add '' --type spacer --section apps --after Mail

- The following removes all spacer tiles
`dockutil --remove spacer-tiles
