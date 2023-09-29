# Firefox-Titlebar-Button-Fix
This theme fixes titlebar min max close buttons for Firefox in linux.

```
.titlebar-buttonbox-container {
    position: absolute;
    right: -9px;
    top: -5px;
}
```
You need to create `chrome` folder in your Profile Directory, you can find your directory in  `about:support`.

After creating `chrome` folder, put `userChrome.css` file in it.

If you're using lastest version of Firefox you need to set `toolkit.legacyUserProfileCustomizations.stylesheets` to true in `about:config` or **any userChrome.css themes won't work**
