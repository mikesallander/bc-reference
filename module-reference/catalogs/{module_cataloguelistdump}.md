## {module_cataloguelistdump,-1,rowLength,targetFrame,sortBy}

Renders a List of all Catalogue names with links to the catalogues.

### Parameters

* `1` - Use -1 to display parent catalogs, use -2 to display all catalogs including sub-catalogs
* `rowLength` - will limit the number of items per row when items are displayed as a list. Default is 1 item per row
* `targetFrame` - e.g. _blank. Specify the frame you want the item to open in
* `sortBy` - will sort the web apps in specified order
  * `Alphabetical` - sorts items alphabetically
	* `Weight` - sorts items by weight

`{module_cataloguelistdump,-1,1,_blank,Alphabetical}`

Renders the catalogue list, with links opening in a new window, alphabetically and all in one column
