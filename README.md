iNZight *Lite* version 0.9.7.8
==============================

*Last Updated: 07/07/15*

This is the online version of iNZight (http://docker.stat.auckland.ac.nz), with four new modules:

- Visualize
- Time Series
- Model Fitting

Underway:
---------
- [Wishlist] Adjust the size of the "Help" button so that it matches the size of the actionButton.	
- [Manipulate] Go through the data extraction / manipulation options.
- [Model Fitting] Implement the model fitting module

Recent Updates (Most to least recent):
----------------------------------------
- [Time Series] Check if it can handle datasets with the "DATE" columns in column 2+.
- [Time Series] Fix "Provide Time Information".
- [Help] This module was removed. Even though it is in iNZight links to the new webpage already exist in the "About" start page and help to every module is available for every module inside the modules. 
- [Visualize]  Add inferential markups once Tom finishes updating iNZightPlots().
- [Advanced] Nest QE and TS under "Advanced".
- [Quick Explore] Merge into 1 tab.
- [General] Changed all global variables to reactive values (CK)
- [Row Operations] Row operations added (CK).
- [General] A Markdown 'troubleshoot' document appears when no data set is loaded (CP).
- [Data Import] URL support added (CK).
- [Quick Explore] Single column plot update - player feature (CK).
- [Time Series] Added shiny validation messages and modified the input panel so that only "Provide Time Information" is shown if the data set has no time variable defined in a format recognized by iNZightTS() (CP).
- [Visualize] Fixed the "Reset All" button (CP).
- [General] Updated help.md files for the "Time Series" and "Visualize" modules and created a template for use in other modules in */panels/0_Template/3_panelname-panel-help.md* (CP).
- [General] Fixed Datatables bug (CK).
- [General] Fixed question mark error (CK).
- [General] 404 Error fixed in "About" module (CK).
- [General] Footer appears at the bottom but sits below the content if window $<$ 767px (TE).
- [Help] Added a new "Help" module (CP).
- [General] Restructured code - new panels now have their own directory (CP).

To do:
------
- [General] Write a "log" file script.
- [General] Find better place for "help" button.

Package dependencies
--------------------
This are all the packages which are loaded by iNZight lite.
Please install all dependencies.

- iNZightPlots
- iNZightTS
- iNZightMR
- markdown
- gpairs
- iNZightRegression
- RJSONIO
- survey

Directories:
------------
- data:
This directory holds all the data. The data must be placed in sub-directories, which will come up as data categories within iNZight-Lite.

- gui-elements:
This directory contains the gui functions for all the old modules (from iNZight revamp). 

- www:
This directory is used for graphics and/or web-related files such as .css and .gif/.jpeg/.png javascript files. Images are stored in a sub-directory called "images". Javascript code is stored in a subdirectory "js".

- panels:
This directory contains the gui, server, help, and other functions for each module. It currently contains the "About", "Time Series", "Visualize", and "Model Fitting" modules. This makes it easier to modify code.

Main files:
-----------
- README:
Documentation for iNZight *Lite*. Update as required.

- global.R:
Defines functions and variables that are used globally. For now, all non-GUI functions are stored here.

- server.R:
Script for shiny server.

- ui.R:
Defines the main GUI.

Note:
-----
This repository will gradually be changed into the following format throughout 2015:

- data:
This directory holds all the data. The data must be placed in sub-directories, which will come up as data categories within iNZight *Lite*. 


- www:
This directory is used for graphics and/or web-related files such as .css and .gif/.jpeg/.png. Images are stored in a sub-directory called "images".

- panels:
This directory contains the gui, server, help, and other functions for each module. The directory/file names will be of the form:
  + [Directory] N_(sub-)panel-name
  + [File] 1_panelname-panel-gui.R
  + [File] 2_panelname-panel-server.R
  + [File] 3_panelname-panel-help.R
  + [File] 4_panelname-panel-null.R
  + [File] 5_panelname-panel-other.R


