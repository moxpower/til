# Sublime Text 3 Setup

Create link so Sublime Text is available via commandline shortcut.

    ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl

Set up the packages via Dropbox, so that changes in one Sublime setup are propagated through to other computer setups. This is done once.

    ln -s ~/Library/Application\ Support/Sublime\ Text\ 3/Packages ~/Dropbox/Sync/Sublime\ Text\ 3/Packages

    ln -s ~/Library/Application\ Support/Sublime\ Text\ 3/Installed\ Packages ~/Dropbox/Sync/Sublime\ Text\ 3/Installed\ Packages

On all satellite computers, run this command:

    ln -s ~/Dropbox/Sync/Sublime\ Text\ 3/Packages ~/Library/Application\ Support/Sublime\ Text\ 3/Packages

    ln -s ~/Dropbox/Sync/Sublime\ Text\ 3/Installed\ Packages ~/Library/Application\ Support/Sublime\ Text\ 3/Installed\ Packages

Source for this idea: I keep forgetting!
