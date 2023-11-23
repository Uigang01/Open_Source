<div align="center">

![issues](https://img.shields.io/github/issues/Open-GD/OpenGD?style=for-the-badge&color=blue)
![forks](https://img.shields.io/github/forks/Open-GD/OpenGD?style=for-the-badge)
![stars](https://img.shields.io/github/stars/Open-GD/OpenGD?style=for-the-badge&color=blue)
![LICENSE](https://img.shields.io/github/license/Open-GD/OpenGD?style=for-the-badge&color=blue)
<a href="https://discord.gg/">
<img src="https://dcbadge.vercel.app/api/server/gcbuuR4JWg">
</a>
</div>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/Open-GD/OpenGD/releases/latest">
    <img src="https://user-images.githubusercontent.com/54410739/226145157-61edd6d9-eec4-479c-83b6-3f0c32e278c3.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">OpenGD</h3>

  <p align="center">
    Open source implementation of Geometry Dash
    <br />   
  </p>
  
![](https://img.shields.io/badge/platforms-windows%20%7C%20linux%20%7C%20mac%20%7C%20android%20%7C%20ios-blue)
    <p align="center">
    <a href="https://github.com/Open-GD/OpenGD/issues">Report Bug</a>
    ·
    <a href="https://github.com/Open-GD/OpenGD/releases/latest">Latest Release</a>
 · 
 <a href="https://github.com/Open-GD/OpenGD/issues">Request Feature</a>
  </p>
</div>


# UNMAINTAINED
new (unfinished) projects are [gdrender](https://github.com/maxnut/gdrender) and [gdclone](https://github.com/opstic/gdclone)
<!-- ABOUT THE PROJECT -->
## About The Project

![Stereo Madness running in OpenGD](https://cdn.discordapp.com/attachments/847950548921614366/1086798200146497647/6046uyhlekoa1.png "OpenGD")


OpenGD is an open-source implementation of the popular game Geometry Dash. Our main goal is to remake the gameplay 1:1, while also improving performance through new engine features and C++ enhancements. We also plan to implement multithreading in the future.

## Status 

We are currently rewriting the gameplay from the ground up, **levels are not playable at the moment**.

### Built With

OpenGD is powered by [axmol](https://github.com/axmolengine/axmol), which is maintained a fork of cocos2dx 4.0 that adds many new features and improvements over the original cocos2dx. The original Geometry Dash is also made with cocos2dx, but with a much older version from 2014.

## Build instructions

Required:
- Python 3.7+
- CMake
- One of the major c++ compilers (MSVC, clang, gcc)


> **Warning**
> OpenGD only builds with latest release branch of axmol, which is [6896f01](https://github.com/axmolengine/axmol/commit/6896f01d3e86a189c8e72ac420c8fdda739531fd) at the moment


<details>

  <summary>Windows</summary>

Clone axmol, run setup.py and restart cmd for command line variables to update
```
git clone --branch release https://github.com/axmolengine/axmol
cd axmol
python setup.py
```

For windows, it is recommended to build axmol separately and link it dynamically to reduce rebuilds, compile time and link time.

In the axmol folder, after running setup.py:
```
cmake -B build_x64 -A x64 -DAX_BUILD_TESTS=OFF
cmake --build build_x64 --config RelWithDebInfo
```

After axmol finished building you can run 
```
git clone https://github.com/Open-GD/OpenGD
cd OpenGD
cmake -B build -A x64 -DAX_PREBUILT_DIR=build_x64
cmake --build build --config RelWithDebInfo
```

> **Warning**
> VS 2019 might not work on Windows, VS 2022 is recommended

</details>

<details>

<summary>Other platforms</summary>
  
Check axmol [Dev setup](https://github.com/axmolengine/axmol/blob/dev/docs/DevSetup.md)

</details>

To actually run the game you will need the resources from the 2.1 version of Geometry Dash.

<!-- LICENSE -->
## License

Distributed under the GPL v3 License . See `LICENSE` for more information.

<!-- ACKNOWLEDGMENTS -->
## Credits

* [axmol](https://github.com/axmolengine/axmol) a fork of cocos2d-x-4.0
* [GD 1.0 decomps](https://github.com/Wyliemaster/Geometry-Dash-1.0) by Wylie
* [GD Physics decomps](https://github.com/camila314/gdp) by Camila
* [GD 2.1 decomps](https://github.com/matcool/gd-decomps) by mat
* [hps](https://github.com/jl2922/hps) high performance C++11 serialization library
* [gdclone](https://github.com/opstic/gdclone) another gd reconstruction project

### Contributors
This project exists thanks to all the people who have contributed:

<a href="https://github.com/Open-GD/OpenGD/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=Open-GD/OpenGD" />
</a>
