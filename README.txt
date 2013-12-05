Low Level Virtual Machine (LLVM)
================================

This directory and its subdirectories contain source code for the Low Level
Virtual Machine, a toolkit for the construction of highly optimized compilers,
optimizers, and runtime environments.

LLVM is open source software. You may freely distribute it under the terms of
the license agreement found in LICENSE.txt.

Please see the documentation provided in docs/ for further
assistance with LLVM, and in particular docs/GettingStarted.rst for getting
started with LLVM and docs/README.txt for an overview of LLVM's
documentation setup.

If you're writing a package for LLVM, see docs/Packaging.rst for our
suggestions.

#Build on arch:
mkdir -p llvm-build
cd llvm-build
ln -s /bin/python2 python
begin; set -lx PATH "$PWD $PATH"; cmake -D0CMAKE_BUILD_TYPE:STRING=RelWithDebInfo ../llvm; end
make -jXX
sudo make install
