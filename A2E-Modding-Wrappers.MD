<p align="center">
  <img width="250" height="250" src="imgs/a2e-plugin.png">
</p>

# A2E Modding Wrapper (Plugin System)
## The goal of the Modding Wrapper is to allow user customizability to increase productivity and ease-of-use applications.

### Table of contents:

- **Documentation**
- - [FS Wrapper](https://github.com/AstroBP/AstroBP-Docs/blob/main/A2E-Modding-Wrappers.MD#fs-wrapper)
- - [Data Wrapper](https://github.com/AstroBP/AstroBP-Docs/blob/main/A2E-Modding-Wrappers.MD#data-wrapper)
- - [GUI Wrapper](https://github.com/AstroBP/AstroBP-Docs/blob/main/A2E-Modding-Wrappers.MD#gui-wrapper)
- - [Color Wrapper](https://github.com/AstroBP/AstroBP-Docs/blob/main/A2E-Modding-Wrappers.MD#color-wrapper)
- - [Texture Wrapper](https://github.com/AstroBP/AstroBP-Docs/blob/main/A2E-Modding-Wrappers.MD#texture-wrapper)
- - [Sound Wrapper](https://github.com/AstroBP/AstroBP-Docs/blob/main/A2E-Modding-Wrappers.MD#sound-wrapper)
- 
- **Export / Imports**
- - Exporting Your Plugin
- - Importing your Plugin
- - Cross-Compatibility
- - Platform-Specfific Plugins
- - Permissions
- 
- **Debugging**
- - Using The Built-In Console
- - "GDJS Access is not allowed!"


## Documentation

### FS Wrapper

*Note: This Wrapper Requires the `Allow File Operation` Permission.*

<br>

**fs.RequestWrite(FileName, Data)**
| Parameter | Type |
|----------|------|
|FileName | String, File Name|
|Data | String, Data to Write to|
##### Returns `boolean`

<br>

**fs.RequestRead()**
| Parameter | Type |
|----------|------|
| none | none |
##### Returns `string | null`

### Data Wrapper

*Note: This Wrapper Requires the `Allow Data Manipulation` Permission.*

<br>

**data.addBlock(GridSpaceX, GridSpaceY, BlockID)**

| Parameter | Type |
|----------|------|
|GridSpaceX | Integer, Grid Space from 1 - 7|
|GridSpaceY | Integer, Grid Space from 1 - 280|
|BlockID | Integer, BlockID from 1 - 30|
##### Returns `boolean`
<br>

**data.removeBlock(GridSpaceX, GridSpaceY)**

| Parameter | Type |
|----------|------|
|GridSpaceX | Integer, Grid Space from 1 - 7|
|GridSpaceY | Integer, Grid Space from 1 - 280|
##### Returns `boolean`
<br>

**data.clearGrid()**<br>*THIS REQUIRES THE `CLEAR GRID` PERMISSION.*

| Parameter | Type |
|----------|------|
|none | none|
##### Returns `boolean`

### GUI Wrapper

*Note: This Wrapper Requires the `Allow GUI Elements` Permission.*

<br>

**gui.createElement(ID, X, Y, {options})**

| Parameter | Type |
|----------|------|
|ID | GUI Element ID to be set.|
|X | Integer from 0 - 720|
|Y | Integer from 0 - 1280|
|options | Dictionary from GUIOptions|
##### Returns `boolean`
<br>

**gui.option(ID, name, value)**

| Parameter | Type |
|----------|------|
|ID | GUI Element ID to edit|
|name | String, these include<br>BorderColor<br>Style|
|value | Integer / String, these include:<br><br>BorderColor: AstroBlue, AstroRed,<br>AstroGreen, AstroYellow, AstroPurple<br><br>Style: 1, 2, 3|
##### Returns `nothing`
<br>

**gui.onClick(ID, function)**

| Parameter | Type |
|----------|------|
|ID | GUI Element ID to add<br>onlick event listener|
|function | callback function|
##### Returns `nothing`
<br>

**gui.delete(ID, function)**

| Parameter | Type |
|----------|------|
|ID | GUI Element ID|
##### Returns `boolean`


### Color Wrapper

*Note: This Wrapper Requires the `Allow Color Manipulation` Permission.*

<br>

**color.setAstroBlue(R,G,B)**

| Parameter | Type |
|----------|------|
|R | Integer from 0 - 255 which<br>Represents Red Value.|
|G | Integer from 0 - 255 which<br>Represents Green Value.|
|B | Integer from 0 - 255 which<br>Represents Blue Value.|
##### Returns `boolean`
<br>

**color.setAstroRed(R,G,B)**

| Parameter | Type |
|----------|------|
|R | Integer from 0 - 255 which<br>Represents Red Value.|
|G | Integer from 0 - 255 which<br>Represents Green Value.|
|B | Integer from 0 - 255 which<br>Represents Blue Value.|
##### Returns `boolean`
<br>

**color.setAstroGreen(R,G,B)**

| Parameter | Type |
|----------|------|
|R | Integer from 0 - 255 which<br>Represents Red Value.|
|G | Integer from 0 - 255 which<br>Represents Green Value.|
|B | Integer from 0 - 255 which<br>Represents Blue Value.|
##### Returns `boolean`
<br>

**color.setAstroYellow(R,G,B)**

| Parameter | Type |
|----------|------|
|R | Integer from 0 - 255 which<br>Represents Red Value.|
|G | Integer from 0 - 255 which<br>Represents Green Value.|
|B | Integer from 0 - 255 which<br>Represents Blue Value.|
##### Returns `boolean`
<br>

**color.setAstroPurple(R,G,B)**

| Parameter | Type |
|----------|------|
|R | Integer from 0 - 255 which<br>Represents Red Value.|
|G | Integer from 0 - 255 which<br>Represents Green Value.|
|B | Integer from 0 - 255 which<br>Represents Blue Value.|
##### Returns `boolean`
<br>

**color.setGlobalTint(R,G,B)**<br>*THIS REQUIRES THE `GLOBAL TINT` PERMISSION.*

| Parameter | Type |
|----------|------|
|R | Integer from 0 - 255 which<br>Represents Red Value.|
|G | Integer from 0 - 255 which<br>Represents Green Value.|
|B | Integer from 0 - 255 which<br>Represents Blue Value.|
##### Returns `boolean`
<br>

### Texture Wrapper

*Note: This Wrapper Requires the `Allow Sprite Manipulation` Permission.*

<br>

**color.setBlockTexture(ID, URL)**

| Parameter | Type |
|----------|------|
|ID | Integer from 0 - 30 which<br>Represents A BlockID.|
|URL | String that contains<br>a Image URL.|
##### Returns `boolean`
<br>

**color.setBuildGUI(URL)**

| Parameter | Type |
|----------|------|
|URL | String that contains<br>a Image URL.|
##### Returns `boolean`
<br>

**color.setGUISquareTexture(URL)**

| Parameter | Type |
|----------|------|
|URL | String that contains<br>a Image URL.|
##### Returns `boolean`
<br>


### Sound Wrapper

*Note: This Wrapper Requires the `Allow Sound Reproduction` Permission.*

<br>

**sound.playSound(ChannelID, URL)**

| Parameter | Type |
|----------|------|
|ChannelID | Integer from 0 - [MAX_SAFE_INTEGER](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/MAX_SAFE_INTEGER#:~:text=The%20Number.,larger%20integers%2C%20consider%20using%20BigInt%20.])<br>which Represents A GDevelop Sound ChannelID .|
|URL | String that contains<br>a Sound URL (mp3, ogg, wav)|
##### Returns `boolean`

## Export / Imports

### Exporting Your Plugin

Exporting your plugin is as easy as pressing a simple button:

(IMAGE EMBED GOES HERE)

**It will be uploaded to the plugin discovery page, and it will manually be checked and approved.**

###### You may also manually export by copying the code, however, keep in mind that manually importing these plugins could do nasty things!

### Importing Your Plugin

There are 2 Ways on how to import your plugin.

1) Store Discovery, in the "Customization" GUI, there will be a option called "Plug-Ins", Pressing said button will allow you to add the plugins, and look at the source (PC Only!)<br><br>
2) Manual imports, by pressing the "Plug-Ins" Text in the Plugin GUI, there will be a GUI that allows you to copy-paste the code, keep in mind that adding plugins could have security risks as these are escalated by default (for testing reasons)

### Cross-Compatibility

You do not need to worry for any of the included Wrappers, However, if you are using anything that is platform specific, keep in mind that there are other platforms as:

- Cordova
- HTML5
- Electron

### Platform-Specific Plugins
You can make your plugins platform-specific by specifing the following parameter:
```javascript
$PLATFORM=Cordova
```
###### This sets the plugin to only launch in Cordova (Android / iOS Exports)

### Permissions
By reading the documentation, you might have seen snippets of text like **"Note: This Wrapper Requires the `permission_name` Permission."**<br><br>This is so that plugins cannot delete data or do malicious things to a device.<br><br>To enable permissions for a plugin, go to Settings > Customization > Plugins > Installed Plugins, find the plugin you want to edit the permissions for, and toggle the switch for said plugin.

## Debugging

### WIP Section.
