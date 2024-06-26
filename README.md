# Firefox-Titlebar-Button-Fix
This theme fixes titlebar min max close buttons for Firefox on linux.

## Table of contents

1. [What is this bug?](#what-is-this-bug)
2. [How to install?](#how-to-install)
3. [Showcase](#showcase)
4. [Compatibility](#compatibility)
   - [Compatibility with other userChrome.css themes](#compatibility-with-other-userchromecss-themes)
   - [Compatibility with Desktop Environments](#compatibility-with-desktop-environments)

# What is this bug?
If you put your cursor at the very top right corner, titlebar close button doesn't get selected unlike every other browser, or Firefox on Windows 7/8/10/11 etc. <br>
(none of the chromium based browsers have this problem on linux)

# How to install?

Unfortunately this fix has two different versions for different browsers based on Firefox. <br>
Please make sure to download the right files.

You can find your profile directory from `about:support`. <br>

![image](https://github.com/birbkeks/Firefox-Titlebar-Button-Fix/assets/67545942/4db37b8a-dfa7-42d9-b2c4-9c32f7d5e751)

1. Go to Settings -> Extensions & Themes and change the theme to anything other than "System theme — auto".
2. Enable `toolkit.legacyUserProfileCustomizations.stylesheets` from `about:config`, <br> otherwise Firefox will ignore userChrome.css file. 
3. Create `chrome` folder inside of your profile directory.
4. Download userChrome.css from releases.
>[!IMPORTANT]
> - Make sure to download userChrome.css file for the right browser! <br>
> - userChrome.css file is different for [Firefox & LibreWolf](https://github.com/birbkeks/Firefox-Titlebar-Button-Fix/releases/tag/FL) and [Waterfox, Floorp, GNU IceCat & Ghostery](https://github.com/birbkeks/Firefox-Titlebar-Button-Fix/releases/tag/WFIG)!

>[!NOTE]
> - On Floorp you also need to change a another option from Settings -> Design -> Browser appeareance and choose something other than "Firefox Photon・Lepton UI" and "GNOME Theme (deprecated)" <br>
![](https://github.com/birbkeks/Firefox-Titlebar-Button-Fix/assets/67545942/d1814a3b-c998-4961-977e-f9b704c6a6f8) <br>
> - Palemoon is **not** supported because it only uses your system's titlebar. <br>
> - Discontinued Firefox based browsers like Cliqz are also **not** supported.

5. Drag and drop userChrome.css into the chrome folder you made.
7. Restart the browser.

# Showcase

<div align="center">
  <p align=center><i>Default Dark theme</i></p>
<img src="https://github.com/birbkeks/Firefox-Titlebar-Button-Fix/assets/67545942/4923e3a5-d119-452d-8604-4ea3e5e357ec">
</div> <br>
<div align="center">
  <p align="center"><i><a href="https://github.com/Godiesc/firefox-gx">Firefox-GX</a> Theme</i></p>
<img src="https://github.com/birbkeks/Firefox-Titlebar-Button-Fix/assets/67545942/7b4dc716-18dd-4d24-a7cb-01867c15c467">
</div>

# Compatibility
## Compatibility with other userChrome.css themes
I only tested this fix with [Firefox-GX](https://github.com/Godiesc/firefox-gx) and it works great but you need to copy all of the userChrome.css code from this repo and paste it into Firefox-GX's userChrome.css file. <br>
<details> 
  <summary> It should look something like this: </summary>

```css

<-- Paste Firefox-Titlebar-Button-Fix code here -->

/* ############# Required files ############## */

@import url('components/ogx_root.css');
@import url('components/ogx_root-personal.css');
@import url('components/ogx_containers.css');
@import url('components/ogx_tabs-bar.css');
@import url('components/ogx_urlbar-searchbar.css');
@import url('components/ogx_windows-controls.css');
@import url('components/ogx_customize-styles.css');
@import url('components/ogx_sound.css');
@import url('components/ogx_arrowpanel.css');
@import url('components/ogx_contextual-menu.css');
@import url('components/ogx_notifications.css');
@import url('components/ogx_close-button.css');
@import url('components/ogx_button-styles.css');
@import url('components/ogx_library.css');
@import url('components/ogx_menu.css');
@import url('components/ogx_icons.css');

/* ############## Extra Files ###############  */

@import url('components/ogx_left-sidebar.css');
@import url('components/ogx_oneline.css');
@import url('components/ogx_tab-shapes.css');
@import url('components/ogx_tree-tabs.css');
@import url('components/ogx_autohide_bookmark-bar.css');
@import url('components/ogx_main-image.css');

/* ############# Your Personal File ##############  */

@import url('components/ogx_tricks.css');
```
</details>

Do **not** use this code because Firefox-GX's code might be different in the future!

## Compatibility with Desktop Environments

I tested this on only KDE.
