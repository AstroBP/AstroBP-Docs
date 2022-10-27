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
