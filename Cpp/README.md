# C++ CNN Project

This folder is configured with a modern CMake build workflow.

## Directory Structure

```text
Cpp/
├── CMakeLists.txt        # CMake build configuration
├── CMakePresets.json     # Presets for Ninja Release and Debug builds
├── .gitignore            # Ignores build/ outputs and compiler artifacts
├── inc/                  # Place your header files here (.h / .hpp)
└── src/                  # Place your source files here (.cpp)
```

## Build Instructions

### Standard CMake

```powershell
# 1. Configure the build
cmake -S Cpp -B Cpp/build -G Ninja

# 2. Build after adding your source files in src/
cmake --build Cpp/build

# 3. Run the compiled executable
.\Cpp\build\bin\cnn_app.exe
```

### Using CMake Presets

```powershell
# Configure using the default preset
cmake --preset default -S Cpp

# Build
cmake --build --preset default
```
