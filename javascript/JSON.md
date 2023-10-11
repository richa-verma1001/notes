
Reference https://javascript.info/json

JSON.stringify(obj);

JSON is data-only language-independent specification, so some JavaScript-specific object properties are skipped by JSON.stringify.

Namely:

Function properties (methods).
Symbolic keys and values.
Properties that store undefined

The full syntax of JSON.stringify is:

```
let json = JSON.stringify(value[, replacer, space])
```

#### Others
* JSON.toJSON()  --> If an object has toJSON, then it is called by JSON.stringify
* JSON.parse()   -> JSON string back into its Data form
