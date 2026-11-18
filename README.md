# Minecraft Clone

A small Minecraft-style voxel game written in C++ with SFML and OpenGL. It is an early prototype for Windows.

## Features

- A world made of blocks, generated in chunks.
- Terrain generated with Perlin noise.
- A first-person player with mouse look, jumping, and walking, sprinting and crouching speeds.
- A main menu scene and a game scene.

## Build

You need Windows, CMake 3.28 or newer, a C++17 compiler and [SFML 2.6.1](https://www.sfml-dev.org/download/sfml/2.6.1/). GLAD, GLFW and nlohmann/json are included in `lib/`.

`CMakeLists.txt` expects SFML in `C:/Program Files/SFML-2.6.1`. Edit `SFML_DIR` and the include path there if you installed it somewhere else.

```
cmake -B build
cmake --build build
```

## Project layout

| Path | Contents |
| --- | --- |
| `main.cpp`, `Game.cpp` | Entry point and the main loop |
| `src/Core` | Blocks, chunks and the world |
| `src/Player` | Player movement and camera |
| `src/UI` | Scenes and interface widgets |
| `src/Utils` | Math helpers, textures and Perlin noise |
| `src/Config.h` | Window, player and interface constants |
