## Dark searchbar and dark background on new tabs in Firefox.

In order to use it, you need to find your user profile folder. Just open Firefox and type this in the URL bar:

about:profiles

Open the "root" directory and add the userChrome.css file in there. You can also modify it if you want to.

This is what it looks like:

![This is what the URL/Search bar looks like](https://user-images.githubusercontent.com/10587438/42100161-1ebfcda8-7bc8-11e8-9577-597a171dfb01.png)

## Making Slack dark

For the new versions (3+) of Slack, you need to edit two files. First you can find your Slack installation directory in the following locations:


    Windows: %homepath%\AppData\Local\slack\
    Mac: /Applications/Slack.app/Contents/
    Linux: /usr/lib/slack/ (Debian-based)

In there you need to open both the following files, and add the content of darkSlack.css at the bottom of them:

resources\app.asar.unpacked\src\static\index.js
resources\app.asar.unpacked\src\static\ssb-interop.js

Please note that if you installed Slack through Snap, you won't be able to edit the files since they're mounted on a read-only filesystem. Just remove Slack from Snap and install it separately.

This functionality is an edit of the following repo, which didn't work completely for me: https://github.com/widget-/slack-black-theme
