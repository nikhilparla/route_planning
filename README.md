# Route Planning Project

The route planning project implementation of Udacity cpp course

## Cloning

Cloned the project including submodules
```
git clone git@github.com:udacity/CppND-Route-Planning-Project.git --recurse-submodules
```

## IO2D installation
* IO2D library is needed for the project and here are the steps taken for that - 
  * Installation instructions for all operating systems can be found [here](https://github.com/cpp-io2d/P0267_RefImpl/blob/master/BUILDING.md)
  * This library must be built in a place where CMake `find_package` will be able to find it
  * Install Cairo: `sudo apt install libcairo2-dev`
    * alredy set the latest version
  * Install graphicsmagick: `sudo apt install libgraphicsmagick1-dev`
    * ImageMagick is a free and open-source software suite for displaying, creating, converting, modifying, and editing raster images.
  * Install libpng: sudo apt install libpng-dev
    * libpng12-dev is already the newest version (1.2.54-1ubuntu1.1)
  Cmake installation
  ```
  git clone --recurse-submodules https://github.com/cpp-io2d/P0267_RefImpl
  cd P0267_RefImpl
  mkdir Debug
  cd Debug
  cmake --config Debug "-DCMAKE_BUILD_TYPE=Debug" ..
  cmake --build 
  sudo make install.
```

## Compiling and Running

### Compiling
To compile the project, first, create a `build` directory and change to that directory:
```
mkdir build && cd build
```
From within the `build` directory, then run `cmake` and `make` as follows:
```
cmake ..
make
```
### Running
The executable will be placed in the `build` directory. From within `build`, you can run the project as follows:
```
./OSM_A_star_search
```
The output of the above command is the picture below.
<img src="map.png" width="600" height="450" />

This implies all the libraries were built and saved successfully and the cmake build in the project can find them.

## Testing

The testing executable is also placed in the `build` directory. From within `build`, you can run the unit tests as follows:
```
./test
```
Removed the dir created for installing io2d since it was large. Added the line in gitignore. Keeping the local copy but since you already did the make install step this folder is not necessary.
