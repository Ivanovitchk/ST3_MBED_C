# Customized Sublime Text 3 for embedded-C

- Heavily customized config of Sublime Text 3 editor tailored for embedded-C
programming.

- includes many useful plugins like bin<->hex converters, hex viewer and a real-time C/C++ linter

- includes syntax highlighting like :<br/><br/>
<img width="793" alt="syntax_1" src="https://user-images.githubusercontent.com/12053635/70868948-1bc20400-1f86-11ea-86a8-63e7638bb4fe.PNG"> <br/>
  Only supported with the above black-background color scheme for now

- for newcomers, this [video][0] is a good start to discover sublime basics and it's <br/> awesome text-editing powers like multiple cursors, selections, snippet-system, ...



# Installation


- ## if sublime is not already installed

  - download and install [Sublime Text 3][1]

  - *clone* this repo somewhere on your computer, eg *desktop*.

  - launch ST3 and press simultaneously **CTRL + SHIFT + P** to open the *command palette*

  - type **Install Package Control** (or just **pcip**) and press enter

  - wait a bit and exit sublime text (make sur to close **all** open instances !)

  - copy & paste the repo contents (ctrl+A in root directory) **inside** <br/>
    **C:/Users/YOURNAME/AppData/Roaming/Sublime Text 3/Packages/.** <br/>
    Overwrite files if asked.

  - ST customizations will apply on launch:
      - don't worry about the garbled UI, we'll fix it later
      - install of all the plugins might take a few minutes depending on your bandwidth.
      - plugins will open update tabs as they install themselves,
      - progress can be tracked by opening the console (press " **²** " key) until log spam stops.

  - To fix the UI, open the *command palette* (**CTRL + SHIFT + P**) <br/>
    Type **package control : upgrade / overwrite all packages** (or just **pc uov**) <br/>
    Wait until completion.

  - restart ST one last time and you're good to go.



- ## if sublime is already installed on your system

  - close **all** instances of sublime

  - go to **C:/Users/YOURNAME/AppData/Roaming/Sublime Text 3/Packages/.** <br/>
    Make a backup somewhere else.

  - follow the *if sublime is not already installed* procedure except the 1st step

  - manually merge back the contents of the previous install to the cloned repo.

  - If you customized some settings & installed plugins before, pay attention to

      - **./Packages/User/Preferences.sublime-settings**
      - **./Packages/User/Package Control.sublime-settings**


# Optional

  - install the awesome & free coding font [Anonymous 3][2] (ST3 will try to use it by default)

  - install the [LLVM compiler][3] to have on-the-fly linting for C-language files

     - LLVM v9.0.0 tested OK as of Dec. 2019
     - linting requires per-project configuration fo the EasyClangComplete plugin.
     - a guide & template .sublime-project files will be provided soon™...




[0]:https://www.youtube.com/watch?v=zIkg3Oo1PVM "Youtube link to a nice video on ST3 features"
[1]:https://www.sublimetext.com/ "Sublime Text 3 homepage"
[2]:https://www.marksimonson.com/fonts/view/anonymous-pro "Anonymous Pro font download"
[3]:https://releases.llvm.org/download.html "LLVM compiler download"
