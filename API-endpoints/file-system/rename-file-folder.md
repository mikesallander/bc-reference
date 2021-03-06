## Rename file or folder

Rename a file or a folder.

### Request

* **Method:** PUT
* **Server:** https://api-[dub|nj|syd].worldsecuresystems.com/
  * Alternatively, use secure site URI (eg. https://mysite.worldsecuresystems.com)
* **Path:** /api/v2/admin/sites/[siteId]/storage/[filePath]?meta
* **Auth Header:** Site token required
* **Required Permissions:** Can use SFTP & File Manager

### Response

Returns a status Code

### Examples

Accepts and returns JSON as Content-Type.

#### JSON

**Request:**
~~~
PUT https://api.worldsecuresystems.com/api/v2/admin/sites/123/storage/images/cat.jpg?meta HTTPS/1.1
Connection: keep-alive
Accept: application/json
Authorization: c50f6e6be0d1481ca0d8eb0c63642fdd171c17846af04cdd95676a0888141f73
 
{
    "name":"dog.jpg"
}
~~~

**Response:**

~~~
HTTP/1.1 200 OK
~~~

### Sample code

Below is some sample code using the bcapi.js SDK. For more information, see [Interacting with APIs using the bcapi.js SDK](http://docs.businesscatalyst.com/content/developer-guides/apis/javascript-sdk.html)

**Rename a file**

Use `save` to change the name of a file.

~~~
var f = new BCAPI.Models.FileSystem.File('/my/file');
f.set('name', 'new-file');
f.save().done(function() {
    console.log('File name has been changed. Path is ' + f.get('path'));
    //prints: /my/new-file
});
~~~

**Rename a folder**

Use `save` to rename a folder:

~~~
var folder = new BCAPI.Models.FileSystem.Folder('/my/folder');
folder.set('name', 'new-folder');
folder.save().done(function() {
    console.log('The folder has been renamed');
    console.log('Path is now ' + folder.get('path'));
    //prints: /my/new-folder
});
~~~

### Error Codes

This method will return the following error codes:

* `200` - OK
* `400` - Bad request:
  * `104000` - Generic FileAPI error
	* `104003` - Not enough privileges
	* `104004` - Invalid login multiple sites
	* `104009`- Path not found
	* `104013` - Web page in workflow moved, if trying to move a page in workflow
	* `104014` - Name required
	* `104015` - Invalid URL if the page name would cause an invalid URL
	* `104016` - Name not unique
	* `104017` - Not allowed web extension
	* `104018` - Can't move folder
	* `104019` - Can't find folder
	* `104020` - Folder reserved
	* `104021` - Folder already exists
	* `104022` - Destination exists
	* `104023` - Unauthorized access
	* `104028` - File or folder name too long
* `401`- when authentication token is incorrect
* `404` - the folder does not exist
