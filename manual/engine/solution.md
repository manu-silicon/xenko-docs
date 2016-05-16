#Solution

In the Xenko Studio, the Solution explorer displays the hierarchy of your game.

The content of each package is grouped into two categories, namely Local packages and External packages. Local packages are your own packages that you created. External packages are the packages that you downloaded from the Internet, for example, the default Xenko package. If you open a package file (```.xkpkg```), you should see a single package of the local package category. If you open a solution file (```.sln```), you may see several packages if the solution contains more than one package.

Each package contains the following three base elements:

* Assets: The assets element contains all the assets contained in a package. You can expand the assets element to see the same hierarchy among the assets that is on the file system. When you select the **Assets** folder, the Asset view displays the assets contained in this folder.
* Code: The code element contains the code libraries and executables in the package. They each correspond to a single .csproj file. By right-clicking an executable, you can set it as the current project that allows you to compile the assets for the related platform and launch the game.
* Dependencies: The dependencies element lists all the other packages that are referenced by this package. The packages in the **Dependencies** list have their assets accessible to this package.

>**Note:** You can change the hierarchy in the **Solution explorer** by creating folders, and renaming or deleting objects.

Xenko uses Visual Studio solution files to list all the packages and code project related to a game. Thus, you can easily integrate the Xenko Studio and Visual Studio together, as they use the same root file for your project. By default, the Xenko Studio creates a new solution file when you create a new project, and manages references to both C# projects and packages.