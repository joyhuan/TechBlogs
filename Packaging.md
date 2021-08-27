# Packaging Programs in JAR Files
## The Java™ Archive (JAR) file format enables you to bundle multiple files into a single archive file. Typically a JAR file contains the class files and auxiliary resources associated with applets and applications.

## benefits
- Security: digital sign
- Decreased download time
- Compression
- Packaging for extensions
- Package Sealing: enforce version consistency. all classes defined in that package must be found in the same JAR file
- Package Versioning
- Portability

## Using JAR Files: The Basics
JAR files are packaged with the ZIP file format, so you can use them for tasks such as lossless data compression, archiving, decompression, and archive unpacking. These tasks are among the most common uses of JAR files, and you can realize many JAR file benefits using only these basic features.

### Creating a JAR File
jar cf jar-file input-file(s)
