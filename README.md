# Sleepy Utilities

A general purpose library that you can use in Solar2D projects with minimal modification.

## Usage instructions
**Import library**
```sh
local utils = require "utils"
```

**Create slider widget**
```sh
utils.createSliderControl(targetGroup, optionsSliderControl)
```

**Close databases**
```sh
tableDatabases = utils.closeDatabases(tableDatabases)
```

**Close files**
```sh
tableFiles = utils.closeDatabases(tableFiles)
```

**Resume timers**
```sh
utils.resumeTimers(tableTimers)
```

**Pause timers**
```sh
utils.pauseTimers(tableTimers)
```

**Cancel timers**
```sh
tableTimers = utils.cancelTimers(tableTimers)
```

**Clear display group**
```sh
utils.clearDisplayGroup(targetGroup)
```

**Clear table**
```sh
targetTable = utils.clearTable(targetTable)
```

**Create slider widget**
```sh
local widthSoundButton = contentWidthSafe / 10
local heightSoundButton = widthSoundButton
local ySoundSlider = yStartingPlacement + heightSoundButton * 1.2

local optionsSliderControl = { id = "soundLevel", filePath = "assets/menu/sound.png", 
    colorBackground = colorBackground, colorButtonDefault = colorButtonDefault, 
    colorButtonFillDefault = colorButtonFillDefault, colorButtonFillOnPress = colorButtonFillOnPress, 
    colorButtonStroke = colorButtonStroke, widthButton = widthSoundButton, heightButton = heightSoundButton, 
    yButton = ySoundSlider, soundSample = tableSoundFiles["answerChosen"] }
local buttonSound = utils.createSliderControl(targetGroup, optionsSliderControl)
```

**Show information box**
```sh
local optionsInfoBox = {
    infoFont = fontName,
    infoText = "Information text shown to the player/user",
    isPromptAvailable = isDontShowAgainPromptShown,
    stringPromptPreference = variableStringDontShowAgainPreference,
}
local yTopFrame = utils.showInformationBox(infoGroup, optionsInfoBox)
```

**Show dialog box**
```sh
local function closeDialogBox()
    ...
end

local function openURL()
    ...
end

local optionsDialogBox = {
    fontDialog = fontName,
    dialogText = "This will take you to www.github.com.",
    confirmText = "Confirm - Open URL",
    confirmFunction = openURL,
    denyText = "Deny",
    denyFunction = closeDialogBox,
}
utils.showDialogBox(dialogGroup, optionsDialogBox)
```

**Load sound effects**
```sh
local tableSoundFiles = {}
local pathFolder = "assets/soundFX/"
local tableFileNames = { "answerChosen.wav", "answerRight.wav" }

tableSoundFiles = utils.loadSoundFX(tableSoundFiles, pathFolder, tableFileNames)
```

**Unload/free sound effects**
```sh
tableSoundFiles = utils.unloadSoundFX(tableSoundFiles)
```

**Show share UI(OS dependent)**
```sh
local urlLandingPage = "www.YourLandingPageHere.com"
local pathShareAsset = "assets/other/shareAsset.png"

utils.showSystemShareUI(pathShareAsset, urlLandingPage)
```

**Show QR code to a web page**
```sh
local pathQRCode = "assets/other/QRCode.png"
utils.showShareQR(qrGroup, pathQRCode)
```

**Show mail UI(OS dependent)**
```sh
local mailAddress = "user@xyz.com"
local mailSubject = "Enter mail subject here"
local mailBody = "Enter mail body here"

utils.showMailUI(mailAddress, mailSubject, mailBody)
```

**Show store page**
```sh
local idAppStore = "1234567890"
utils.showRateUI(idAppStore)
```
