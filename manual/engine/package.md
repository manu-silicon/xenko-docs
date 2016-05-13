# Package

Xenko uses package system, where each game itself is contained in a package, and can also use content from other packages. Thus, sharing resources across multiple games becomes possible.

A package is basically a container for:
* Game assets
* Code libraries
* Dependencies

A dependency is a reference from one package to another package, which allows another package using the contents from this package. When a package is a game, it also contains code executables (one per platform) along with game assets, code libraries, and dependencies.

Packages are saved on a disk with the ```.xkpkg``` extension.