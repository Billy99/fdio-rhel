# Red Hat FD.io Documentation Repository

This is the official downstream repository for the Red Hat FD.io product documentation.
Currently, only VPP (Vector Packet Processing) is support, but other projects under FD.io may be supported in the future.

## Building

This section describes how to generate documentation from this repository.

### Required Tools

In order to generate a document from this source, *asciidoctor* must be installed.
For more details, see https://asciidoctor.org/docs/install-toolchain/.
There are a few ways to install, below is the 'dnf' method:
```
   sudo dnf install -y asciidoctor
```


To use the Asciidoctor PDF converter, make sure Ruby >= 2.0.0 is installed.
```
  ruby --version
  ruby 2.4.4p296 (2018-03-28 revision 63013) [x86_64-linux]
```

Then install the PDF converter:
```
  gem install asciidoctor-pdf --pre
  gem install rouge
```


### Generate Documents

To generate an HTML version of a given document, run *asciidoctor* on a given *master.adoc* file. This will generate a *master.html* file in the same directory.
```
      asciidoctor doc-VPP_Installation_and_Configuration_Guide/master.adoc
```

To generate a PDF version of a given document, run *asciidoctor-pdf* on a given *master.adoc* file. This will generate a *master.pdf* file in the same directory.
```
      asciidoctor-pdf doc-VPP_Installation_and_Configuration_Guide/master.adoc
```


## Branches

### Production Branches (English)

Production branches map to published content for each version of Red Hat FD.io released.

*master*: The most recent documentation version. Currently VPP 18.04.


### Working Branches

Writers use topic branches to track work that has not yet been verified merged to a production branch.

Topic branches use the format 'BZ#_123456_' with an optional description appended. For example 'BZ#1322343_VPP_Install_Updates'.

Topic branches can be safely deleted when their content has been merged to a production branch.



