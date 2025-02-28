=== OpenMenu - The official plugin for OpenMenu ===
Contributors: openmenu
Donate link: http://openmenu.com
Tags: openmenu, restaurant, menu, restaurants, menus, open menu, dining, food
Requires at least: 5.0
Tested up to: 5.5.1
Stable tag: 3.5
 
Easily create posts that are based on your OpenMenu.  Fully integrates an OpenMenu or OpenMenu's and a restaurants Deals/Coupons into an existing theme.

== Description ==
This plugin allows you to easily create posts that are based on your OpenMenu and thus embedding restaurant menus in any Wordpress website.  This plugin fully integrates an OpenMenu or OpenMenus into an existing theme.  Widget / Menu ready themes work best.

The OpenMenu Plugin is the official plugin for OpenMenu and adding restaurant menus to any Wordpress website.

Get your OpenMenu at: http://OpenMenu.com

Features:

* OpenMenu Custom Post Type
* Widgets: Restaurant Location / Deals and Coupons / Specials / Cuisine Tag Cloud / QR Code / Filtered OpenMenu
* [openmenu], [openmenu_qrcode] and [openmenu_deals] Shortcodes
* Custom Functions
* Site wide setiings
* Lots of settings to control the look and feel of the way menus look


== Detailed Features ==
OpenMenu Custom Post Type: 
	Create custom posts which are menus based off of your OpenMenu.  Choose what to display, how to display it and the plugin does the rest.
	
	Settings:
		OpenMenu ID - This is a required field that is your OpenMenu ID
		
		Filters
			Menu Name to display: If your OpenMenu contains multiple menus (ex. Lunch / Dinner) you can choose which menu to display in your post by entering the menu name here. (supports a comma-separated list)
			Group Name to display: If your OpenMenu contains multiple menu groups (ex. salads / deserts) you can choose which group to display in your post by entering the group name here. (supports a comma-separated list)

		Restaurant Information: Stores basic information about the restaurant that is referenced by the menu. This is primarly used in scenarios where many restaurant menu's will be displayed.  Information, along with the excerpt, will be used to generate a single page of all menus.

		Cuisine Types: Define which cuisine type describes this restaurant.

Widgets:
	OpenMenu: Location  - Displays the restaurants location and hours
	OpenMenu: Specials  - Displays the menu items marked as special
	OpenMenu: Tag Cloud - A tag cloud for the cuisine types
	OpenMenu: QR Code - Displays a QR Code to your mobile site on OpenMenu 
	OpenMenu: Filter - Displays a list of menu items controlled by many definable filters
	OpenMenu: Deals - Display the deals attached to your OpenMenu

Short code:
	[openmenu]
	
	Parameters:
		openmenu_id	 = Your OpenMenu ID (not the OpenMenu URL, just the ID part)
		display_type     = menu (only option currently available)
		menu_filter      = Will display only the menu name matching this filter (supports a comma-separated list)
		group_filter     = Will display only the group name matching this filter (supports a comma-separated list)
		display_columns  = 1 | 2 - How many columns to display a menu in
		split_on	 = item | group - In 2 column display what do we split on
		background_color = Set the background color the menu will display on
		group_break 	 = 0 | 1 - Forces a 2-column display with hard breaks between groups
		embedded	 = 0 | 1 - Uses OpenMenu Embedded instead of rendering the menu locally
		generic_colors   = 0 | 1 - [embedding] Forces the use of the  generic colors for a menu 
		short_tags       = 0 | 1 - [embedding] Uses short tags for the special tags on menu items
		width            = [embedding] - Define the width of the embedded window (leave off for responsive)

		[defaults to OpenMenu Option setting]

	Samples: 
		[openmenu openmenu_id="sample"]
		[openmenu openmenu_id="sample" display_type="menu" display_columns="1"]
		[openmenu openmenu_id="sample" embedded="1"]

	[openmenu_qrcode]
	
	Parameters:
		openmenu_id	= OpenMenu ID (not the OpenMenu URL, just the ID part)
		size		= size for the QR Code (max 500) - defaults to 128

	Samples: 
		[openmenu_qrcode openmenu_id="sample"]
		[openmenu_qrcode openmenu_id="sample" size="256"]


	[openmenu_deals]
	
	Parameters:
		openmenu_id		= OpenMenu ID (not the OpenMenu URL, just the ID part)
		deal_id			= Show only a single deal based off of its ID
		compact_view		= shows the deals in a compact view (only the headline is displayed)
		show_print		= Determines whether the Clip/Print link is displayed in a deal
		new_window		= When show_print is true this determines if links are opened in a new window
		width			= width to display the deal
		width_units		= sets the units for the width value [px | %]

	Samples: 
		[openmenu_deals openmenu_id="sample"]
		[openmenu_deals openmenu_id="sample" width="500" width_units="px" compact_view="1"]

Custom Functions: 
	Display a location block: openmenu_location( post_id, title );
	Display a specials block: openmenu_specials( post_id, title );

