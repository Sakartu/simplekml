Simplekml
---------

This is a (modified) clone of the code found at https://code.google.com/p/simplekml/. It encorporates a number of changes, which are listed here:

 - The id field of the main Document feature is no onger read-only. Changing the id field of the Document may help when one is trying to create a Tour, in which a gx:AnimatedUpdate requires that you give the id of the feature to change.
 - The constructor of the Kml and Document classes now both have a "name_as_id" feature. If this is set to True, the id property of the main Document will be the same as it's name. This feature is also implemented to help with creating Tours (see above)

Original documentation
----------------------

simplekml is a python package which enables you to generate KML with as little effort as possible.

At the time of making this package nothing was available (at least I could not find anything) that could create KML files easily. You needed a lot of bloated code to even create a simple point. This is understandable because the KML standard is quite extensive, but what if you just work with the simple elements of KML like Document, Folder, Point, LineString and Polygon? This package supports those elements and everything documented in the KML Reference. With simplekml creating a KML file containing a point as simple as::

    import simplekml
    kml = simplekml.Kml()
    kml.newpoint(name="Kirstenbosch", coords=[(18.432314,-33.988862)])
    kml.save("botanicalgarden.kml")

See the http://simplekml.readthedocs.org for usage and reference.
Visit http://code.google.com/p/simplekml/ for the homepage.
