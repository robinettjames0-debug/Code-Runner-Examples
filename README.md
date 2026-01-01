# Code Runner Examples

This repository contains examples and configuration for running multi-file programs using Code Runner mobile app. 
It also contains a list of all supported languages and their run and compile commands

## 📱 About Code Runner

Code Runner is a mobile application that allows you to write, compile, and run code directly on your mobile device. This repository serves as a reference for handling multi-file projects and includes configuration for all supported programming languages.

## 🗂️ Multi-File Program Examples

### Java 22 Project Example
```
│── Main.java
│── Utils.java
│── run
└── compile
```

`compile`:
```bash
#!/bin/bash
/usr/local/openjdk22/bin/javac Main.java Utils.java
```

`run`:
```bash
#!/bin/bash
/usr/local/openjdk22/bin/java Main
```

### Python Package Example
```
project/
├── mypackage/
│   ├── __init__.py
│   └── helper.py
├── main.py
└── run
```

`run`:
```bash
#!/bin/bash
/usr/local/python-3.8.1/bin/python3 main.py
```

### C++ Project Example with CMake
```
project/
├── include/
│   └── functions.h
├── src/
│   ├── main.cpp
│   └── functions.cpp
├── CMakeLists.txt
├── compile
└── run
```

`CMakeLists.txt`:
```
cmake_minimum_required(VERSION 3.13)
project(hello LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 14)

add_executable(main ${CMAKE_CURRENT_LIST_DIR}/src/main.cpp m
${CMAKE_CURRENT_LIST_DIR}/src/functions.cpp)
target_include_directories(main PRIVATE ${CMAKE_CURRENT_LIST_DIR}/include)
```

`compile`:
```bash
#!/bin/bash
mkdir build
cd build
cmake ..
make
```

`run`:
```bash
#!/bin/bash
./build/main
```

## 📋 Supported Languages

The `languages.json` file in this repository contains the complete list of supported programming languages and their corresponding compile/run commands.