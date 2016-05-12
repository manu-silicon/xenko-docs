# Project organization

We have discussed how to [create a project](http://doc.xenko.com/latest/manual/getting-started/howto-create-and-setup-new-game.html) in the Xenko Studio. In this topic, we will discuss how a Xenko project is organized.

A Xenko project is organized into various parts. Each game is contained in a package. A project simply means a game project. In Xenko Studio, the Solution explorer section displays the hierarchy of your game. Assets are the objects used in your game. Finally, resources are images, textures, and entity images used in your game.

Thus, following is the hierarchy of game projects in Xenko:

* [Package](#package) 
* [Project](#project)
* [Solution](#solution)
* [Assets](#assets)
* [Resources](#resources)

<a name="package"></a>
## Package

Xenko uses package system, where each game itself is contained in a package, and can also use content from other packages. Thus, sharing resources across multiple games becomes possible.

A package is basically a container for:
* Game assets
* Code libraries
* Dependencies

A dependency is a reference from one package to another package, which allows another package using the contents from this package. When a package is a game, it also contains code executables (one per platform) along with game assets, code libraries, and dependencies.

Packages are saved on a disk with the ```.xkpkg``` extension.

<a name="project"></a>
## Project

In the Xenko Studio, a project refers to a game project. You can create new games, new packages, and play various types of sample games.

After you create a new project in the Xenko IDE, Xenko creates a Visual Studio application at the same location on your machine. The Visual Studio application includes the **Assets**, **Bin**, and **Resources** folders similar to a .NET application.

<a name="solution"></a>
##Solution

In the Xenko Studio, the Solution explorer displays the hierarchy of your game.

The content of each package is grouped into two categories, namely Local packages and External packages. Local packages are your own packages that you created. External packages are the packages that you downloaded from the Internet, for example, the default Xenko package. If you open a package file (```.xkpkg```), you should see a single package of the local package category. If you open a solution file (```.sln```), you may see several packages if the solution contains more than one package.

Each package contains the following three base elements:

* Assets: The assets element contains all the assets contained in a package. You can expand the assets element to see the same hierarchy among the assets that is on the file system. When you select the **Assets** folder, the Asset view displays the assets contained in this folder.
* Code: The code element contains the code libraries and executables in the package. They each correspond to a single .csproj file. By right-clicking an executable, you can set it as the current project that allows you to compile the assets for the related platform and launch the game.
* Dependencies: The dependencies element lists all the other packages that are referenced by this package. The packages in the **Dependencies** list have their assets accessible to this package.

>**Note:** You can change the hierarchy in the **Solution explorer** by creating folders, and renaming or deleting objects.

Xenko uses Visual Studio solution files to list all the packages and code project related to a game. Thus, you can easily integrate the Xenko Studio and Visual Studio together, as they use the same root file for your project. By default, the Xenko Studio creates a new solution file when you create a new project, and manages references to both C# projects and packages.

<a name="assets"></a>
## Assets

Assets are the objects used in your game, such as data, meshes, textures, materials, and sounds. Most of the assets are generated while importing a source file, for example, while importing an audio file or a 3D model.

Assets can also be created from scratch, such as entities. For each asset, a single file is created, usually with an extension starting by ```.xk```. For example, the texture asset uses the ```.xktex``` extension. You can sort assets into folders and subfolders for easy access. The root path of the assets of a package is stored in the package file.

<a name="resources"></a>
## Resources

Resources are images, textures (```[.dds](https://en.wikipedia.org/wiki/DirectDraw_Surface)``` files), and entity images used in your game. Resources are stored in the **Resources** folder of a game application.

>**Note:** As a best practice, all data resources should be moved inside the **Resources** folder so as to move your project easily. If resources are outside of the project, moving the project breaks the links and compiler issues can occur.