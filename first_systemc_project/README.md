This was an system first project exercise from
https://medium.com/@techAsthetic/getting-started-with-systemc-setup-code-and-run-baad1943ec4b

My environment: 
CMake 4.01 in Linux mode (first test in Windows 11's wsl Linux---Ubuntu)

The Cmake related error first encountered: 
CMake 4.01 seems to have removed min version, or actually,
require 3.5 or higher. So, I edited the CMakeList.txt accordingly.

The g++ example from the article worked.

I added a .gitignore file to ignore the build.

To build the project (copying article) (the mkdir build part is only required during intial build):
mkdir build
cd build
cmake ..
make
