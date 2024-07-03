## 1.5.0 Custom Menu Item Update
 - New feature for modpack curators wanting to inform end users on changes
 - Allows for adding your own main menu item using a rich text file
 - 4 supporting config entries (Enable, Title, Weight, Path)
 - The new .txt file must be in your own /Emblem/ folder
 - An example file has been provided in the defaults folder
 - Theme-able with features from 1.4.0 update
 - Added 2 new config entries for menus
 - Offset will adjust the menu position vertically
 - Height will adjust the spacing of menu items
 - Cleaned up logs & updated readme

## 1.4.5 LobbyCompatibility Compatibility
 - Added LobbyC as soft dependancy
 - Fixed LobbyC icon alignment & visibility in lobby list
 - Increased random delay between logo glitch waves
 - Refactored dynamic recoloring of lobbylist
 - Updated instructions file

## 1.4.4 MoreCompany Flavor
 - Theme color now applies to MoreCompany crewcount
 - Cosmetics button is also recolored
 - Button no longer appears early during init scene
 - Further cleaned up some logs

## 1.4.3 LCBetterSaves Compat
 - When LCBetterSaves is present we will avoid messing with it
 - Cleaned up some log entries

## 1.4.2 This one is for Lunxara
 - Host option highlight is now correctly toggled to 'friends-only' by default

## 1.4.1 Hotfix
 - Fixed default submenu theme color missing alpha value
 - Updated config tips
 
## 1.4.0 The Colorful Update
 - All submenus on the main screen can be custom themed
 - Color palette is calculated from one single config entry
 - Two new boolean configs added to the Menus section
 - Re-using menu colors on submenu buttons is optional
 - Essentially an entire new mod within a mod 
 - This is being released with some minor known compatability bugs
 - Submenu coloring doesn't currently support live updates to cfg

## 1.3.2 Fixes
 - Fixed live changes not working on glitched logo
 - Fixed submenus stopping glitched logo animations
 - Dialed back scaling on retro TV effect to fix mouse positioning

## 1.3.1 New features
 - Added new config option for Left/Center/Right version alignment
 - Added experimental glitchy logo effect
 - Updated readme

## 1.3.0 Live Config Changes
 - Any config changes will now be applied without restart
 - Use any config editor, even notepad
 - Please report any bugs, extensive testing needed
 - Fixed typed text not working on second game load
 - Fixed scanline shader obscuring other plugins ui objects
 - Added feature, press \ key to preview loading screen
 - Slideshow transitions are no longer optional
 - Added a config file dispatcher/watcher to track cfg changes
 - Added unique names to repeatedaction coroutines
 - Refactored classes to use event listeners
 - Original headers are now hidden instead of replaced
 - Loadtext now starts its own object and doesn't touch the original
 - Video and image backgrounds now use the same container
 - Refactored MediaManager into singleton pattern
 - Fixed loading screen BG colors
 - Made some config descriptions clearer
 - Cleaned up logs
 
## 1.2.8 Bug fixes
 - Made loading text more readable using magic
 - Improved coroutine performance
 - Fixed bug where coroutines continued to run in main game

## 1.2.7 Loading Text Effects
 - Loading text can now be swapped on the slideshow timer
 - Loading text can now appear to be typed out
 - Retro TV effects now work on opening scenes
 - Added log header ascii bar
 - Fixed some naming rule breakers
 - Refactored header replacement again, better but still messy

## 1.2.6 Slideshow Transitions
 - Added animated slideshow opacity fade over time
 - Added config option to enable transitions
 - Adjusted random image selection to not use the same image twice in a row
 - Added config option for transition time
 - Made slideshow reuseable on various objects
 - Refactored configurator & delayhelper into singleton patterns
 - Reorganized header replacement methods to make sense
 - Renamed some gameobjects for sanity

## 1.2.5 New Features
 - Added scanlines as an embedded shader, setting is in experimental section
 - Added slideshow to rotate any image section when setup to be random
 - Cleaned methods that weren't checking if they already existed
 - Cleaned some debug log entries, fixed class prefix's

## 1.2.4 The TV Update
 - New experimental Retro TV styling for entire main menu scene
 - Camera volume masking fix for more company compatability

## 1.2.3 Media Path Refactor
 - Added caching to improve performance of repeated path queries
 - Fixed path processing to accurately handle nested Emblem folders
 - Removed padding for LobbyHost and LobbyList for consistency
 - Moved corner layer behind popup menus and version number
 - Refined de-borking log entries into one
 - Removed sub-menu corners as they were doubled up with custom ones
 - Darkened transparent menus over background images for readability

## 1.2.2 Oops
 - Missed one important detail in config path descriptions

## 1.2.1 Simpler Paths
 - Added new path conversion mechanism to help with confusing instructions!
 - We now search for the plugins/\*/Emblem/ folder that contains your files
 - Custom Themes or ModPacks all need a 'BepInEx/plugins/Emblem' folder
 - Configs use something like Myfolder/BackgroudFlyingDolphins.png and it will work
 - Instructions and readme have been updated
 - Moved instructions to plugin root for acessability
 - Apologies for the convoluted treasure hunting
 - Backwards compatible
 - Updated config path defaults

