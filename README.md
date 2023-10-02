This is a temporary shim that allows recent versions of Apache Tika
to be run by Hadoop.

The major issue is that Tika and Apache POI use recent versions of commons-io,
and this has to be shaded to work with Hadoop.

We also have to strip out xerces and xml-apis.

See **FILL IN LINKS HERE**
