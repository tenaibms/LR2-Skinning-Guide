---
layout: page
title:  "Basic Skinning Syntax"
parent: "Getting Started"
date:   2023-09-30 14:21:08 -0700
nav_order: 2
---
## Basic Syntax ##
LR2 skins have a very simple syntax. Every word with `#` in front of it is a command. Everything with `//` in front of it is a comment. 

{: .note }
Commands are usually written in all caps, but this is not a strictly enforced rule, rather just a convention.

```
// Comment
#COMMAND // Valid
#command // Also valid but less preferred
```
Every command has a certain number of properties which can be delimited using either tabs or commas. The first property of a command typically is just null, and should just be left as zero. This is a quirk that you'll have to remember. 

{: .note }
All snippets on this website will use tabs rather than commas for ease of reading, however you should either set up your csv editor to export as commas or replace the tabs with commas in a text editor.

```
// Tabs
#COMMAND	0	1	2	3	4	5
// Commas
#COMMAND,0,1,2,3,4,5
```

Commands are usually written with their properties written above as a reminder, like so.

```
//#COMMAND	(NULL)	prop1	prop2	prop3	prop4	prop5
#COMMAND	0	1	2	3	4	5
```
The majority of skinning commands involve drawing images to the screen. Commands that begin with `SRC` refer to the source of an image, and commands that begin with `DST` refer to the destintation an image. For example, this is a simplified version of the image drawing command:

```
//SRC_IMAGE	(NULL)	gr	x	y	w	h				
#SRC_IMAGE	0	0	0	0	0	0	
//DST_IMAGE	(NULL)	time	x	y	w	h
#DST_IMAGE	0	0	0	0	0	0
```

For more information about those commands, please see [`#SRC_IMAGE`]({{ site.baseurl }}{% link docs/commands/src_image.md %}) and [`#DST_IMAGE`]({{ site.baseurl }}{% link docs/commands/dst_image.md %}) respectively.