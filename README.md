## Building a Leo node and CLI WALLET 

### On *nix

Dependencies: GCC 4.7.3 or later, CMake 2.8.6 or later, and Boost 1.55.

#### Ubuntu 16.04 LTS The Trusty Tahr install instruction.

You need to install classic lib to compile your code here :

x)) Install Leo Build to run your private node and CLI WALLET

Pick your folder to install leo node
make leo
cd /leo
git clone https://github.com/thirdbrainsa/ThirdBrainCoin

If you don't have git installed do a apt-get install git

x)) Install dependencies

sudo apt-get install cmake build-essential libboost-all-dev 

x)) Build !

To build, change to a directory where this file is located, and run `make`. The resulting executables can be found in `build/release/src`.

xx) Run the Daemon

You have screen installed by defaut (apt-get install screen if you have not)

then 

tape :

screen -S daemon
cd /thirdbraincoin/build/release/src
./tbd

Do a CTRL a+d after to detach the screen

Do a screen -ls to list the screen

Do a screen -r <ID> of the screen to re-enter in the screen and do a CRTL a+d to exit without closing the daemon
  
I prefer to run a deamon inside a screen but you can also launch it in the way you want.

**Advanced options:**

* Parallel build: run `make -j<number of threads>` instead of `make`.
* Debug build: run `make build-debug`.
* Test suite: run `make test-release` to run tests in addition to building. Running `make test-debug` will do the same to the debug version.
* Building with Clang: it may be possible to use Clang instead of GCC, but this may not work everywhere. To build, run `export CC=clang CXX=clang++` before running `make`.

### On Windows
Dependencies: MSVC 2013 or later, CMake 2.8.6 or later, and Boost 1.55. You may download them from:

* http://www.microsoft.com/
* http://www.cmake.org/
* http://www.boost.org/

To build, change to a directory where this file is located, and run theas commands: 
```
mkdir build
cd build
cmake -G "Visual Studio 12 Win64" ..
```

And then do Build.
Good luck!