Site Wide OpenMenu Settings:
	
	Look & Feel: 
		Display Type: What information will be displayed: Menu, Restaurant Information or Both
		How many columns: How many columns will be used to display a menu (1 or 2)
		Use Short Tags: Menu Item tags like special, vegatarian, halal, gluten free and such will be shortened to one or two letters
		Theme: only default is currently supported

	Your Menu: 
		Show Allergy Information: Determines if Allergy Information is displayed in a menu
		Show Calories: Determines if Calories are displayed in a menu
		Hide Prices: Determines if prices are shown for your menu items

	Wordpress Theme: 
		Show posts on homepage: Determines whether OpenMenu post types are displayed on the homepage blog post listing and in the RSS feed for the website.
		Hidesidebar: Forces the sidebar of a post to be hidden.  Gives the impression of a full-width page and may be more desirable when displaying menus.
		Width override: Attempts to force the width of the post to this amount.  Can be helpful for adjusting the display on troublesome themes.
		Menu background color: Set the background color the menu will display on (defaults to white - #fff)

Icon designed by Ben Dunkle, core designer for Wordpress.org. Website: http://field2.com - Contact ben@field2.com

== Installation ==

1. Unzip the openmenu.zip file
2. Upload the entire 'openmenu' folder to the '/wp-content/plugins/' directory
3. Activate the plugin through the 'Plugins' menu in WordPress
4. Update Site Wide options through the Settings -> OpenMenu Options


== Frequently Asked Questions ==

= Do you provide any online help? =

Yes.  We have a complete help system at: http://OpenMenu.com/help

= How do I get my menu converted to an OpenMenu so I can use this awesome plugin? =

Goto: http://OpenMenu.com and read about OpenMenu
OpenMenu Creator: http://OpenMenu.com/creator

= How do I find out about updates to this plugin? =

Any updates will be posted on the OpenMenu - http://OpenMenu.com/blog

= Can I display menus for multiple restaurants? =

Yes.  This is the main reason for using custom post types.  This allows you to create an entire Wordpress website of restaurants and menus

= Can I add a menu to a page? =

Yes.  All you need to do is use the shortcode described above.  Very simple and can be added anywhere in a page in minutes.

= My menu breaks my theme, what can I do? =

An issue that sometimes comes up is the slug of the page conflicts with theme styles.  Avoid a page slug like 'menu' which may conflict with menu stylings.

== Screenshots ==
1. OpenMenu Overview
2. Adding/Editing a Menu
3. OpenMenu Options
4. Sample Rendered Menu
5. Powerful Widgets
6. Deals and Coupon Widget / Shortcode

== Changelog ==
= 3.5 = 
* Updated embedding shortcode method to use the new responsive embedding code

= 3.0 = 
* Release for Wordpress 5.4.2
* Fixed issue with menus not displaying using shortcode

= 2.7 = 
* Release for Wordpress 5.2.2
* Fixed issue with create_function deprecated message

= 2.6 = 
* Release for Wordpress 4.8

= 2.4 = 
* Fixed deprecated function issues in the Widgets code 

= 2.3 = 
* Fixed issues for SSL sites

= 2.2 = 
* Support for Wordpress 4.4

= 2.1 = 
* Support for Wordpress 4.3

= 2.0 = 
* Updated OpenMenu inputs now take the OpenMenu ID instead of the OpenMenu URL
* Add embedded option to the openmenu shortcode. This builds the menu using OpenMenu Embedded instead of building locally.

= 1.6.19 = 
* Fixed issue with one-column rendering not working from shortcodes

= 1.6.18 = 
* Support for Wordpress 3.8.1

= 1.6.17 = 
* Support for Wordpress 3.8
* Add group_break parameter to the openmenu shortcode. This can override the global setting

= 1.6.16 = 
* Support for Wordpress 3.7
* Updated the menu/group filtering in shortcodes to handle an ampersand properly
* Updated the single-openmenu custom post page to properly support an ampersand in filtering

= 1.6.15 = 
* Support for Wordpress 3.5.2
* Updated the render class to fix issues with currency symbol for some European countries 

= 1.6.14 = 
* Added the new Group Break rendering option to display a 2-coumn display with a hard break between groups

= 1.6.13 = 
* Updated the render class to show a key for short tags showing only the tags used in the OpenMenu

= 1.6.12 = 
* Updated the render class to fix issues with currency symbol for some European countries

= 1.6.11 = 
* Updated the render class to fix issues with currency symbol for some European countries

= 1.6.10 = 
* Added option to QR widget to open the mobile site link in a new window
* Added Deal Widget so an OpenMenu's deals can be placed into a widget ready theme
* Added [openmenu_deals] shortcode 

= 1.6.9 = 
* Added an OpenMenu Filter widget
* Updated Specials Widget to properly handle currency symbols
* Removed unused functions and cleaned up existing codebase

= 1.6.8 = 
* Updated aspect ratio issue with image thumbnails
* Changed name of myfeed_request() function to prevent conflicts

= 1.6.7 = 
* Updated render class to fix issue with Menu Item Images not showing
* Updated the default style to better align with the base style provided by OpenMenu on all menu renderings

= 1.6.6 =
* Fixed issues where some user experienced blank menus

= 1.6.5 =
* Added Show/Hide prices to Settings -> OpenMenu
* Updated render and reader engine

= 1.6.4 =
* Updated render class to better support foreign currencies

= 1.6.3 =
* Added 'Include Mobile Link' to QR Code widget so a direct link to a restaurants mobile site on OpenMenu is displayed
* Updated some copy to better align with the OpenMenu brand
* Fixed state missing from Restaurant Location widget
* Fixed ref parameter

= 1.6.2 =
* Updated menu renderings to include short tag renderings
* Added a new Use Short Tag option to the global OpenMenu settings - this allows menu item tags like special, vegan, vegatarian to be shortened to one or two letters.

= 1.6.1 =
* Updated render class to support filters with quotes and commas in their names

= 1.6 =
* Added support for OpenMenu Format v1.6
* Added Menu and Menu Group notes to rendering
* Added gluten-free tag to menu rendering
* Updates to support Wordpress 3.3

= 1.5.7 =
* Updated Menu and Menu Group filters to support comma-separated lists

= 1.5.6 =
* Fixed function names to prevent collision with other plugins/themes

= 1.5.5 =
* Fix issue with render class handling carriage returns
* Updated reader class to work with disabled items (will not read them from an OpenMenu)

= 1.5.4 =
* Update render class to handle carriage returns in menu item descriptions
* Fix issue with the OpenMenu attribution appearing twice

= 1.5.3 =
* Updated Render class to v1.3.4
* Update to the display of calorie information
* Better support for pricing localization

= 1.5.2 =
* Fixed function naming issue which caused problems in some themes

= 1.5.1 =
* Fixed menu/menu group filter issue

= 1.5 =
* Added QR Code widget
* Added shortcode for QR Codes (openmenu_qrcode)
* Added new Your Menu section to OpenMenu Settings allowing you to control some of the menu information displayed
* Update OpenMenu settings to include Split On (you control whether the menu split 2 column displays on Menu Groups or Menu Items - defaults to Menu Item
* Update openmenu shortcode to include the new split_on parameter

= 1.4.5 =
* Fixed bom issue causing problems

= 1.4.4 =
* Fixed issue with encoding on currency symbols

= 1.4.3 =
* Added price to Menu Group Options and Menu Item Options

= 1.4.2 =
* Updated to support OpenMenu Format v1.5

= 1.4.1 =
* Added Menu URL and Menu URL Title to the Menu Widget
* Rename get_custom_field to om_get_custom_field to prevent conflicts with themes

= 1.4 =
* Added background_color attribute to the OpenMenu shortcode
* Modified CSS on default theme - change dl from overflow:auto to overflow:hidden
* Updated main code to read OpenMenu's (v1.4)
* Updated some code to be compatible with Wordpress 3.2

= 1.3.7 =
* Fixed issue with special characters in the menu or group filter not working properly

= 1.3.6 =
* Fixed issue with widgets (missing function)

= 1.3.5 =
* Fixed issue with widgets (missing function)

= 1.3.4 =
* Removed unused function
* Fixed Thumbnail to 32px x 32px per the OpenMenu Format
* Fixed issue with empty menu groups causing error

= 1.3.3 =
* Added Currency Symbols to menu item prices and alternate size prices

= 1.3.2 =
* Minor bug fixes

= 1.3.1 =
* Text and copy changes only

= 1.3 =
* Added Thumbnail images to menu listing
* Remove Setting link from plugin page (permission issue for some users)
* Update the location of the sample menu to http://openmenu.com/menu/sample
* Moved the styling of the OpenMenu tag to the OpenMenu theme stylesheet

= 1.2.1 =
* Fixed display issue with 2-column menu

= 1.2 =
* Updated to handle v1.2 of the OpenMenu Format
* Added group name filter to shortcode and OpenMenu posts

= 1.1.3 =
* Fixed issue where special characters were being double encoded and therefore not dispayed properly

= 1.1.2 =
* Updated OMF Reader class to handle server configuration that don't support simple_xml
* Fixed issue with handling missing information from custom post types / options

= 1.1.1 =
* Fixed issue with Dashboard display

= 1.1 =
* Added Menu / Menu Group Widget
* Added auto-detection of installed plugin folder (no longer assume /openmenu folder)
* Updated Restaurant Location widget to add the Include Hours setting
* Updated Specials Widget to include Menu Name filter
* Fixed issue where empty menu group (no menu items) caused crash

= 1.0.1 =
* Initial public release


== Upgrade Notice ==

= 1.0.1 =
* Initial public release