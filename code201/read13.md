# local storage

***The localStorage and sessionStorage properties allow to save key/value pairs in a web browser.***

***The localStorage object stores data with no expiration date. The data will not be deleted when the browser is closed, and will be available the next day, week, or year.***

***The localStorage property is read-only.***

### Syntax
window.localStorage

>Syntax for SAVING data to localStorage:

- localStorage.setItem("key", "value");

>Syntax for READING data from localStorage:

- var lastname = localStorage.getItem("key");

>Syntax for REMOVING data from localStorage:

- localStorage.removeItem("key");


# HTML5 Storage

*is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string. If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype.*

> interface Storage {
  getter any getItem(in DOMString key);
  setter creator void setItem(in DOMString key, in any data);
};
Calling setItem() with a named key that already exists will silently overwrite the previous value. Calling getItem() with a non-existent key will return null rather than throw an exception.

Like other JavaScript objects, you can treat the localStorage object as an associative array. Instead of using the getItem() and setItem() methods, you can simply use square brackets. For example, this snippet of code:

var foo = localStorage.getItem("bar");
// ...
localStorage.setItem("bar", foo);
…could be rewritten to use square bracket syntax instead:

var foo = localStorage["bar"];
// ...
localStorage["bar"] = foo;
There are also methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).

>interface Storage {
  deleter void removeItem(in DOMString key);
  void clear();
};
Calling removeItem() with a non-existent key will do nothing.

Finally, there is a property to get the total number of values in the storage area, and to iterate through all of the keys by index (to get the name of each key).

>interface Storage {
  readonly attribute unsigned long length;
  getter DOMString key(in unsigned long index);
};
If you call key() with an index that is not between 0–(length-1), the function will return null.


# HTML5 STORAGE IN ACTION

Every time a change occurs within the game, we call this function:


function saveGameState() {
    
    if (!supportsLocalStorage()) { return false; }

    localStorage["halma.game.in.progress"] = gGameInProgress;

    for (var i = 0; i < kNumPieces; i++) {

	localStorage["halma.piece." + i + ".row"] = gPieces[i].row;

	localStorage["halma.piece." + i + ".column"] = gPieces[i].column;
    }

    localStorage["halma.selectedpiece"] = gSelectedPieceIndex;

    localStorage["halma.selectedpiecehasmoved"] = gSelectedPieceHasMoved;

    localStorage["halma.movecount"] = gMoveCount;
    return true;
}