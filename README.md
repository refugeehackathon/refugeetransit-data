# refugeetransit-data

Data repository for refugeetransit project


## Data source

The data originates from [refugeemap.com][refugeemap.com].

![refugeemap.com][refugeemap.com-screenshot]



## Data conversion

The original data comes as compressed KMZ which can be unarchived as KML.
In order to being consumed in the Android application the KML must be
converted into GeoJSON. However, when converting into GeoJSON the icon
references used on the original map are lost. To keep this information
the value from `<styleUrl>...</styleUrl>` we copy the value into the
`<ExtendedData>` node.

### Example for the added node

``` xml
<Data name='poitype'>
	<value>#icon-503-4186F0</value>
</Data>
```


[refugeemap.com-screenshot]: gfx/refugeemap.com-screenshot.png
[refugeemap.com]: http://refugeemap.com
