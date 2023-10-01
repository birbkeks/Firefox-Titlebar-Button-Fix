# Firefox-Titlebar-Button-Fix
This theme fixes titlebar min max close buttons for Firefox in linux.

The bug is, if you put your cursor at the very top right corner, titlebar close button doesn't get selected unlike every other browser or Firefox in Windows 7/8/10/11 etc. (This problem might occur because of your desktop environment choice.)
<p align="center">
<img src="https://raw.githubusercontent.com/birbkeks/FirefoxCSS-Store.github.io/main/images/themes/ftbf.png">
</p>

# userChrome.css Code
```
.titlebar-buttonbox-container {
    position: absolute;
    right: -9px;
    top: -5px;
}

#alltabs-button {
    display: none !important;
}

.titlebar-spacer[type="pre-tabs"], .titlebar-spacer[type="post-tabs"] {
    display: none !important;
}

#private-browsing-indicator-with-label {
    margin-right: 100px !important;
}
```
# How to install
You need to create `chrome` folder in your Profile Directory, you can find your directory in  `about:support`.

After creating `chrome` folder, put `userChrome.css` file in it.

If you're using lastest version of Firefox you need to set `toolkit.legacyUserProfileCustomizations.stylesheets` to true in `about:config` or **any userChrome.css themes won't work**
