# Firefox-Titlebar-Button-Fix
This theme fixes titlebar min max close buttons for Firefox on linux.

## What is this bug?
If you put your cursor at the very top right corner, titlebar close button doesn't get selected unlike every other browser, or Firefox on Windows 7/8/10/11 etc. <br>
(none of the chromium based browsers have this problem on linux)

# How to install?

Unfortunately this fix has two different versions for different browsers based on Firefox. <br>
Please make sure to download the right files.

You can find your profile directory from `about:support`.

1. Go to Settings -> Extensions & Themes and change the theme to anything other than "System theme — auto".
2. Enable `toolkit.legacyUserProfileCustomizations.stylesheets` from `about:config`, <br> otherwise Firefox will ignore userChrome.css file. 
3. Create `chrome` folder inside of your profile directory.
4. Download userChrome.css.
>[!IMPORTANT]
> - Make sure to download userChrome.css file for the right browser! <br>
> - userChrome.css file is different for "Firefox & LibreWolf" and "Waterfox, Floorp, GNU IceCat & Ghostery"!

>[!NOTE]
> - On Floorp you also need to change a another option from Settings -> Look & Feel -> Browser appeareance and choose something other than "Firefox Photon・Lepton UI" and "GNOME Theme (deprecated)" <br>
> - Palemoon is **not** supported because it only uses your system's titlebar. <br>
> - Discontinued Firefox based browsers like Cliqz are also **not** supported.

5. Drag and drop userChrome.css into the chrome folder you made.
7. Restart the browser.

# Compatibility
## Compatibility with other browsers

