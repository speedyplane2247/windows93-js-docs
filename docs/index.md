# Windows 93 JavaScript
*Created by Domenic Waterdash, Draco, DarkPhoenix10 and 1024x2*

Please note that new things may be discovered.

## Things that may come in handy
```js
$prompt('prompt text here', 'text in prompt text box') //displays a prompt message
$notif('notif text here') //displays a notification bubble on the bottom right
$alert('alert text here') // displays an alert message
$alert.info('info text here') // displays an info message
$alert.error('error text here') // displays an error message
$alert.progress('body','text') // see example of this, there are more arguments.
$alert.help('test') // another dialog, see example.
$confirm('confirm text here') // displays a question dialog
// (you can put html in these functions)
// there's a lot more to these functions as listed here. i plan to make a more detailed documentation of these in the future. (clue: passing objects to them and do more while writing less, as well as more features)
$window('http://example.com') // opens a website in a window (bear in mind that some websites do not work in this) due to cross-origin related stuff
$explorer('/c/a folder somewhere'); //opens up an explorer window in that directory
$exe('application name') // open an application of your choice
$explorer.setCurrent(id) // find the explorer window via id then focus on it (0 is always the desktop)
$window.current.maximize() // toggles between maximising to the window that is currently being used
$window.current.minimize(); // minimise the window that's currently being focused on
$window.current.restore(); // if the window that's currently being used has been minimised, open it back up again.
$window.current.destroy(); // closes the window that's currently being focused on (no animation)
$window.current.close(); // same as destroy but with animation
$loader.script("http://scriptu.rl/dot.js") // loads a script, similar to $exe("js ")

new Audio('/path/to/audio/audio.mp3').play(); // doesn't work with wav files sadly (btw the audio doesn't have to be on the windows 93 website)
$audio('alert').play() // new Audio().play() but can play windows 93 sounds specified by name
$boot.VERSION // returns the w93 version
system42.data._path // returns directories of things (.desktop returns where the desktop is located, .home returns where the users home is and .skin returns the folder the skin is)
system42.data._selected // returns an array of every shortcut or file selected at that moment
$explorer.current.getPath() // returns the path of the folder you're currently in from the explorer window you're currently using (can also be desktop)
$explorer.current // returns an object containing information about the explorer window you're currently using ( $explorer.current.id returns an id that you can use with $explorer.setCurrent(id))
$fullscreen() // toggle fullscreen
$fs.utils.getInfo('/a/file/dir.js'); // gives out info of that file in an object
location.reload() // restarts windows 93
$window.current.id // gets the id of the current window
$explorer.exe.SelectAll() // select everything in the current explorer window (can also be desktop)
$explorer.exe.EditShortcut() // open the edit shortcut dialog for the thing that is currently selected
$window.current.changeTitle('title'); // changes the title of the window that's currently being focused on
$window.current // returns an object containing info about the program that's currently being focused on
$window.current.cfg // returns all sorts of info about the program that's currently being focused on (is too big so i can't put everything here)
$window.current.changeIcon('/a/path/to/an/image.png') // set the icon of the window that's currently being focused on to something else (image doesn't have to be on w93, can be off another website)
$window.current.changeSize({width: 640, height: 480}) // set the size of the current window in pixels (some windows have a size limit)
le._apps // returns all applications in objects
$fs.utils.exist('/a/file/dir.js') // check if a file exists, and if it exists, returns 0, if it doesn't exist, return false// if it's a folder you're specifying, it'll just return the contents of it in objects
$fs.utils.getMenuOpenWith('/a/file/location.js') // returns the programs you can open the specified file with in an array with each application in an object
$fs.utils.getFileMenu('/a/directory') //however, if you want a neater directory or whatever listing, then use the "foldersList" array in this
// file creation
localforage.setItem('filename.txt', 'hello world') // create/edit file, only effective after a restart or explorer refresh
localforage.getItem('filename.txt').then(function(okthen){return okthen}) // get contents of a file
$store.set('desktop/meme.txt', 'hello world'); // alternative method to creating/editing files, effective sometimes for files that already exist
$store.getRaw('desktop/meme.txt') // alternative method to reading files, effective sometimes for files that already exist
$explorer.refresh() // refresh explorer
$archive('/folder/name')  // put the contents of the folder into a zipped archive that you can download
```
## Malicious:
```js
system42.data._settings.skin = "TOPKEK"; // changes the iconset to one that doesn't exist which causes all icons to fail loading unless you change the var back to 'w93'
// arc is now irrelevant.
$explorer.exe.Open($explorer.exe.SelectAll()) // select every file from the current explorer session and execute them
$explorer.exe.Delete($explorer.exe.SelectAll()); // select every file from the current explorer session and delete them
$file.format(function(){document.location.reload(true)}) // re-installs windows 93 (thanks domenic)
$file.delete("/a/") // deletes /a/, messes up a lot of things.
```

## Examples:
This has been moved [here](examples.md)
