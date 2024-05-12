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

# Compatibility
## Compatibility with other userChrome.css themes
I only tested this fix with [Firefox-GX](https://github.com/Godiesc/firefox-gx) and it works great but you need to copy all of the userChrome.css code from this repo and paste it into Firefox-GX's userChrome.css file. <br>
<details> 
  <summary> It should look something like this: </summary>

```
/* Source file made available under Mozilla Public License v. 2.0 See the main repository for updates as well as full license text. 
   https://github.com/Godiesc/firefox-gx */

   /* ONLY WORKS ON FIREFOX & LIBREWOLF */

   /* Remember to change your theme to anything other than "System theme - auto". */

   /* Minimize Button */

   .titlebar-min {
      border-radius: 0 !important;
      width: 50px !important;
      height: 44px !important;
      padding: 0px !important;
      position: inherit !important;

      > .toolbarbutton-icon {
         border-radius: 0 !important;
         width: 100% !important;
         height: 100% !important;
      }
   }

   /* Maximize Button */

   .titlebar-max {
      border-radius: 0 !important;
      width: 50px !important;
      height: 44px !important;
      padding: 0px !important;
      position: inherit !important;

      > .toolbarbutton-icon {
         border-radius: 0 !important;
         width: 100% !important;
         height: 100% !important;
      }
   }

   /* This button turns the maximized window into a smaller window. */

   .titlebar-restore {
      border-radius: 0 !important;
      width: 50px !important;
      height: 44px !important;
      padding: 0px !important;
      position: inherit !important;

      > .toolbarbutton-icon {
         border-radius: 0 !important;
         width: 100% !important;
         height: 100% !important;
      }
   }

   /* Close Button */

   .titlebar-close {
      border-radius: 0 !important;
      width: 50px !important;
      height: 44px !important;
      padding: 0px !important;
      position: inherit !important;

      > .toolbarbutton-icon {
         width: 100% !important;
         height: 100% !important;
      }
   }

  /* This code bellow is a fix for rounded top window corners. */

  /* If the window is maximized, make the red close background color *not* rounded. */


   :root:is([sizemode=maximized], [sizemode=fullscreen])

   .titlebar-close {
      > .toolbarbutton-icon {
         border-radius: 0 !important;
      }
   }

  /* If the window is *not* minimized, *make* the red close background color rounded because */
  /* side of the window gets rounded but the red background doesn't care. */


   :root:not([sizemode=maximized], [sizemode=fullscreen])

   .titlebar-close {
      > .toolbarbutton-icon {
         border-top-right-radius: 12% !important;
         border-top-left-radius: 0px !important;
         border-bottom-right-radius: 0px !important;
         border-bottom-left-radius: 0px !important;
      }
   }

  /* Empty space on the top left appears for some reason in windowed mode. */
  /* Also adds spacing to the plus icon on the right. */

  .titlebar-spacer[type="pre-tabs"] {
     display:none !important;
  }

  /* It had "absolute" value before and somehow */
  /* because of this bottom of the min-max-close buttons were not properly sized. */

  :root[tabsintitlebar] .titlebar-buttonbox {
     position: revert !important;
     appearance: none !important;
  }

  /* This fix is not related to the min-max-close buttons but */
  /* it fixes the very left corner misalignment. */

  .tabbrowser-tab {
     padding: 0 3px !important;
  }


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

Do **not** use this code since my code or Firefox-GX's code might be different in the future!
