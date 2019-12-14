# SublimeText3 customizations

- customized config of Sublime Text 3 editor

- includes V-naming rules syntax highlighting

- includes many usefull plugins for embedded dev

- for new users, this [video][0] is a good start on how to use the awesome editor features of ST3



# Installation


- ## if sublime is not already installed

  - download and install [Sublime Text 3][1]

  - open sublime, type "CTRL + SHIFT + P" to open the command palette

  - type Install Package Control and press enter

  - wait and exit sublime text (make sur to close *all* open instances !)

  - clone this repo somewhere on your computer, eg desktop.

  - open the repo and copy all it's content (ctrl+A inside the repo root directory) and paste it to
  **C:\Users\YOURNAME\AppData\Roaming\Sublime Text 3\.**. Overwrite files if asked.

  - All customizations will apply on launch (packages downloads & install will happen, which
  will take a few minutes or more depending on your itnernet speed).
  Progress can be tracked by view menu & console

  - you will have a garbled interface until you open the command palette (CTRL + SHIFT + P)
    and type "package control : upgrade / overwrite all packages", wait until completion

  - close all the package-controlled-opened plugin tabs

  - restart sublime one last time and you're good to go.



- ## if sublime is already installed on your system

  - close all instances of sublime

  - go to **C:\Users\YOURNAME\AppData\Roaming\Sublime Text 3\.** and make a backup somewhere else

  - follow the "if sublime is not already installed" procedure except it's first step

  - manually merge back the contents of the previous install to the cloned repo.

  - If you customized some settings & installed plugins before, pay attention to

      - ".\Packages\User\Preferences.sublime-settings" if manually modified before
      - ".\Packages\User\Package Control.sublime-settings" if manually modified before


# Optional

  - install the awesome & free coding font [Anonymous 3][2] (ST3 will try to use it by default)

  - install the [LLVM compiler][3] to have on-the-fly linting for C-language files

     - LLVM v9.0.0 tested OK as of Dec. 2019
     - linting requires per-project configuration fo the EasyClangComplete plugin.
       A guide & template for this will be provided in the future.




[0]:https://www.youtube.com/watch?v=zIkg3Oo1PVM "Youtube link to a nice video on ST3 features"
[1]:https://www.sublimetext.com/ "Sublime Text 3 homepage"
[2]:https://www.marksimonson.com/fonts/view/anonymous-pro "Anonymous Pro font download"
[3]:https://releases.llvm.org/download.html "LLVM compiler download"
