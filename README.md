SublimePaneNavigation
=====================

"SublimePaneNavigation" is a plugin for the Sublime Text 2 editor that provides increased keyboard navigation between tabs and split panes (when using multiple split panes in a window). This plugin primarly does 3 things:

1. **Tab Navigation:** Changes the `ctrl+tab` and `ctrl+shift+tab` key bindings to cycle through the tabs in the **active pane** in the order that they appear in the pane (as opposed to in order of recency, as is the default); note that this is unlike the built in behavior for `cmd+shift+]` and `cmd+shift+[` for a mac (`alt+shift+]` and `alt+shift+]` for Windows or Linux), which cycle through the tabs in the active window, across all split pane.
2. **Split Pane Navigation:** Adds key bindings for `ctrl+]` and `ctrl+[` to cycle through the multiple split panes open in a window (if there are multiple split panes).
3. **Sending Tabs To Other Panes:** Adds key bindings for `ctrl+shift+left` and `ctrl+shift+right` to send tabs from their current pane to the next/previous panes (if there are multiple split panes in a window).


## Installation

### By Package Control

1. Download & Install **`Sublime Text 3`** (https://www.sublimetext.com/3)
1. Go to the menu **`Tools -> Install Package Control`**, then,
    wait few seconds until the installation finishes up
1. Now,
    Go to the menu **`Preferences -> Package Control`**
1. Type **`Add Channel`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    input the following address and press <kbd>Enter</kbd>
    ```
    https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
    ```
1. Go to the menu **`Tools -> Command Palette...
    (Ctrl+Shift+P)`**
1. Type **`Preferences:
    Package Control Settings – User`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    find the following setting on your **`Package Control.sublime-settings`** file:
    ```js
    "channels":
    [
        "https://packagecontrol.io/channel_v3.json",
        "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
    ],
    ```
1. And,
    change it to the following, i.e.,
    put the **`https://raw.githubusercontent...`** line as first:
    ```js
    "channels":
    [
        "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
        "https://packagecontrol.io/channel_v3.json",
    ],
    ```
    * The **`https://raw.githubusercontent...`** line must to be added before the **`https://packagecontrol.io...`** one, otherwise,
      you will not install this forked version of the package,
      but the original available on the Package Control default channel **`https://packagecontrol.io...`**
1. Now,
    go to the menu **`Preferences -> Package Control`**
1. Type **`Install Package`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
    search for **`PaneNavigation`** and press <kbd>Enter</kbd>

See also:

1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


Usage
-----
There are four key bindings associated with this plugin (note that in the descriptions, "next" and "previous" refer to the order in which the tabs/panes appear in the window, not based on recency as is the default in Sublime Text 2):

* `ctrl+tab`: cycle to the next tab in the active pane
* `ctrl+shift+tab`: cycle to the previous tab in the active pane
* `ctrl+]`: cycle to the next pane in the active window
* `ctrl+[`: cycle to the previous pane in the active window
* `ctrl+shift+left`: send the current tab to the next pane in the active window
* `ctrl+shift+right`: send the current tab to the previous pane in the active window

Configuring
-----------
If you would like part of the available functionality (for example, if you only want the split pane navigation), simply comment out the key bindings for the unwanted functionality. Additionally, if you would like to change the key bindings, simply edit the "Key Bindings" file available in the preferences menu: `Preferences->Package Settings->Pane Navigation->Key Bindings - Default`.
