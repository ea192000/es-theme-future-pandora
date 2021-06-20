# Future Pandora

This repository contains the EmulationStation theme "Future Pandora" 

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

Sample Images
-------------

## **System view**

![Image](https://i.imgur.com/iX5SRwp.png)

## **Basic view**

![Image](https://i.imgur.com/RcnoAaE.png)

## **Detailed / Video view**

![Image](https://i.imgur.com/O30tpPV.png)

## **Grid view**

![Image](https://i.imgur.com/n9pitOl.png)

