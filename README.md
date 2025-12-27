# Memory Management Chatbot

![C++](https://img.shields.io/badge/C++-17-blue.svg?style=flat&logo=c%2B%2B)
![CMake](https://img.shields.io/badge/CMake-3.11+-green.svg?style=flat&logo=cmake)
![Platform](https://img.shields.io/badge/Platform-Linux-lightgrey.svg?style=flat)

A C++ chatbot demonstrating modern memory management concepts including smart pointers, move semantics, and the Rule of Five.

<img src="images/chatbot_demo.gif"/>

## What It Does

An interactive chatbot that answers questions about C++ memory management. The chatbot uses a knowledge graph where:
- **Nodes** represent possible answers
- **Edges** represent user queries
- **Levenshtein distance** finds the best matching answer

## Memory Management Concepts Used

- **Smart Pointers** - `unique_ptr` and `shared_ptr` for ownership
- **Rule of Five** - Custom copy/move constructors and assignment operators
- **Move Semantics** - Efficient transfer of resources without copying
- **RAII** - Resource management tied to object lifetime
- **Ownership Transfer** - Moving objects between graph nodes

## Project Structure

```
├── src/
│   ├── chatgui.cpp/h       # wxWidgets GUI
│   ├── chatbot.cpp/h       # ChatBot with Rule of Five
│   ├── chatlogic.cpp/h     # Knowledge graph management
│   ├── graphnode.cpp/h     # Graph nodes (answer storage)
│   ├── graphedge.cpp/h     # Graph edges (query matching)
│   └── ...
├── images/
│   ├── chatbot_demo.gif    # Demo animation
│   └── ...
└── CMakeLists.txt
```

## Dependencies

- cmake >= 3.11
- make >= 4.1
- gcc/g++ >= 5.4
- wxWidgets >= 3.0

### Install wxWidgets (Linux)
```bash
sudo apt-get install libwxgtk3.0-gtk3-dev
```

## Building

```bash
git clone https://github.com/Mohamedhendawy312/Memory-Management-Chatbot.git
cd Memory-Management-Chatbot
mkdir build && cd build
cmake .. && make
./membot
```

## Author

Mohamed Hendawy