bAutoSize
=========
## What
jQuery plugin that resize elements at window resize.
Build to escape CSS problems and cross browser compatibility issues.

## Why
It can be used to resize elements (images, text boxes, etc) relative to window or its DOM parent.
The element can be restrict to a specific width/height proportion, or to have minimum and/or maximum values.

It was originally designed to make a full screen multi canvas (html5) application with multiple layer canvases.

Other applications : 
* background image of your website (absolute or fixed positioned) "stretch" or "fit" like
* multi browser implementation of "fluid layout" of any website
* make one (more) or all elements of a layout to "auto fit" to window
* canvas or JavaScript games
* etc. .. your imagination is the limit ..

To manual control the plugin (not auto trigger at window resize) see "manual.autosize.html" example.

## About
 * version 0.3 - 12.07.2012
 * since 07.07.2012
 * author B.G.Adrian
 * website http://btools.eu
 * license MIT License
 * source https://github.com/BTooLs/bAutoSize
 
### Settings
 
**parent** : dom element or jquery selector.
	Default value : $(container).parent()
	
**trigger_at_load** : boolean, if true the first resize is done at page load.
	Default value : true
	
 **trigger_minimum** : min px for difference at resize to trigger the resize.
	Default value : 20
	
 **width_offset** : pixel integer value, take from the parent size width.
	Default value : 0
	
 **height_offset** 
	Default value : 0
	
 **width_perc** : percent of available space that the element will occupy. Values starting from 0.1 (10%).
	Default value : 1 (1 = 100%)
	
 **height_perc** :
	Default value : 1
 **minimum** false or object with minimum a sizes in pixels.Examples : "false", "{w : 300, h : 200}", "{h : 600}".
	Default value : false
	
 **maximum** Works same as minimum.
	Default value : false
	
 **height_proportion** boolean or > 0.1 value to keep the height proportional of width. 
 		Examples : "0.5" means that the height will always be half of the width. "2" will be twice as big.
 			True (or 'auto') will let the plugin calculate the proportion. False to disable it.
	Default value : false
	
 **callback**  Function that will be called after each resize. No paremeters are sent (int this version).
	Default value : null
	
**callback_env** Invocation value of the callback (enviroment). Ex "callback : window.myObj.refresh, callback_env : window.myObj".
	Default value : window
	
 **resize_children** Force sizes on all element childrens too.
	Default value : false
	
 **debug** Debug data sent to javascript console.
	Default value : false
	
#### Changelog

v.0.3 12.07.2012
* added lock and unlock methods
* added rollback method
* added : image examples
* changed the way that methods are called
* bugfix : methods were called without context (thisArg)
* modified : height_proportion now supports 'auto' (true) value
* modified : debug messages now has prefix "[bautosize]"