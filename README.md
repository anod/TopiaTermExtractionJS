Topia TermExtract 1.1.0 for JavaScript
======================================

Port of python's package topia.termextract 1.1.0 to JavaScript

## Original package

[topia.termextract 1.1.0][1] 

## Example

    <script type="text/javascript" src="vendors/underscore-1.4.2-min.js"></script>
    <script type="text/javascript" src="vendors/backbone-0.9.2-min.js"></script>
    
    <script type="text/javascript" src="src/anod/topia/namespace.js"></script>
    <script type="text/javascript" src="src/anod/topia/lexicon.js"></script>
    <script type="text/javascript" src="src/anod/topia/defaultfilter.js"></script>
    <script type="text/javascript" src="src/anod/topia/tagger.js"></script>
    <script type="text/javascript" src="src/anod/topia/termextractor.js"></script>

    <script>
        var tagger = new window.anod.Topia.Tagger({},{
            'lexicon' : window.anod.Topia.lexicon
        });
        var filter = new window.anod.Topia.DefaultFilter();
        var extractor = new window.anod.Topia.TermExtraction({
             'tagger' : tagger, 'filter' : filter
        });
        
        var tags = extractor.call(document.getElementById("source").innerHTML);
        tags.sort();
        document.getElementById("result").innerHTML = tags.join("<br/>");
     </script>

See [termextraction.html][2]

## Dependencies
 * Underscore.JS
 * Backbone.JS

## Author of the port

Alex Gavrishev, 2013

 [1]: http://pypi.python.org/pypi/topia.termextract/
 [2]: https://raw.github.com/anod/TopiaTermExtractionJS/master/termextraction.html
