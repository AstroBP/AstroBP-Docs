<p align="center">
  <img width="250" height="250" src="imgs/a2e-plugin.png">
</p>

# A2E Modding Wrapper (Plugin System)
## The goal of the Modding Wrapper is to allow user customizability to increase productivity and ease-of-use applications.

### Table of contents:

- **Documentation**
- - FS Wrapper
- - Data Wrapper
- - GUI Wrapper
- - Color Wrapper
- - Texture Wrapper
- - Sound Wrapper
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
