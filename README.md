# EditorIconMaker

This tool was made for capturing Satisfactory-style screenshots for use as item or building icons.
 
## Install Instructions:

1. Download and unzip the repo OR clone it to the Plugins folder of your mod's project folder.
2. Open up the Editor and use a Content Browser to navigate to the "NogsIconMaker Content" plugin content folder.
3. Open the IconGameLevel level from the content browser.
	* If the Editor crashes, go to Edit > Project Settings... and then pick "Maps & Modes" from the Project subheading. Under "Default Maps", set the "Editor Startup Map" and "Game Default Map" to the IconGameLevel level from before.
4. Use the World Outliner window to select the IconCaptureActor present in the level. In the "Details" window, set the propert "Desc" under the Default caregory to the Descriptor you want to make an icon for. 5. Click the "Load Descriptor" button, which is above the Desc field, to load the item into the scene. You should see the item's mesh appear inside the Level viewport.

All of the settings related to the icon capture are loaded from the Descriptor you selected, and then the values are set on the IconCaptureActor. Adjust your settings until you are happy.

* Some of the settings may load in to be 0, and will need to be changed to result in a good icon. To move your mesh properly into view, use a positive X axis Location setting. Set the MainLight Intensity to 3 and the Sky Light Intensity to 1 for best results.
* To create an icon file, click one of the 'Snap' buttons (64-2k) depending on what resolution icon snap you want the take. These buttons are in the Default category. You can click the popup that appears to open the folder where the icon file was taken.
* Optionally, save your Descriptor Settings in the descriptor by clicking the "Save Descriptor" button. (You may have to mark the BP as changed and save it manually for this to work)

## Snap On Play: 

You can automate the process of making (or retaking) icons in bulk with the "Snap On Play" array property in the Automation section. When you Play the level, descriptors in this array will be cycled through and icons will be snapped of them in the sizes you checked in the Texture Creation section.

## Buildings : 

For buildings, the ChildActor component will be used for the snapshots instead of a Mesh component.


## Troubleshooting: 

* To view 1:1 what you will get out when Snapping a Picture, set your Viewport to use the IconCaptureActor Camera.
* When ever you Snap a Picture and your Viewport adjusts itself, your view wasnt properly framed. 
* Snapping a Picture may Reset the Viewports Camera, while maintaining the Transform.
* Problems may vary depending on your Viewport Settings, Windows or Project Resolution Scaling etc..
