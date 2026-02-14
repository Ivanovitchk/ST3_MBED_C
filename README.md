# Customized Sublime Text for embedded-C

- Heavily customized config of Sublime Text editor tailored for embedded-C
programming.

- includes many useful plugins like bin<->hex converters, hex viewer, trailing
whitespace highlighting & trimming, bracket highlighting, git gutter...

- includes syntax highlighting like :<br/><br/>
<img width="793" alt="syntax_1" src="https://user-images.githubusercontent.com/12053635/70868948-1bc20400-1f86-11ea-86a8-63e7638bb4fe.PNG"> <br/>
  Only supported with the above black-background color scheme for now

- for newcomers, this [video][0] is a good start to discover sublime basics and it's <br/> awesome text-editing powers like multiple cursors, selections, snippet-system, ...



# Installation (Sublime Text 4 - Linux)


- ## Fresh install

  - download and install [Sublime Text 4][1]

  - *clone* this repo somewhere on your computer, eg *desktop*.

  - launch ST4 and press simultaneously **CTRL + SHIFT + P** to open the *command palette*

  - type **Install Package Control** (or just **pcip**) and press enter

  - wait a bit and exit sublime text (make sure to close **all** open instances !)

  - copy & paste the repo contents **inside** <br/>
    **~/.config/sublime-text/Packages/** <br/>
    Overwrite files if asked. This should give you:
    ```
    ~/.config/sublime-text/Packages/
    ├── Material Theme/
    │   └── .python-version
    └── User/
        ├── Preferences.sublime-settings
        ├── Sunburst_VNR.tmTheme
        ├── Material-Theme-Darker.sublime-theme
        ├── ... (all other settings)
    ```

  - ST customizations will apply on launch:
      - install of all the plugins might take a few minutes depending on your bandwidth.
      - progress can be tracked by opening the console (press " **²** " key) until log spam stops.

  - restart ST one last time and you're good to go.


- ## Windows

  Same procedure but the packages path is: <br/>
  **C:/Users/YOURNAME/AppData/Roaming/Sublime Text/Packages/**


- ## If sublime is already installed on your system

  - close **all** instances of sublime

  - go to your packages path and make a backup somewhere else.

  - follow the *Fresh install* procedure except the 1st step

  - manually merge back the contents of the previous install to the cloned repo.

  - If you customized some settings & installed plugins before, pay attention to

      - **./Packages/User/Preferences.sublime-settings**
      - **./Packages/User/Package Control.sublime-settings**


# Known issues & caveats

  - **Package Control bootstrap race**: on first launch, some packages
    (AlignTab, TrailingSpaces) may get stuck in `in_process_packages` and end
    up in `ignored_packages`. Fix: clear `in_process_packages` in
    `Package Control.sublime-settings`, remove the affected packages from
    `ignored_packages` in `Preferences.sublime-settings`, restart ST.

  - **Material Theme Python runtime**: Material Theme has no `.python-version`
    file, so ST4 loads it under Python 3.3 where `mdpopups` is unavailable,
    causing `AttributeError: 'module' object has no attribute 'version'`.
    Fix: the `Material Theme/.python-version` file (containing `3.8`) in this
    repo forces the correct runtime. Make sure it's copied to
    `Packages/Material Theme/`.

  - **Material Theme SyntaxWarnings**: harmless `"is" with a literal` warnings
    in the console from `extras.py`. Material Theme is unmaintained, these
    won't be fixed upstream but don't affect functionality.

  - **soupsieve warning**: `The soupsieve package is not installed` from bs4.
    Cosmetic, does not affect functionality.

  - **SublimeCImproved_VNR**: installed automatically by Package Control via
    the custom repository URL in `Package Control.sublime-settings`.


# Optional

  - install the awesome & free coding font [Anonymous Pro][2] (ST will try to use it by default)

  - on Linux, install **Segoe UI Variable** for the sidebar font (the theme override expects it):
    - Arch/CachyOS: `paru -S ttf-segoe-ui-variable`
    - or download from [Microsoft][3]


[0]:https://www.youtube.com/watch?v=zIkg3Oo1PVM "Youtube link to a nice video on ST features"
[1]:https://www.sublimetext.com/ "Sublime Text 4 homepage"
[2]:https://www.marksimonson.com/fonts/view/anonymous-pro "Anonymous Pro font download"
[3]:https://learn.microsoft.com/en-us/typography/font-list/segoe-ui "Segoe UI font"
