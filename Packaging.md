# Packaging Programs in JAR Files
The Java™ Archive (JAR) file format enables you to bundle multiple files into a single archive file. Typically a JAR file contains the class files and auxiliary resources associated with applets and applications.

## Benefits
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
### Sealing Packages within a JAR File
Packages within JAR files can be optionally sealed, which means that all classes defined in that package must be archived in the same JAR file. You might want to seal a package, for example, to ensure version consistency among the classes in your software.
### Enhancing Security with Manifest Attributes
## Signing and Verifying JAR Files
### Understanding Signing and Verification
### Signing JAR Files
### Verifying Signed JAR Files

## Using JAR-related APIs
```java JarRunner http://www.example.com/TargetApp.jar```
The JarRunner application consists of two classes, JarRunner and JarClassLoader. JarRunner delegates most of the JAR-handling tasks to the JarClassLoader class. JarClassLoader extends the java.net.URLClassLoader class.
### The JarClassLoader Class
### The JarRunner Class
```java JarRunner url [arguments]```

Answers to Questions and Exercises: JAR

Questions

Question: How do you invoke an applet that is packaged as a JAR file?

Answer: To invoke an applet packaged as a JAR file, open a page containing the applet:
```
<applet code=AppletClassName.class
        archive="JarFileName.jar"
        width=320 height=240>
</applet>```
Question: What is the purpose of the -e option in a jar command?

Answer: This option is available since Java SE 6. It sets the entrypoint as the application entry point for stand-alone applications bundled into executable jar file. The use of this option creates or overrides the Main-Class attribute value in the manifest file. This option can be used during creation of jar file or while updating the jar file. This option specifies the application entry point without editing or creating the manifest file. For example, this command creates Main.jar where the Main-Class attribute value in the manifest is set to Main:

jar cfe Main.jar Main Main.class
Question: What is the significance of the manifest in a JAR file?

Answer: A JAR file's manifest provides meta-information about the other contents of the JAR file. The manifest itself resides in META-INF/MANIFEST.mf. The meta-information can include

Dependencies on other jar files
The name of a class to run when "java -jar file.jar" is invoked
Versioning information
Security information
Question: How do you modify a JAR's manifest file?

Answer: Typically, modifying the default manifest involves adding special-purpose headers to the manifest that allow the JAR file to perform a particular desired function.

To modify the manifest, you must first prepare a text file with a complete and valid manifest file. You then use the JAR tool's m option to add the information in your file to the manifest.

The manifest file your prepare must end with a new line or carriage return. The last line will not be parsed properly if it does not end with a new line or carriage return.
