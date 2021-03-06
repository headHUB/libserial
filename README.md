# Libserial

----
LibSerial provides a convenient, object oriented approach to accessing serial ports on POSIX systems.

You will need a recent g++ release, (anything after gcc-3.2 should work), to compile libserial, and you will also need to install Google Test (gtest) and the boost unit test library.  For Debian users:

```
sudo apt install libgtest-dev libboost-dev
```
----
If you get the source code from github and would like to install the library, you will need to generate the configure script first:

```
make -f Makefile.dist
```

----
You can skip this step if you are using a release package (which already contains the `configure` script). Once you have the `configure` script, run the following commands:

```
./configure 
make
make install
```

----
If you are a developer interested in utilizing the unit tests, ensure serial port names are appropriate for your hardware configuration in the UnitTests.cpp file:

```
#define TEST_SERIAL_PORT_1 "/dev/ttyUSB0"
#define TEST_SERIAL_PORT_2 "/dev/ttyUSB1"
```

The unit tests will be built during the make step above or you can build them by simply by running the compile script (which uses cmake):

```
./compile.sh
```

Unit test executables built using make can be run from the libserial/test/ directory:
```
./test/UnitTests
./unit_tests
```

Alternatively, unit test executables built using the compile script can be run from the libserial/build/bin/ directory: 
```
./build/bin/UnitTests
./build/bin/unit_tests
```

----
Complete documentation is available [here](http://libserial.readthedocs.io/en/latest/index.html).

----
(You can let people know that this Repository was useful to you by clicking the "Star" in the upper right of the repository home page!)