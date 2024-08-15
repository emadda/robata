# Robata

Put it on the grill.

Robata is a window selector app for macOS.

[Download for macOS](https://github.com/emadda/robata/releases/download/v-001/Robata-001.dmg).

Please [report any issues or feedback you have](https://github.com/emadda/robata/issues).

You can also contact me at [enzo@robata.app](mailto:enzo@robata.app).


Learn more: [robata.app](https://robata.app).

# Keyboard shortcuts

- z
	- Zoom.
	- If you hover over a window the zoom is centered there, otherwise the closest image center is used.

- c
	- Close window currently under mouse.

- cmd-d
	- Discover windows.
	- Window discovery only needs to be one when Robata first opens.
	- macOS window APIs only allow reading windows that have been on an active space.
	- Spaces can only be switched to when an app focuses on one of its own windows on that space.
	- To find all your windows, this creates a small window on each space, visits each space, and then closes.
	- It should take around 10 seconds.
	- Or you can manually switch to different spaces instead.


# Custom methods of opening

By default the bottom left of any attached trackpads open Robata. You just need to rest your finger lightly (no tap needed).

You can customize this via File -> Settings.


You can attach your own keyboard or mouse shortcuts to toggle Robata using any of these methods:


- Via the .app file.

```
# Toggles the UI.
open /Applications/Robata.app
```


- Custom URL schemes.

```
robata://show
robata://hide
robata://toggle
```

Used in a shell script:
```sh
#!/bin/sh
open "robata://toggle"
```


- Tap the Dock icon.
- Apple Shortcuts.
- `Settings ▶ Keyboard ▶ Keyboard Shortcuts... ▶ App Shortcuts ▶ Add Robata` 
- Alt-tab.




# Permissions

Robata requires:

- Settings -> Privacy & Security -> Accessibility 
- Settings -> Privacy & Security -> Screen & System Audio Recording


Drag and drop the app onto these lists and enable the toggle.

It only uses the screenshot API whilst the UI is being viewed. Accessibility is required for access to window titles, sizes and to the trackpad.


# Security: Apple Notarized

Robata is [notarized](https://developer.apple.com/documentation/security/notarizing_macos_software_before_distribution) by Apple, which has the following benefits:

- It has been scanned and verified to be malware free.
- The app cannot be modified in any way, so the code that was checked by Apple is the code that runs.
- The developer ID is verified.
- Apple can remotely disable any apps found to contain malware in the future.

Robata does not access the network or disk whilst it runs.




