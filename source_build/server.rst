Compiling the server launcher (Outdated as of 2021-07-27)
=========================================================

Prerequirements
---------------
- **Ubuntu** - :code:`sudo apt-get install git cmake pkg-config`
- **Fedora** - :code:`sudo dnf install git make cmake pkg-config gcc-c++ libstdc++.i686 glibc-devel.i686`
- **macOS** - :code:`brew install cmake`

Requirements
------------
- **Ubuntu** - you'll need to :code:`sudo dpkg --add-architecture i386`, then install the required packages: :code:`sudo apt-get install g++-multilib`
- **macOS** - none

Build instructions
------------------
.. code:: bash

   git clone --recursive https://github.com/minecraft-linux/mcpelauncher-manifest.git -b master mcpelauncher && cd mcpelauncher
   mkdir -p build && cd build
   cmake -DBUILD_CLIENT=OFF ..
   make -j$(getconf _NPROCESSORS_ONLN)

After compiling you should look at the :ref:`server` page. This server binary only works with Minecraft 1.12.x.
