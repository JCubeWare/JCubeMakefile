![JCubeMakefile](https://jcubeware.com/Public/Images/JCubeMakefile.png)

## 🗒️ TODO

[ ] Support for Windows installing.  

## 📚  About  📚

JCubeMakefile is a temporary way to build JCubeSuite projects before a new
build system is created.

## 🖥️  Installing  🖥️

JCubeMakefile requires make, build-essential and mingw-w64 on your device:

```
sudo apt install make
sudo apt install build-essential
sudo apt install mingw-w64
```

Once these are correctly installed, you should be able to use the makefile 
using the typical command `make` inside the build directory

## 💼  Usage  💼

JCubeMakefile functions under the pretense that:

1. Your project's source files are inside the source/ folder
2. There is a ProjectConfiguration.mk file inside the root directory.

Both these are covered by us in our projects already.
If you wish to use the JCubeMakefile in your project, put all C files inside the 
source/ directory and use this template for ProjectConfiguration.mk

```bash
##====[ PROJECT SETTINGS  ]====##

#JCUBEMAKE.PROJECT.
 JCUBEMAKE.PROJECT.NAME = TestProject
 #JCUBEMAKE.PROJECT.VERSION.
  JCUBEMAKE.PROJECT.VERSION.MAJOR = 0
  JCUBEMAKE.PROJECT.VERSION.MINOR = 0
  JCUBEMAKE.PROJECT.VERSION.REVISION = 1
 # Types: LIBRARY, EXECUTABLE
 JCUBEMAKE.PROJECT.TYPE = LIBRARY
 # Targets: Win32, Win64, Linux, JCubeOS
 JCUBEMAKE.PROJECT.TARGETS = Win32 Win64 Linux JCubeOS
```
