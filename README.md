# Firefox-Titlebar-Button-Fix
This theme fixes titlebar min max close buttons for Firefox in linux.

## What is this bug?
If you put your cursor at the very top right corner, titlebar close button doesn't get selected unlike every other browser, or Firefox on Windows 7/8/10/11 etc. <br>
(none of the chromium based browsers have this problem)

<p align="center">
<img src="https://raw.githubusercontent.com/birbkeks/FirefoxCSS-Store.github.io/main/images/themes/ftbf.png">
</p>

# How to install

>[!IMPORTANT]
>Make sure to apply Dark or Light theme from Extensions & Themes to make it work.

You need to create `chrome` folder in your Profile Directory, you can find it from `about:support`.

After creating `chrome` folder, put `userChrome.css` file in it.

If you're using latest version of Firefox you need to set `toolkit.legacyUserProfileCustomizations.stylesheets` to true in `about:config` or **any of the userChrome.css theme won't going to work**

# userChrome.css Code

> [!NOTE]
>Applying this theme breaks All tabs button so I had remove it to fix it, you can edit it back but it will look weird than usual. 
>To get it back, just delete (in the line 36) `display: none !important` from `#alltabs-button` and add 
>```
>margin-right: 100px !important;
>```


```
.titlebar-buttonbox-container {
    position: absolute;
    right: -6px;
    top: 2px;
}

:root[tabsintitlebar] .titlebar-buttonbox {
    width: 142px !important;
    height: 32px !important;
}

.titlebar-min:-moz-lwtheme {
    border-radius: 0 !important;
    width: 40px !important;
    height: 37px !important;
}

.titlebar-max:-moz-lwtheme {
    border-radius: 0 !important;
    width: 40px !important;
    height: 37px !important;
}

.titlebar-restore:-moz-lwtheme {
    border-radius: 0 !important;
    width: 40px !important;
    height: 37px !important;
}

.titlebar-close:-moz-lwtheme {
    border-radius: 0 !important;
    width: 56px !important;
    height: 37px !important;
}

#alltabs-button {
    display: none !important;
}

.titlebar-spacer[type="pre-tabs"], .titlebar-spacer[type="post-tabs"] {
    display: none !important;
}

#private-browsing-indicator-with-label {
    margin-right: 145px !important;
}
```
