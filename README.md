# MH370

flightmap shows a flight over a rotating globe in D3. I've modified it to show MH370.

## Available functions

Highlight and rotate the globe to a specific country (not all countries are included in the dataset):

    selectCountry("United States")

Turn the plane graphic on (currently just a red box)

    planeOn = true;

Rotate the globe to a specific latitude / longitude coordinate:

    centerAt( [ 37.77493, -122.419416 ] );

Add a permanent path to the globe:

    addLine( [[37.77493, -122.419416], [20.3492, -130.2921]] );

## International Date Line

The example at http://mapmeld.github.io/flightmap crosses the International Date Line. If you are traveling west from Honolulu to Japan, you should give Honolulu's longitude as usual:

    centerAt([21.683414, -158.031954]);

Then wrap Japan's longitude to a value less than -180. For example +140 degrees East could be represented as -220 degrees West.

    centerAt([35.64, -220]);

If you were traveling in the other direction, you could give Japan's longitude as +140 degrees East and Honolulu's longitude as +202 degrees East.

## License

flight-map is available under an open source MIT License

It is based on the World Tour topojson / orthographic projection example at http://bl.ocks.org/d/4183330/
