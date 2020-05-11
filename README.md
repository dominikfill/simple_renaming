<h2>Introduction</h2>

<p><b> Simple Renaming Panel </b> is a small, but really powerful tool to rename more objects at once. The tool includes basic functionalities of adding suffixes, prefixes, search and replace, add suffixes depending on the object type and much more. You decide which kind of objects will be effected by the renaming task, all or just selected objects, should it affect image textures, materials, objects, object data, bones or groups. This tool can be a real everyday helper as renaming multiple objects is needed very often and keeping the naming conventions can be tedious. The tool provides you with a clear feedback of what has been renamed. This tool is kept simple to be user friendly but offers everything you need to stay organized. </p>

<h3>Download and Installation</h3>

You can download the Simple Renaming Panel for blender 2.79 and blender 2.80 from the releases section <a href="https://github.com/Weisl/simple_renaming_panel/releases" target="_blank">here</a>.
Like any other Add-on, you can simply install it by going to <b> File &gt; User Preferences &gt; Add-ons </b> and click at the button <b>Install from File </b>. In the new opened window choose the .zip file of the addon and press <b>Install from file </b>.
<b>The Simple Renaming Panel</b> should now appear in your add-ons window and can be activated.

<img src="img/install_addon.jpg" alt="Installation Addon " />


<h4>Simple Renaming Panel</h4>

<img src="img/mainPanel.jpg" alt="Installation Addon " />
<ul>
	<li> Choose which kind of objects you want to rename:</li>
	<li> Changes effect selected or all</li>
	<li> Replace names with a new name</li>
	<li> Search and replace </li>
	<li> Match case for the search and replace</li>
	<li> Add prefixes </li>
	<li> Add suffixes </li>
	<li> Numerate objects</li>
	<li> Trim string </li>
	<li> Data: Keeping the object data names clear and organized can be really painful in blender, this button simply renames the data according to the objects and adds a specified suffix.</li>
</ul>

<h4>Key Feature:</h4>

<ul>
	<li>Works for objects, materials, collections, image textures, object data and bones</li>
	<li>Choose if all or just selected objects should be effected </li>
	<li> Restrict renaming operation to specific object types (meshes, curves, empties, cameras, metaballs, lightprobes, volume objects etc.) </li>
	<li>Search and replace </li>
	<li>Match case option for search and replace</li>
	<li>Regex Support</li>
	<li>Add suffixes and prefixes</li>
	<li>Numerate </li>
	<li>Trim names</li>
	<li>Rename object data after object name</li>
	<li>Add suffixes  or prefixes by specific object types </li>
	<li>Simple and clean UI</li>
	<li>Customizable UI position</li>
	<li>Auto updater</li>
</ul>
<h4>Improved Basic UI</h4> 
I have improved the UI based on the input from Bookyakuno. This makes it easier to use, while keeping the efficiency from before. 

<h4> Advanced UI (Experimental) </h4> 
You can specify the number of leading zeros next to the new name input. Every # represents one 0. You can also disable the automated numeration completely. This is especially useful for the newly introduced variables. Additional Buttons allow you to easily add these variables and show you which ones are available for this renaming process. This UI is still WIP. 

<h4> Renaming Variables (Experimental)</h4> 
 
The biggest new feature are the renaming variables. They expand the functionality of the renaming panel drastically while keeping it fast and efficient. Variables are defined by the @ symbol. This is because other typical symbols like $ are already used for Regular Expressions. The variables can be generated by either press the button next to the input field or simply type it in. The current variables are:
<ul>
<li>	@f : filename</li>
<li>	@h: high poly (user defined, default = high)</li>
<li>	@l: low poly (user defined, default  = low)</li>
<li>	@c: cage (user defined, default  = cage)</li>
<li>	@d: date </li>
<li>	@u1: (user defined)</li>
<li>	@u2: (user defined)</li>
<li>	@u3: (user defined)</li>
<li>	@i: time</li>
<li>	@n: number </li>
<li>	@r: random</li>
</ul>
Currently only supported in Object mode

<ul>
<li>	@p: object parent (if it has one)</li>
<li>	@o: object</li>
<li>	@a: active object</li>
<li>	@t: type </li>
</ul>
An arbitrary number of renaming variables van be used in any input field and at any position. Variables can be combined and used together with regular strings. 

E.g., 
@f_@t_object_@i  ([filename]_[objecttype]_object_[time]_[number]). Furthermore, it is now possible to deactivate the number at the end of newly generated names.

Note: 
Be careful by using the renaming variables in the Search input. It will only compare the strings. If you use the date variable @d it will only find the objects that have the current date and the same format. 

By deactivating the Numeration and using the custom number variable @n. It is finally also possible to rename many objects at once with a increasing number in the middle of the string. 

E.g., objeckt_001_high,  objeckt_002_high. objeckt_003_high. 
This can be useful for baking multiple high poly object onto one low poly object within marmoset or substance. 

<h4>Bone Renaming in Edit Mode</h4> 

Bones can now be renamed in the edit mode and the mode won’t change to pose mode. 

<h4> Search and Select </h4> 
The search can now be used to select objects. This uses works with the settings for renaming like only effecting selected and objects of a certain type. This feature works for object renaming as well as bone renaming in pose mode. 

