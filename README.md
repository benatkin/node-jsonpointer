# JSON Pointer for nodejs

This is an implementation of [JSON Pointer](http://tools.ietf.org/html/draft-pbryan-zyp-json-pointer-00).

## Usage

    var jsonpointer = require("jsonpointer");
    var obj = { foo: 1, bar: { baz: 2}, qux: [3, 4, 5]};
    var one = jsonpointer.get(obj, "/foo");
    var two = jsonpointer.get(obj, "/bar/baz");
    var three = jsonpointer.get(obj, "/qux/0");
    var four = jsonpointer.get(obj, "/qux/1");
    var five = jsonpointer.get(obj, "/qux/2");

    jsonpointer.set(obj, "/foo", 6); // obj.foo = 6;

## Testing

    $ node test.js
    All tests pass.
    $

## Author

(c) 2011 Jan Lehnardt <jan@apache.org>

## License

MIT License.