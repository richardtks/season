# season - CSON Node module

Read and write CSON/JSON files seamlessly.

## Installing

```sh
npm install season
```

## Building
  * Clone the repository
  * Run `npm install`
  * Run `grunt` to compile the CoffeeScript code
  * Run `grunt test` to run the specs

## Docs

```coffeescript
CSON = require 'season'
```

### CSON.stringify(object)

Convert the object to a CSON string.

`object` - The object to convert to CSON.

Returns the CSON string representation of the given object.

### CSON.readObject(objectPath, callback)

Read the CSON or JSON object at the given path and return it to the callback
once it is read and parsed.

`objectPath` - The string path to a JSON or CSON object file.

`callback` - The callback to call with the error or object once the path
             is read and parsed.

### CSON.writeObjectSync(objectPath, object)

Write the object to the given path as either JSON or CSON depending on the
path's extension.

`objectPath` - The string path to a JSON or CSON object file.

`object` - The object to convert to a string and write to the path.

### CSON.isObjectPath(objectPath)

Is the given path a valid object path?

Returns `true` if the path has a `.json` or `.cson` file extension, `false`
otherwise.