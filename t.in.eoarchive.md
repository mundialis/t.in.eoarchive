## DESCRIPTION

*t.in.eoarchive* is a GRASS GIS addon python script to import a spatial
and temporal subset of a EO collection from a given archive into GRASS
as STRDS. Currently only the EOLAB archive and only the Sentinel-2 MAJA
collection is supported.

The spatial subset is defined by the current computational region, while
the temporal subset is defined by the **start** and **end** parameters.
If the **start** parameter is omitted, the earliest date with available
data is assumed as **start**. If the **end** parameter is omitted,
today's date is assumed as **end**.

The path to the mounted data directory can be defined by the
**mountpoint** parameter.

The resulting STRDS will contain semantic labels according to the user
defined **bands**

## EXAMPLE

Import bands 4,8 as well as the cloudmask for July 2022 of the
Sentinel-2 L2A MAJA collection of the EOLAB archive that is available
via the /codede mountpoint

```sh
t.in.eoarchive start=2022-07-01 end=2022-07-31 bands=S2_B4,S2_B8,S2_CLM output=S2_july_2022 mountpoint=/codede archive=eolab collection=S2-L2A-MAJA
```

## SEE ALSO

*[r.import](r.import.md) [t.create](t.create.md)
[t.register](t.register.md) [r.semantic.label](r.semantic.label.md)*

## AUTHOR

Guido Riembauer, [mundialis](https://www.mundialis.de/)
