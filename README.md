Key data
============

- name of the plugin: Metadata export plugin
- author: Felix Gründer
- current version: 1.0.0.0
- tested on OJS version: 2.4.6
- github link: https://github.com/ojsde/metadataExport.git
- community plugin: no
- date: 24.5.2016

Description
============

This plugin provides an export of article metadata.
After installation, a new sidebar block "EXPORT METADATA" is displayed containing the following elements:
- buttons by which the scope of the export can be determined: 
  all articles of the current journal, all articles of the current issue or just the current article
- a select box for choosing one of the formats BibTeX, MARC XML, RDF and RIS
  
By clicking "Export" the automatic download of the export file starts.

In contrast to the already existing citation plugin of OJS (as part of the "reading tools"), the metadata are not only displayed, but also offered for download.

Installation
============

- rename the unzipped folder to *metadataExport* and copy it to *plugins/generic*
- execute the following shell command: 
  *$ php tools/upgrade.php upgrade* (see https://pkp.sfu.ca/ojs/UPGRADE)
- in *Setup / Step 5* move the metadata export block to the appropriate position in the sidebar

 
Implementation
================

Database access, server access
-----------------------------
- reading access to OJS tables: 1

		plugin_settings

- writing access to OMP tables: 0

- new tables: 0
- recurring server access: yes

		An xml file is generated and sent to the browser
 
Classes, plugins, external software
-----------------------
- OJS classes used (php): 4
	
		lib.pkp.classes.plugins.BlockPlugin
		lib.pkp.classes.plugins.GenericPlugin
		lib.pkp.classes.xml.XMLCustomWriter
		classes.handler.Handler

- necessary plugins: 3

		BibtexCitationPlugin
		CustomBlockManager
		ProCiteCitationPlugin
		
- optional plugins: 0
- use of external software: no
	
- file upload: no
 
Metrics
--------
- number of files: 25

Settings
--------
- none

Plugin category
----------
- plugin category: generic

Other
=============
- does using the plugin require special (background)-knowledge?: no
- access restrictions: no


