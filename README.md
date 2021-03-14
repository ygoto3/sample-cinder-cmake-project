# sample-cinder-cmake-project

A sample CMake project for Cinder

Requirement
---

- CMake v3.7~
- Unix Makefiles

To develop
---

```sh
$ cd third-party
$ git submodule add git://github.com/cinder/Cinder.git
$ cd Cinder
$ mkdir build
$ cd build
$ cmake ..
$ make -j4
$ cd ../../..
$ mkdir build
$ cmake ..
```

