This is a tweaked fork of the original [Saleae SWDAnalyzer](https://github.com/saleae/swd-analyzer) where the bit-level sampling 
annotation labels for bits that are read are in a more appropriate position that the original (e.g. addressing the issue raised in 
[#2](https://github.com/saleae/swd-analyzer/issues/2) - making less changes than [nezza's PR](https://github.com/saleae/swd-analyzer/pull/4) 
which seems to address more issues)

# Saleae ARM Serial Wire Debug (SWD) Analyzer

Saleae ARM Serial Wire Debug (SWD) Analyzer

## Getting Started

### MacOS

Dependencies:
- XCode with command line tools
- CMake 3.11+

Installing command line tools after XCode is installed:
```
xcode-select --install
```

Then open XCode, open Preferences from the main menu, go to locations, and select the only option under 'Command line tools'.

Installing CMake on MacOS:

1. Download the binary distribution for MacOS, `cmake-*-Darwin-x86_64.dmg`
2. Install the usual way by dragging into applications.
3. Open a terminal and run the following:
```
/Applications/CMake.app/Contents/bin/cmake-gui --install
```
*Note: Errors may occur if older versions of CMake are installed.*

Building the analyzer:
```
mkdir build
cd build
cmake ..
cmake --build .
```

### Ubuntu 16.04

Dependencies:
- CMake 3.11+
- gcc 4.8+

Misc dependencies:

```
sudo apt-get install build-essential
```

Building the analyzer:
```
mkdir build
cd build
cmake ..
cmake --build .
```

### Windows

Dependencies:
- Visual Studio 2015 Update 3
- CMake 3.11+

**Visual Studio 2015**

*Note - newer versions of Visual Studio should be fine.*

Setup options:
- Programming Languages > Visual C++ > select all sub-components.

Note - if CMake has any problems with the MSVC compiler, it's likely a component is missing.

**CMake**

Download and install the latest CMake release here.
https://cmake.org/download/

Building the analyzer:
```
mkdir build
cd build
cmake ..
```

Then, open the newly created solution file located here: `build\swd_analyzer.sln`
