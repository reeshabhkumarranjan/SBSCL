# Installation

## LP solver
For running flux balance analysis simulations a LP solver is required. The respective jars have to be made available.

Download the GLPK Solver Pack `GLPKSolverPack.jar` (please note the GPL licensing terms)
and LPSOLVE Solver Pack `LPSOLVESolverPack.jar` (please note the LGPL licensing terms) from
http://scpsolver.org/ and add in the library folder according to the `pom.xml`.


### GLPK

```
sudo apt-get install libglpk-dev
sudo apt-get install libglpk-java
```

File -> Project Structure -> Libraries

/usr/lib/x86_64-linux-gnu/jni/libglpk_java.a
/usr/lib/x86_64-linux-gnu/jni/libglpk_java.so
/usr/lib/x86_64-linux-gnu/jni/libglpk_java.so.36
/usr/lib/x86_64-linux-gnu/jni/libglpk_java.so.36.2.0


The artifact does not include the binary libraries, which have to be installed separately.
When testing with Maven it may be necessary to indicate the installation path of the GLPK for Java shared library (.so or .dll).
```
mvn clean install -DargLine='-Djava.library.path=/usr/local/lib/jni:/usr/lib/jni'
```


### cplex
- get academic license, install, add cplex jar to cplex folder.