<h4> Presets for the Prefix/Suffix by Type Panel </h4> 
The presets allow you to easily save different naming conventions for different object types and switch quickly between them.

<h4>Known Issues: </h4> 

•	Time: Ignores the current time zone and uses always Coordinated Universal Time (UTC)
•	The Category Tab in the preferences does not work 
•	The selection order is still ignored 
•	Be really careful with using @p and 

<h4>Future:</h4> 

•	Test the renaming variable system further and handle more edge cases for the individual variables.
•	Improve the operation and variable descriptions 
•	Improve the UI for selecting variables with different columns similar to the Editor Type dropdown
•	Add more user defined variable slots
•	Add and special variables for other renaming modes (e.g., especially for textures and actions)
•	Remove duplicate code for the simple and advanced UI
•	Refactor the code for adding new renaming variables 
•	Add a Search and Select functionality
•	Add specialized renaming operators. (Baking Pair)
 

<h4>Type Suffix Prefix</h4>

<img src="img/sufPrebyTypePanel.jpg" alt="Installation Addon " />
<ul>
	<li><b>[NEW]</b> Choose betweeen Suffix and Prefix</li>
	<li>Geometry: all meshes</li>
	<li>Material: all materials</li>
	<li>Empty:  all empty objects </li>
	<li>Curve: all curves</li>
	<li>Armature: all armatures objects (not bones)</li>
	<li>Group: all groups</li>
	<li>Lattice: all lattices</li>
	<li>Data: all object data</li>
	<li><b>[NEW]</b> Surfaces: all surface objects</li> 
	<li><b>[NEW]</b> Cameras : all cameras </li>
	<li><b>[NEW]</b> Lights: all lights </li>
	<li><b>[NEW]</b> Bones: all bones </li>
</ul>

<img src="img/popup.jpg" alt="Installation Addon " />

<h3>Release Notes</h3>

<h4>[1.5.0] blender 2.80 beta</h4>

<h4>[1.4.1] blender 2.80 beta</h4>
<ul>
<li> [Fix]: Renaming only selected Bones in Object mode shows now an info that selected bones can only be renamed in object mode.</li>
<li> [Fix]: Improved Error handling</li>
<li> [Fix] Duplicate popup window is not shown in the tools panel anymore.</li>
</ul>

<h4>[1.4.0] blender 2.80 beta</h4>
<ul>
<li><b>[NEW]</b> Feature: Introduction of the powerful renaming variables </li>
<li><b>[NEW]</b> UI: Toggle between simple and advanced UI</li>
<li><b>[NEW]</b> Presets for rename by type</li>
<li><b>[NEW]</b> Search and select for Object renaming </li>
<li> [Fix] Bone renaming in Pose mode </li>
</ul>

<h4>[1.3.1] blender 2.80 beta</h4>
<ul>
<li><b>[NEW]</b> UI: User Defined Hotkeys </li>
<li><b>[NEW]</b> UI: Add additional options to the User Preferences of the addon</li>
</ul>

<h4>[1.3.0b] blender 2.80 beta</h4>

<ul>
<li><b>[NEW]</b> UI: The simple renaming panel is now part of the properties panel </li>
<li><b>[NEW]</b> UI: The panel uses for big parts the single column layout </li>
<li><b>[NEW]</b>The codebase was updated to fit the new requironments of blender 2.80 </li>
<li><b>[NEW]</b>The new blender 2.80 specific object types are supported (e.g., grease pencil, lightprops). Groups and Layers have been removed from the addon. </li>
<li><b>[NEW]</b> An option to provide more control over which object type is effected by the renaming action was added. </li>
<li><b>[NEW]</b> It is possible to rename selected bones (Thanks to  <a href="https://github.com/cube-creative">Cube Creative</a>) </li	
</ul>

<h4>[1.3.0a] blender 2.80 alpha</h4>

<ul>
<li>[DELETED] Renaming of Collections </li>
<li>[DELETED] Renaming of Render Layers </li>
<li>[DELETED] UI Popup </li>
<li>[CHANGED] Tool panel to Properties panel </li>
<li> [FIXED] This addon can't be installed from the zip file. </li>
</ul>

<h4>[1.2.0]</h4>

<ul>
	<li>[NEW] Renaming works now in different modes: object, material, image texture, group, data and bone </li>
	<li>[NEW] Change the tool shelf category of the add-on in the preferences </li>
	<li>[NEW] Added a match case checkbox has been added to search and replace</li>
	<li>[NEW] A simple and well organized information panel lists which objects have been renamed and includes some additional information </li>
	<li>[NEW] Not only suffixes, but also prefixes can be added by object type</li>
	<li>[CHANGED] Suffix by type has been renamed to type suffix and prefix panel and is now part of the main panel</li>
	<li>[NEW]Surfaces, cameras, lights and bones have been added to the type suffix and prefix panel</li>
	<li>[UPDATED]Auto updater 1.0.3</li>
	<li>[FIX] A lot of minor bugs have been fixed</li>

</ul>

<h4>[1.0.1]</h4>

<ul>
	<li>[New] The posibility to give the objects a new name has been added</li>
</ul>

<img src="img/simplePanel_title_01.jpg" alt="Teaser Banner " />
<img src="img/simplePanel_title_02.jpg" alt="Teaser Banner " />
