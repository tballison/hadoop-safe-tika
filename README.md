This is a temporary shim that allows recent versions of Apache Tika
to be run by Hadoop. This artifact is custom-built for Nutch.

The major issue is that Tika and Apache POI use recent versions and features of commons-io,
and this has to be shaded to work with Hadoop.

We also have to strip out xerces and xml-apis.

See https://github.com/apache/nutch/pull/776

The versioning follows the pattern for tika's docker image: regular semver 2.9.3 (Tika's version) 
and then an extra digit to track the version of the shim, e.g. 2.9.3.1 would be the second release of the shim that 
works with Tika 2.9.3