# OpenGL Compute Shader Template

A minimal OpenGL 4.5 starter kit with compute shader support for GPU-driven particle simulation.

## Features

- **Compute Shaders**: GPU-accelerated particle updates
- **GLFW Window**: Cross-platform windowing
- **ImGui Overlay**: Real-time stats display (particle count, FPS)
- **Camera Controls**: Mouse-based orbit camera
- **Catch2 Testing**: Shader compilation tests
- **CMake Build**: FetchContent dependencies (GLFW, GLM, ImGui, Catch2)

## Using This Template

To start a new project from this template:

```bash
# Clone the template
git clone https://github.com/csunday95/opengl-template.git my-project
cd my-project

# Disconnect from this template repo
git remote remove origin
git remote add origin <your-new-repo-url>

# Push to your new repo
git branch -M main
git push -u origin main
```

This gives you a clean, independent project. If you want to track template improvements later, you can add `git remote add upstream https://github.com/csunday95/opengl-template.git` and merge updates as needed.

## Building

```bash
cmake --preset debug
cmake --build build/debug
./build/debug/opengl_template
```

## Options

```
--particles N     Number of particles (default: 4096)
--width W         Window width (default: 1280)
--height H        Window height (default: 720)
```

## Architecture

- `src/core/`: GL initialization, shader loading, camera
- `shaders/compute/`: Particle update kernel
- `shaders/render/`: Point rendering (vert + frag)
- `tests/`: Shader compilation tests
