## Hypher

A small and fast JavaScript hyphenation engine. Can be used as a jQuery plugin.

##jQuery

To use the jQuery plugin include `jquery.hypher.js` in your HTML document together with any number of language pattern files from the `dist/browser` directory in the [patterns repository](https://github.com/bramstein/hyphenation-patterns). It is important that you include `jquery.hypher.js` before any language pattern files.

    <script src="jquery.hypher.js"></script>
    <script src="en-us.js"></script>

This will extend jQuery with a `hyphenate` method. Given the following HTML:

    <p>Hyphenation is <em>important</em></p>

You can hyphenate the text content of the `p` element like so:

    $('p').hyphenate('en-us');

The `hyphenate` method only works on the text content of the elements it is called on, so in the above example the word "important" will not be hyphenated. To also include the text content of the `em` element, simply include it in your selector:

    $('p, em').hyphenate('en-us');

This naturally also applies to your own classes:

    $('p.hyphenate, em, a').hyphenate('en-us');

This will hyphenate only `p` with class `hyphenate` and `em` and `a` elements.


## License
Hypher is licensed under the three clause BSD license (see BSD.txt.)

## See also
* [Hyphenation patterns for use with Hypher](https://github.com/bramstein/hyphenation-patterns)
* [Hyphenator.js](http://code.google.com/p/hyphenator/)

## Contributors

* Laurens Meurs - improvements to the exception list
