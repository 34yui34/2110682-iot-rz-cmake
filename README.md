# 2110682-iot-rz-cmake
A repository for hosting IOT-RZ compiler suite used in 2110682 Embedded &amp; Real-Time Systems course. <br />
All source files and its contents belongs to Prof.Prabhas Chongstitvatana (Department of Computer Engineering, Chulalongkorn University). <br />
You can find the original course materials and IOT-RZ compiler suite from this link:<br /> [2110682 Embedded &amp; Real-Time Systems course materials](https://www.cp.eng.chula.ac.th/~prabhas//teaching/embed/2024/index-embed.htm) <br />

# Project structure
This is the directory structure of the project: <br />
- **`iot-rz/`**: This is the main project directory.
  - `archived/`: Contains all test files from the original course material.
  - **`bin/`**: Contains helper bash script for building and running compiler suite tools.
    - `build-tools`: bash script for building all compiler suite tools.
    - `runner-tools`: bash script for running compiler, assembler and simulator.
  - `doc/`: Documents from original course material.
  - `example/`: Examples chosen from archived folder.
  - **`tools/`**: Main folder containing source code for compiler, assembler and simulator.
    - **`as21/`**: Contains source code for assembler.
      - `build/`: Build folder for assembler executable. This folder will be created after running build-tools.
      - `include/`: Contains header files for assembler.
      - `src/`: Contains source files for assembler.
      - `unused/`: Contains unused files from original material.
      - `CMakeLists.txt`: CMake file for assembler.
    - **`rz36-2/`**: Contains source code for compiler.
      - `build/`: Build folder for compiler executable. This folder will be created after running build-tools.
      - `include/`: Contains header files for compiler.
      - `src/`: Contains source files for compiler.
      - `doc/`: Contains documents from original material
      - `unused/`: Contains unused files from original material.
      - `CMakeLists.txt`: CMake file for compiler.
    - **`sim21/`**: Contains source code for simulator.
      - `build/`: Build folder for simulator executable. This folder will be created after running build-tools.
      - `include/`: Contains header files for simulator.
      - `src/`: Contains source files for simulator.
      - `unused/`: Contains unused files from original material.
      - `CMakeLists.txt`: CMake file for simulator.
  
- **`.gitignore`**: gitignore file.

- **`LICENSE`**: LICENSE file.

- **`README.md`**: README file.
<br />

# How to use
To build all tools:
```
cd iot-rz/bin
./build-tools --build-all
```
This will build all tools (assembler, compiler and simulator) in their respective build directory.<br /><br />
To clean all build artifacts:
```
cd iot-rz/bin
./build-tools --clean
```
This will clean out all build artifacts.<br /><br />
To run any tools:
```
cd iot-rz/bin
./runner-tools {tool-types} {input_file_path}
```
{tool-types} can be any of these three values: "as21", "rz36" or "sim21"<br />
{input_file_path} input file path for the tool. this can be absolute path or relative path.


