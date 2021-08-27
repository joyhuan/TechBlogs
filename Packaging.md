# Packaging Programs in JAR Files
The Java™ Archive (JAR) file format enables you to bundle multiple files into a single archive file. Typically a JAR file contains the class files and auxiliary resources associated with applets and applications.

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

- Creating a JAR File: ```jar cf jar-file input-file(s)```
- View contents: ```jar tf jar-file```
- Extract contents: ```jar xf jar-file [archived-file(s)]```
- Updating a JAR File: ```jar uf jar-file input-file(s)```

## Running JAR-Packaged Software
- Applets Packaged in JAR Files
- JAR Files as Applications: ```java -jar jar-file```

## Working with Manifest Files: The Basics
JAR file's manifest gives a JAR files versatility.

The manifest is a special file that can contain information about the files packaged in a JAR file. By tailoring this "meta" information that the manifest contains, you enable the JAR file to serve a variety of purposes.
### Understanding the Default Manifest
When you create a JAR file, it automatically receives a default manifest file. There can be only one manifest file in an archive, and it always has the pathname

META-INF/MANIFEST.MF
When you create a JAR file, the default manifest file simply contains the following:

Manifest-Version: 1.0
Created-By: 1.7.0_06 (Oracle Corporation)
### Modifying a Manifest File
```jar cfm jar-file manifest-addition input-file(s)```
### Setting an Application's Entry Point
### Adding Classes to the JAR File's Classpath
You specify classes to include in the Class-Path header field in the manifest file of an applet or application. 
```Class-Path: jar1-name jar2-name directory-name/jar3-name```
### Setting Package Version Information
