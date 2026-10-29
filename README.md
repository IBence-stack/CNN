# CNN

Convolutional Neural Network and image processing project.

## Project Structure

```text
CNN/
├── Cpp/               # C++ core implementation
│   ├── CMakeLists.txt # CMake build configuration
│   ├── inc/           # Header files (.h / .hpp)
│   └── src/           # Source files (.cpp)
├── Python/            # Python workflow & scripts
│   ├── .venv/         # Virtual environment (local)
│   ├── requirements.txt
│   └── main.py
└── Executable/        # Executable binaries directory
```

## Getting Started

### C++ (CMake)

Configure and compile the C++ project:

```powershell
# Configure build
cmake -S Cpp -B Cpp/build

# Compile
cmake --build Cpp/build
```

### Python

Activate the virtual environment and install packages:

```powershell
# Activate venv (PowerShell)
.\Python\.venv\Scripts\Activate.ps1

# Install dependencies (when added to requirements.txt)
pip install -r Python\requirements.txt
```
