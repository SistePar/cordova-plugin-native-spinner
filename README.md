# cordova-plugin-native-spinner

> Cordova plugin for showing a native spinner based on Paldom/SpinnerDialog

## Installation

**Current state from git**:

* PhoneGap - `phonegap local plugin add https://github.com/SistePar/cordova-plugin-native-spinner`
* Cordova - `cordova plugin add https://github.com/SistePar/cordova-plugin-native-spinner`

## Methods
- `SpinnerDialog.show`
- `SpinnerDialog.hide`

#### SpinnerDialog.show
    SpinnerDialog.show([title], [message], [cancelCallback])

- __title__: Spinner title (Android only). Optional. _(String)_
- __message__: Spinner message. Optional. _(String)_
- __cancelCallback__: Callback to invoke when spinner cancel event fired (tap or Android hardware back button event). If set, spinner dialog will be fixed, you should explicitly call `SpinnerDialog.hide`. Due to legacy reasons you can provide boolean value (true/false) to set spinner not cancelable. Optional, defaults to `false`. _(Function/Boolean)_

#### SpinnerDialog.hide
    SpinnerDialog.hide();

## Usage

```
// Show spinner dialog
SpinnerDialog.show();

// Show spinner dialog with message
// Note: spinner dialog is cancelable by default
SpinnerDialog.show(null, "message");

// Set spinner dialog fixed
SpinnerDialog.show(null, null, true);

// Set spinner dialog fixed with callback
// Note: callback fires on tap events and Android hardware back button click event
SpinnerDialog.show(null, null, function () {console.log("callback");});

// Show spinner dialog with title and message (Android only)
SpinnerDialog.show("title", "message");

// Set spinner dialog fixed (cannot be canceled with screen touch or Android hardware button)
SpinnerDialog.show("title", "message", true);

// Overlay opacity and text color options (IOS only)
SpinnerDialog.show(null,"Message",true, {overlayOpacity: 0.35,  textColorRed: 1, textColorGreen: 1, textColorBlue: 1}); 

// Change only overlay opacity (IOS only)
SpinnerDialog.show(null,"Message",true,{overlayOpacity:0.70});

// Change only text color (IOS only)
SpinnerDialog.show(null,"message",true, { textColorRed: 0.1, textColorGreen: 0.1, textColorBlue: 1});

// Hide spinner dialog
SpinnerDialog.hide();
```

## License
See "LICENSE".
Fork from https://github.com/greybax/cordova-plugin-native-spinner 

