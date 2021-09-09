# TP_VTS

[![Twitter Follow](https://img.shields.io/twitter/follow/wiccy84.svg?style=social)](https://twitter.com/wiccy84) 
[![Twitch](https://img.shields.io/twitch/status/wiccy84?style=social)](https://www.twitch.tv/wiccy84) 
[![Youtube](https://img.shields.io/youtube/channel/views/UCjd9Mee-jdZOHtpEF0KrdWg?style=social)](https://www.youtube.com/c/WiccyNeet/videos)<br><br>
This is a plugin for using Vtube Studio with Touch Portal <br>

## Installation

Grap the latest release of TP_VTS from [releases](https://github.com/Wiccy84/TP_VTS/releases).
In Touch Portal click on the cog in the top right, then click on plug-ins on the left. Now click on Import plug-in and navigate to where you downloaded TP_VTS.tpp and click open and then OK. You should now see a warning that you have installed a plugin that you have not trusted yet click Trust Always to not get the warning again or Ok to pass the warning once. Clicking No will not allow the plugin to work.

If it is not already loaded, load Vtube Studio. Once loaded the plugin should attempt to connect to VTS. The first time it does this you will get a pop up asking you if you would like to let the plugin access VTS. If this does not happen open the settings of VTS and make sure the API is on and the port is set to 8001. Once you see the pop up click allow and the authentication key will be saved for next loads. You can revoke this permissions anytime in VTS by going into the settings and clicking on remove plugins and selecting "Touch Portal - VTS Plugin" and clicking select.

## Usage

Currently this plugin adds six actions to Touch portal for use with VTS.

**Load Model** -  on load of Touch Portal and connection to VTS this is populated with a list of all models currently accessable to VTS. Use the drop down list to select a model to load. (This list currently can only be updated by stop/start the plugin or restarting TP itself.)

**Move Model** -  This action is to move your model around! There are six paramaters for this action
* Time(s)
  * Time to travel in seconds from origin to the paramaters you input. min = 0, max = 2, **Example - Time(s): 0.5.**
* Relative
  * If movement is done from 0,0 or from where the model currently is. True is from 0,0 and False is from models current posistion.
* X
  * This is the movement of the left and right plane. A negative number will go left and a positive number will go right. -1 and 1 are the edges of the screen but you can input a max of -1000, 1000. **Example - X: 0.5**
* Y
  * This is the movement of the up and down plane. A negative number will go down and a positive number will go up. -1 and 1 are the edges of the screen but you can input a max of -1000, 1000. **Example - Y: -0.2**
* Rotation
  * For Rotating your model negative number will turn counter clockwise and positive will go clockwise. min = -360, max = 360, **Example - Rotation: -90**
* Size
  * The size of your model displayed. A negative number will make smaller and a positive number will make larger. min = -100, max = 100, **Example - Size: -75**

![coordinate_explanation](images/coordinate_explanation.png)

**Run Hotkey** - For executing any hotkeys you have made for the current model. Just fill in the field with the name of the hotkey.

**Tint All Art Mesh** - For tinting your whole model. Click on the drop down box, this will show a swatches palette. You can pick from them or click custom colours which will open a colour picker window to pick any colour you want and change the opacity as well. **White = default model colour**.

**Tint Art Mesh** - This has the same colour picker from "Tint All Art Mesh" but with optional paramaters to add. All fields can contain multiple paramater inputs seperated by a comma and a space i.e. ", "

* Mesh Number
  * For tinting a mesh via its number. This is the number of meshes location in the array (It does not correspond to the number at the end of an artmesh name). **Example - Mesh Number: 0, 25, 100**
* Name Exact
  * For tinting a mesh with the exact name you input. **Example - Name Exact: HairLeft1, HairRight2, artMesh99**
* Name Contains
  * For tinting all meshes that contain what you input in its name. **Example - Name Contains: Hair**
* Tag Exact
  * For tinting all meshes within the exact tag you input. **Example - Name Exact: HairLeft, HairBack**
* Tag Contains
  * For tinting all meshes within all tags that conatian what you input. **Example - Name Exact: Clothing**

**Display Model Data** - This will gather all relevent model data you might need for this plugin and save it as a txt file in TP_VTS plugin folder. Once it has compiled that data it will open it automatically for you to read. **You should NOT run this in a button that you will use often. It is only for information gathering to be used by you in the other actions.**

