# conan_scons

In order to compile the given program, SCons and Conan are both required. 

You can just try to compile the hello application by

```bash
scons
```
in the root of the project. Expected output looks like

```bash
scons: Reading SConscript files ...
PROJECT: Installing /media/sf_E_DRIVE/dev/scons_conan/conanfile.txt
Requirements
Packages

PROJECT: Generator scons created SConscript_conan
PROJECT: Generator txt created conanbuildinfo.txt
PROJECT: Generated conaninfo.txt
scons: done reading SConscript files.
scons: Building targets ...
gcc -o src/hello.o -c src/hello.c
gcc -o src/hello src/hello.o
scons: done building targets.
```
