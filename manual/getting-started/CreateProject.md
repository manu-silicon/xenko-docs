# Create a project

We have discussed various features of the [Xenko Launcher](xenko-launcher/index.md). Now let us create a new project. Xenko provides two ways to create a project: you can create an empty project, or you can start with an existing sample.

While creating a new project you can also:

 * Create a simple and functional **New Project** by selecting a new game template.
 * Create a **New Package**.
 
   >**Note:** A game package is not a game, but a library of components as assets, scripts, and so on. A game package is not an executable file as a game, but it can be shared between different projects with its components.
   
 * Explore the **Samples** provided for graphics, audio, physics, UI, and so on along with two complete sample games: 
 
   * JumpyJet, a 2D scrolling game, and 
   * SpaceEscape, a 3d runner game.

 Feel free to check and explore these samples which helps you learn how to work with Xenko Game Engine.

This topic provides steps to create an empty project. 

**To create a new project:**

 1.	On the Xenko Launcher, click the Start button.
 
    ![media/CreateProject_StartButton.png](media/CreateProject_StartButton.png)
    _Start button of Xenko Launcher_

	The **New/open project** window opens.CreateProject_NewWindow
	
    ![media/CreateProject_NewWindow.png](media/CreateProject_NewWindow.png) 
    _New/open project window_
	
 2. Select **New Game** and click **Select**.
 
    The **Create a new game** window opens. This window helps to configure the new project.
	
    ![media/CreateProject_CreateNewGame.png](media/CreateProject_CreateNewGame.png) 
    _Create a new game_
	
 3.	Type a name to your new game in the **Namespace** box.
 4.	Select the required platform from the **Platforms** section. If your system does not have a particular platform requirement, a message is displayed.
 >**Note:** Xamarin license is required to build your game on iOS or Android.

 5.	Select the required configurations for graphic API and colors from the **Rendering** section.
 
    i. **Graphic API**: Select the required graphic API from the list. The graphic features are dependent on the API that you select. For advanced graphic features, select latest graphic API.

	>**Note:** Some of the graphic cards do not support the latest APIs. For mobile devices, restrict the selection to profile 9_1 or profile 10_0 respectively.
	
	ii.	**Colors**: Select the required range of colors for your game. You can choose either LDR or HDR. LDR (Low Dynamic Range) ranges from 0 to 1. HDR (High Dynamic Range) allows any random float values. HDR gives more possibilities but it is complex.
 
 6. Select the required orientation from the **Orientation** section.

  >**Note:** For PC games, use landscape. Portrait is suitable for mobile based games.

 7. Click **OK**.
    A new game is created and opened in **Xenko Game Studio**.
  
  >**Note:** Parameters done while creating a new project can be modified in the Xenko Game Studio whenever required.

Now, your project is ready. We can add some components to the game using the [Xenko Game Studio](game-studio-interface.md).
