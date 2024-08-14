# Future Pandora

This repository contains the EmulationStation theme "Future Pandora".

IMPORTANT: Since 06/2024, this theme has been updated with the latest release from [github.com/ea192000/EmulationStation](https://github.com/ea192000/EmulationStation)

About
-----

This theme is based on Futura V theme by FlyingTomahawk (https://github.com/FlyingTomahawk/es-theme-futura-V) and Pandora Box frontend.

Has been updated to work with EmulationStation 2.10.0 by jrassa (https://github.com/jrassa/EmulationStation).

License
-------

This theme can be replicated, modified or used under the CC-BY-NC-SA license.

Create new System Template
--------------------------
### Create a folder with the system short name on this root folder (example **test**):

```
/future-pandora/
             /_art/
             /_xml/
             ...
             /test/
             ...
```

### Create 3 PNG images with ressolution of 510x290 px (recomended size):

- test/screenshot_center.png
- test/screenshot_left.png
- test/screenshot_right.png

### Create 1 PNG image for system logo with ressolution of 600x170 px (recomended size):

- test/system.png

### Create a xml file (**theme.xml**) with the following template and replace:

- **{{ system_description }}**: Description of system (to be shown in main screen only).
- **{{ system_name }}**: Name of the system.
- **{{ system_year }}**: Year of the system (example: 1973 - 2005).
- **{{ system_manufacturer }}**: Name of the company owned of the system.


```xml
<theme>
    <formatVersion>3</formatVersion>
    <include>./../theme.xml</include>
	<view name="system, basic, detailed, video, grid">
        <image name="logo">
            <path>./system.png</path>
        </image>
    </view>
	<view name="system">
		<text name="system_description" extra="true">
			<text>{{ system_description }}</text>
		</text>	
		<image name="screenshot_left" extra="true">
			<path>./screenshot_left.png</path>			
		</image>
		<image name="screenshot_center" extra="true">
			<path>./screenshot_center.png</path>
		</image>			
		<image name="screenshot_right" extra="true">
			<path>./screenshot_right.png</path>
		</image>
	</view>
	<view name="basic, detailed, video">
		<text name="system_name" extra="true">
			<text>{{ system_name }}</text>
		</text>		
		<text name="system_year" extra="true">
			<text>{{ system_year }}</text>
		</text>	
		<text name="system_manufacturer" extra="true">
			<text>{{ system_manufacturer }}</text>
		</text>				
	</view>		
</theme>
```

### Finally, the folder must contain these files:

```
/future-pandora/
             ...
             /test/
                   screenshot_center.png
                   screenshot_left.png
                   screenshot_right.png
                   system.png
                   theme.xml
             ...
```

Changing resolution and language
--------------------------------

This template has been created to work on 720p and 1080p (originally was thinking to work on old machines), with texts on spanish and english.

There are a way to change from 1080p to 720p and language. All has been configured on file **theme.xml** from root directory:

```xml
<theme>
	<formatVersion>4</formatVersion>
	<!-- Assets -->
	<include>./_xml/assets/default.xml</include>
	<include>./_xml/assets/fonts.xml</include>
	<include>./_xml/assets/colors.xml</include>
	<include>./_xml/assets/sounds.xml</include>
	<!-- Views -->
	<include>./_xml/views/system.xml</include>
	<include>./_xml/views/basic.xml</include>
	<include>./_xml/views/detailed.xml</include>
	<include>./_xml/views/grid.xml</include>
	<!-- Images -->
	<include>./_xml/images/1080p.xml</include>
	<!-- Language -->
	<include>./_xml/language/english.xml</include>
</theme>
```

On folder **/_xml/images/** are 2 xml:

- 720p.xml
- 1080p.xml

On folder **/_xml/language/** are 2 xml:

- english.xml
- spanish.xml

If you want to change language to spanish and resolution to 720p, only must change those values on **theme.xml**:

```xml
	<!-- Images -->
	<include>./_xml/images/720p.xml</include>
	<!-- Language -->
	<include>./_xml/language/spanish.xml</include>
```

Also you can create your own language xml, or resolution xml using those as reference.

Sample Images
-------------

## **System view**

![Image](https://i.imgur.com/iX5SRwp.png)

## **Basic view**

![Image](https://i.imgur.com/RcnoAaE.png)

## **Detailed / Video view**

![Image](https://i.imgur.com/MMqKMst.png)

## **Grid view**

![Image](https://i.imgur.com/n9pitOl.png)

