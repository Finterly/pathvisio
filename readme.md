*********************
 PROJECT STRUCTURE 
*********************

| File/Folder | Description |
| ------------- | ------------- |
| apidoc/ (autogenerated)  | contains autogenerated documentation |
| build/ (autogenerated)  | contains generated class files |
| release/ (autogenerated) | output: jnlp, jar and zip package. |
| lib/ | contains the external libraries that PathVisio needs. |
| example-data/ | mapp and gpml files for quick testing |
| modules/ | the java source code for each of the different modules |
| pathvisio.sh | shortcut for running PathVisio from the command line (Linux/MacOSX) |
| pathvisio.bat | shortcut for running PathVisio from the command line (Windows) |
| readme.md | this file |
| build.xml | ant build file (see below) |
| pathvisio.iss | inno-setup script, to generate installer |

****************************
 HOW TO IMPORT IN ECLIPSE 
****************************

For detailed instructions, please see: https://github.com/PathVisio/pathvisio/wiki/PathVisio-setup-in-Eclipse

*************************
 HOW TO BUILD WITH ANT 
*************************

Using the ant build file, you can build the project from the command line. You can also use ant to generate the apidocs and to create an executable jar.

It is also possible to set up eclipse to build ant targets.

First make sure ant is set up properly. It comes with eclipse, but you'll have to check if the path is set correctly if you want to run it from the command line.

The ant build file provides the following targets, which you can invoke it from the directory which contains build.xml with 
```
ant <target>
```

where <target> is one of:
```
compile:   just compile all classes
docs:      generate all apidocs
exe:       generate executable jar file
clean:     remove all generated files
dist:      generate zip package and windows installer. 
           The zip package only includes files needed to *run* not compile.
all:       clean, then compile, jar, dist and docs.
```

********************************
 HOW TO RUN FROM THE TERMINAL 
********************************

If you have managed to build the classes with ant or with eclipse, you 
can use pathvisio.bat to start java from the command line.
