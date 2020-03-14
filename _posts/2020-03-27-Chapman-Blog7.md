---
layout: post
title: "Blog 7"
---
Basic Python for ArcMap
-----------------------

Here are some basic commands for starting a new map document in ArcMap which is the software typically used for GIS which is written in Python.

### Comments
	##double pound is used for a comment line

	'''
	triple-quoted strings can be used
	for multiline comments in Pyhton
	'''

### Print to Screen
	print "Hello World"
	print 3*6

### Variables & Assignment
	mapName = "Valencia"
	mapname = "Northridge"

### Strings
A string can be wrapped by double quotations marks

	aMapName_1 = "Valencia"

Or, it can be wrapped by single quotations marks

	aMapName_2 = 'Northridge'

If you use a pair of double quotation marks to surround your text , you can use single quotation marks inside the string and vice versa

	aString = "My name is 'Soheil' "
	aQuery = ' "Area" > 1000 '

### Concatenation
Strings can be concatenated using + sign

	aString_1 = "Geographical"
	aString_2 = "Information"
	aString_3 = "Systems"

	print aString_1 + aString_2 + aString_3

### New Line & Tab
New line

	\n

Tab

	\t

Examples:

	aString_1 = "Geographical Information Systems"
	aString_3 = "Geographical \tInformation \n\tSystems"

### ArcPy
ArcPy is a site package(Python site package) – library of added functionalities with multiple modules. It provides access to all geoprocessing tools, extensions, functions and classes for working with ESRI GIS data.
It must be imported to the script:

	import acrpy

### Setting the Environment
The workspace must be set for geoprocessing. Using ArcPy you can retrieve or set the environment settings of your map. This can be done using *env* class of ArcPy.

	env.workspace

##### Workspace Path Assignment
String literal with “r” before the path:

	aWS = r"C:\Geog\Workspce"

Double backslash “\\\” in path name:

	aWS = "C:\\Geog\\Workspace"

Single forward slash “/” in pathname:

	aWS = "C:\\Geog/Workspace"