## 1.2.0

 #### Asset location changes
 - Profile codes were attempting to move images and videos which exceeded the 20mb limit
 - Emblem won't use the BepinEx/config folder anymore for media
 - Image & video paths must now be relative to BepInEx/plugins
 - Please PLEASE read new instructions at Darkbrewery-Emblem/Defaults/EmblemInstructions.md
 - After following directions, if you still need assistance, check into the discord channel
 
 #### Config updates
 - Reorganized config options for my sanity, sorry folks but you will have to rebuild your cfg's
 - Header logo has some new default settings
 - Removed canvas recoloring config
 - Removed loading text wrap config
 - All config descriptions are less verbose
 
 #### New config features
 - Added transparency option for loading images
 - Added scale option for loading images
 - Added option to use different png's & mp4's as loading screen background
 - Added option so mp4's can be picked randomly if listed paths are separated by |
 - Added option so main and Loading logo paths can be left blank to use no image at all
 - Added main & loading background color options instead of global canvas color
 - Added experimental vignette to blend background images with background colors
 - Added padding config for borders

 #### Fixes
 - Fixed loading images not respecting vertical y-offset config
 - Fixed loading screen being zoomed slightly closer than main menu
 - Fixed stretch loading image not properly overriding scale and offset
 - Reset rectransform on more objects for overall layout consistency

 #### Code changes
 - Major code refactoring
 - Moved background management to its own class
 - Expanded the color parser helper to accept RGB and RGBA
 - Some method names are now less verbose
 - Changed up some default backgrounds
 - Lots of small things I forgot to add to the changelog
 - Configurator has been cleaned for readability
 - Update Readme


## 1.1.6
 - Fixed ultrawide backgrounds being squished
 - Fixed mp4s not using master audio volume settings
 - Adjusted png texture conversion
 - Cleaned up some global constants
 - Removed some default images and compressed logo
 - Light code refactoring

## 1.1.5
 - Fixed mp4 videos restarting when opening submenus
 - Fixed the vanilla sticky menu item highlighting bug
 - Enabled audio track playback from mp4's
 - Backgrounds now persist within menus
 - Added background layers for readability
 - Renamed some new Emblem gameobjects

## 1.1.4
 - Configs configs configs
 - Added version number formatting, 4 new configs!
 - Replaced center loadingtext config with a Y-offset config
 - Edited some config texts
 - Updated readme

## 1.1.3
 - Fixed video pausing when entering menus
 - Fixed borders hiding behind video layer
 - Fixed menu colors not applying transparency alpha
 - Added logs to moodsetter
 - Simplified new GameObject names
 - Cleaned up global constants, more specific

## 1.1.2
 - Hotfix for videos blocking view of the loading screen

## 1.1.1
 - Added option to use mp4 for video background instead of png
 - Fixed flicker of menu colors on first load

## 1.1.0
 - Diving into menu recoloring
 - Added config options to change menu colors
 - Sortof fixed glitchy menus by disabling animations and replacing with triggers
 - Added delay helper for lethalconfig compatability
 - Updated config tooltips

## 1.0.9
 - Added config option to change the border coloring
 - Refactored the border methods, both screens have the same placement now
 - Logwarden has stopped all the loggers from arguing
 - Moved pathfinder probe to it's own home, centralizing the helper
 - Cleaned up some code and logs

## 1.0.8
 - Replaced header and loading image centering with % Y offset
 - Reset container elements to fix vanilla borked object spacing
 - Fixed broken stretch loading image feature
 - Adusted menu borders
 - Improved UI element searching
 - Updated readme

## 1.0.7
 - Added ability to use multiple loading text messages and have 1 randomly chosen
 - Added config entry for canvas recoloring on/off to keep this as modular as possible
 - Refactored scenemanagement, imagereplacement, loadingtext, simplified code
 - Created some helpers, reduced duplication
 - Prefixes on logs to help diagnose future issues
 - Removed unused baseclass, organized namespace
 - Updated readme

## 1.0.6
 - Preparing for more plugin complexity..
 - Update log entries to be more clear, removed rendundant ones
 - Reorganized code and cleaned up unecessary comments
 - Refactored to use constants from Emblem namespace within classes
 - Added a ColorParser class for improved code consistency

## 1.0.5
 - Set custom background default to true so users see it working right away
 - Added option to change color of canvas behind the background

## 1.0.4
 - Updated docs
 - Reworded config options for useability
 - Image path configs are now relative to BepInEx folder
 - Updated default paths
 - Compressed included sample images
 - Updated prefix method to fallback on any random png if the prefix isn't present at all before throwing an error
 - Paths in logs now properly show BepInEx as path root

## 1.0.3
 - Re-organized paths again, lets see how this goes
 - Added prefix support
 - Updated docs

## 1.0.2
 - Since thunderstore is squishing folder paths, we will point to .pngs directly for now, updated defaults

## 1.0.1
 - Fixed default paths
 - Added a couple more generic background images

## 1.0.0
 - Initial Release