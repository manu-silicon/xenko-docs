# Guidelines

Xenko users will be reading your articles to learn about the engine in their every day work. 
Your goal is to write pages easy to understand and that are accessible to all. 
To help you in your quest and to have an unified documentation easy to use,
we ask you to follow to the below Guidelines when writing.

* [Writing Style](#Style)
  * [Conversation Tone](#Tone)
  * [Second Person](#Person)
  * [Active Voice](#ActiveVoice)
  * [Simple Vocabulary](#SimpleVocabulary)
* [Pages Content](#PagesContent)
  * [Getting Started Pages](#GettingStarted)
  * [Tutorials Pages](#Tutorials)
  * [Samples Pages](#Samples)
  * [Section Header Pages](#SectionHeader)
  * [Overview Pages](#Overview)
  * [Reference Pages](#Reference)
  * [HOWTO Pages](#Howtos)
  * [Avoid Long Explanations](#LongExplanations)
  * [Avoid Long Articles](#LongArticles)
  * [Use Images & Videos](#UseImagesVideos)
* [Pages & Files Structure](#FilesStructure)
  * [Pages Hierarchy](#PagesHierarchy) 
  * [Pages Order](#PagesOrder)
  * [Files Hierarchy](#FilesHierarchy)
  * [Files Name](#FilesName)
* [Formatting](#Formatting)
  * [Definitions](#Definitions)
    * [Xenko Terms](#XenkoTerms)
    * [Video Game Terms](#VideoGameTerms)
    * [Job Specific Terms](#JobTerms)
  * [Page References](#References)
  * [Related Topics](#RelatedTopics)
  * [API References](#APIReferences)
  * [Code References](#CodeReference)
  * [Placeholders](#Placeholders)
  * [Labels](#Labels)
  * [Remarks](#Remarks)
  * [Platform Specific Remarks](#PlatformRemarks)
  * [Notices](#Notices)
  * [Media](#Media)
    * [Videos](#Videos)
    * [Images](#Images)
    * [Diagrams](#Diagrams)
  * [Tables](#Tables)
  * [Lists](#Lists)
  * [Headers](#Headers)
  * [Letter Capitalization](#Capitalization)
  
Note: The following directions are just guidelines not rules. 
If they are not appropriate to your specific use-case, feel free to ignore them.

# <a name="Style"> Writing Style

## <a name="Tone"> Conversation Tone

> **Appropriate**
> 
> We want our documentation to have a conversational tone. You should feel as though you
> are having a conversation with the author as you read any of our tutorials or explanations.
> Your experience as a reader should be informal, conversational, and informative. You should
> feel as though you are listening to the author explain the concepts to you.
> 
> **Inappropriate Style**
>
> One might see the contrast between a conversational style and the style one finds with
> more academic treatments of technical topics. Those resources are very useful, but the authors
> have written those articles in a very different style than our documentation. When one reads
> an academic journal, one finds a very different tone and a very different style of writing.
> One feels that they are reading a dry account of a very dry topic.  

The first paragraph above follows our recommendation conversational style. The second
is a more academic style. You see the difference immediately. 

##  <a name="Person"> Second Person

> **Appropriate**
> 
> You should write your articles as though you are speaking directly to the reader. 
> You should use second person often (as I just have in these two sentences). 
> 2nd person doesn't always mean using the word 'you'. Write directly to the reader. 
> Write imperative sentences. Tell your reader what you want them to learn.
> 
> **Inappropriate**
> 
> An author could also choose to write in 3rd person. In that model, an author must find 
> some pronoun or noun to use when referring to the reader. A reader might often find 
> this 3rd person style less engaging and less enjoyable to read.

The first paragrah follows our recommended style. The second uses 3rd person. 
Please write in second person. You probably found that much easier to read.

##  <a name="ActiveVoice"> Active Voice

Write your articles in active voice. Active voice means that the subject of 
the sentence performs the action (verb) of that sentence. It contrasts with passive voice, 
where the sentence is arranged such that the subject of the sentence is acted upon. 
Contrast these two examples:

> **Appropriate**
> 
> The compiler transformed source code into an executable.

> **Inappropriate**
> 
> The source code was transformed into an executable by the compiler.

The first sentence uses active voice. The second sentence was written in passive voice. 
(Those two sentences provide another example of each style).

We recommend active voice because it is more readable. Passive voice can be more difficult to read.

##  <a name="SimpleVocabulary"> Simple Vocabulary

Keep in mind that Xenko users are not all native English speaker when you write your articles.
Your audience is international and they probably don't have the vocabulary you have.

As a general rule try to *target a 5th grade reading level" when you write.

#  <a name="PagesContent"> Pages Content

This documentation is composed of different types of pages. The expected content and layout
of the page directly depends on the type. Before writing your article, start by identifying the 
type of page you are targeting, then follow the below templates for content and layout.

In addition to content and layout guidelines based on the type of page, we finish this section 
with a few generic recommendations for the content.

##  <a name="GettingStarted"> Getting Started Pages

Getting Started articles aim at guiding new Xenko user in its first steps. Pages should cover only basic 
and essential topics and don't need to explain concepts in depth. Only one subject should be covered per page.

Pages targeting any kind of audience should be inserted directly under the Getting Started root page.
Pages targeting a specific audience should be inserted under a page specifying the audience. Getting
Started pages order should follow the progress of a Xenko new user.

A Getting Started page consists of the following content:

1. The page title (the subject dealt in the page).
2. A paragraph explaining what the reader will learn in the page.
3. The knowledge needed to be able to follow the instructions (if any).
4. An image or a video illustrating what the user will learn (if possible).
5. A table of content summarizing the main steps of the page (if applicable).
6. The sub-titles and the content of the page.

Example:
```
# Design Scenes with Xenko.

In this article you will learn how to create scenes from the editor in Xenko.
This page assume that you are already able to import assets in Xenko.

[Scene Image](media/scene.png)

* [Drag and drop elements in your scene](#Drag and drop elements in your scene)
* [Navigate in the scene editor](#Navigate in the scene editor)
* [Adjust the position of your elements](#Adjust the position of your elements)

## Drag and drop elements in your scene

...
```

##  <a name="Tutorials"> Tutorials Pages

The purpose of tutorials is to accompany users through the creation of a game component. Each tutorial 
starts from a initial state (most of the time an empty game) and ends to a final state (mini game or 
game component completed). A page should be created for each main step of the final realization.
Pages should be ordered chronologically and next pages should start exactly were previous pages stop.
A folder should be created for each tutorial. 

A tutorial header page consists of the following content:

1. The page title (name of the tutorial).
2. A description of what will be realized and what can be learned from the tutorial. 
3. The knowledge needed to be able to complete the tutorial (if any). 
4. One or several images of the final realization (if possible). 
5. A table of content with the links to the tutorial sub-pages (ordered list).

Example
```
# My 2D game tutorial

In this tutorial you will create a simple 2D game from scratch. You will learn how to create a scene,
perform collisions between elements and add a UI to your game.
This tutorial assumes that you know how to create a new project and import assets in Xenko.

[My 2D Game Image](media/my2dGame.png)

1. [Import assets](ImportAsset.md)
2. [Create your level](CreateLevel.md)
3. [Add Collisions](AddCollisions.md)
4. [Add a UI](AddUI.md)
```

A tutorial page consists of the following content:

1. The page title (realization of the page) 
2. A description of what will be realized in the current page and what will be learned. 
3. One or several pictures illustrating the realization of the page (if possible).
4. A table of content summarizing the main steps of the page. 
5. The sub-steps and the content of the page.
6. A link to the previous and to the next page of the tutorial.

Example
```
# Add UI to the game

In this page you will add a simple UI to your game. You will learn how to create a UI using Xenko default 
design and make it interact with the gameplay.

[My Game UI Image](media/MyGameUI.png)

1. [Add a UI component](# Add a UI component)
2. [Set the UI](# Set the UI)
3. [Make UI interact with your game](# Make UI interact with your game)

## Add a UI component 

...

Previous [Use Physics Collisions](UsePhysicsCollision.md) | Next [Deploy your game](DeployYourGame.md)
```

Note: as much as possible each instruction should be surrounded by two images showing the state 
before and after the instruction. Image before the first instruction should correspond to the initial
state and last image should correspond to the final state.

##  <a name="Samples"> Samples Pages

For each Xenko sample, a documentation sample page should be created. The purpose of this page is to explain
what is shown in the sample, what is the difficulty and what can be learned.

A sample page consists of the following content:

1. The page title (name of the sample).
2. A paragraph explaining what is shown in the sample and what can be learned.
3. The knowledge needed to be able to understand this sample (if any). 
4. One or several images of the samples (if possible).
5. A table of content summarizing the different points of the sample (if needed).
6. The sub-titles and the content of the page.

Example:
```
# Material Sample

This sample shows you how to create different types of material in Xenko. You will learn how to 
create metallic, organic and layered and blended materials. 

In order to fully understand this sample, you need to know standard lighting models. To learn more 
about this have a look  that [Lighting Models](../Graphics/LightingModels.md).

![Material Sample Image1](media/materialSample1.md)

* [PBR Materials](# Physically Based Materials)
* [Metallic Materials](# Metallic Materials)
* [Organic Materials](# Organic Materials)

...

```

##  <a name="SectionHeader"> Section Header Pages

Section headers are the top pages of the folders of the documentation. The goal of header pages is 
to introduce the section topic, to expose the best features of the engine and to provide quick links 
to the main topics of the section.

A header page consists of:

1. The name of the section as title
2. An image illustrating the section (for sub-folder this image can be skipped)
3. A short introduction sentence explaining what is the section about.
4. A paragraph exposing the main and best features of the engine on the topic.
5. A short paragraph explaining what can be learned by reading this section. 
6. Links to the section overview and the main topics of the section. For the main sections,
one image per link illustrating the sub-topic will be added as a grid.

Note: for sub-folder headers the section header page can be replaced by the overview page when appropriate.

Example
```
# Physics

![Physic Section Image](media/PhysicSection.png)

Physics allows you to make physic simulations in your game.

Xenko has a physic system fully integrated in its game studio. Its dedicated physic editor allows you to
directly edit physic shapes of objects or to automatically generate them from the models. 

In this section you will learn how to simulate collisions between objects, add trigger regions, apply 
physic law on objects, etc.

|Overview| Physic Shapes| Simulation
|![OverviewImage](media/Overview.png)|![Physic Shapes](media/PhysicShapes.png)|![Simulation](media/Simulation.png)
```

##  <a name="Overview"> Overview Pages

The purpose of overview pages is to give a full insight of a wide topic to the reader. It should 
expose and explain the main concepts from a high level point of view.

An overview page consists of:

1. The Page title (Section name + Overview).
2. A short paragraph explaining what is the topic or section about.
3. A paragraph exposing the objectives, the challenges and the limitations (if applicable).
4. An explanation of the main or base concept (if applicable)
5. A paragraph listing the more specific solutions and corresponding concepts (if applicable)
6. A table of content of the sub-topics of the page.
7. The sub-topics with their content (if possible add an image after each sub-topic title).

Example
```
Physics Overview

This page introduces you the different ways to simulate physic interaction in your game.

The goal of the physic engine is to provide ways to produce and automate actions on your game elements
so that they seems to follow physic laws. Accurate physic simulations being very costly all physic behaviors
have to be approximated. 

To simplify the computation we use simplified physic shapes and different types of physic objects 
for the physic calculations. 

* Physic Shapes(# Physic Shapes)
* Physic Object Types(# Physic Object Types)
* Physic Constrains(# Physic Constrains)
* Physic Forces(# Physic Forces)

# Physic Shapes

![Physic Shapes Image](media/PhysicShapes.png)

...

```

##  <a name="Reference"> Reference Pages

Reference pages explain in depth a specific concept, feature, or element.

A reference page consists of:

1. The page title (name of the concept)
2. The definition of the concept.
3. The standard usages of the concept.
4. An image illustrating the concept (if possible)
5. A table of content of the sub-topic of the page (if needed)
6. The sub-topics with the content.

Example
```
# Materials

A material is a set of rules defining how to render an element.

You can use materials with model, particles system and sprites to define the color, lighting and shadowing
of your element.

![Material Image](media/Material.png)

* Object Geometry(# Object Geomatry) 
* Object Shading(# Object Shading)
* Layers(# Layers)

1. Object Geometry

...
```


##  <a name="Howtos"> HOWTO Pages

The goal of the HOWTO pages is to provide a list of clear instructions to realize a specific thing. 
Each HOWTO page should be independent from other HOWTO pages and guide the reader towards 
only one and single target. It should not define nor explain any concept.

A HOWTO page consists of:

1. The page title (phrase starting with a verb describing the target)
2. The goal of the page and what the user will learn to doc-audience
3. The knowledge needed to understand the instructions.
4. An image of the final realization (if possible)
5. A table of content of the main steps taken to reach the objective
6. The main steps and their explanations and sub-instructions (add the step number in the sub-title)

Example
```
# Add particles inside our UI

In this page you will learn how to attach particles to an UI element.

This page assumes that you know how to use particles and UI elements in general.

![Particles In UI Image](media/ParticlesInUI.png)

1. Create your particle Effect(# Create your particle Effect)
2. Create your UI(# Create your UI)
3. Add a UI link component(# Add a UI link component)

## 1. Create your particle Effect.

...

```

Note: as much as possible each instruction should be surrounded by two images showing the state 
before and after the instruction. Image before the first instruction should correspond to the initial
state and last image should correspond to the final state.

##  <a name="LongExplanations"> Avoid Long Explanations

Long explanation are quite indigestible for the reader. Most of the time, he simply skips them.
If not, he is not able to remember the essential point of the explanation. 

To avoid this, try to never explain more than one concept in a simple paragraph.
Try to keep your explanation short and simple and when possible add an image or a diagram 
that corresponds to the concept next to your text.

This guideline is even more important for Getting Started, Samples, Tutorials and HOWTO pages,
where the text should correspond more to instructions than explanations about Xenko concepts.
In those pages, you should either try to explain the concept in a simple lline or replace the
explanation by a reference to the page dedicated to the concept.

##  <a name="LongArticles"> Avoid Long Articles

Try to avoid writing articles longer than 8 to 10 screen heights. Long articles discourage users 
to start reading and make the navigation harder. If the content of your article cannot fit in
the above number of screen, split your article into several articles.

##  <a name="UseImagesVideos"> Use Images & Videos

As much as possible add images or videos to accompany your explanation. This helps the reader a lot.

Also whenever it makes sense, we recommend you to use small videos instead of images. 
We believe that the time where we had to use diagrams with lots of arrows going in all directions
because videos were too heavy is over. Nowadays Internet connections and compression algorithms 
are good enough to include short videos in the documentation and increase even more the ease of
understanding.

#  <a name="FilesStructure"> Pages & Files Structure

The hierarchy of the documentation pages is specified in the [manual/toc.md](manual/toc.md) file
and is independent from the file hierarchy of this repository. For example, a single article can
be added several times at different location in the documentation if needed. Nevertheless for ease
we ask you to try to keep the same hierarchy between the documentation pages and this
repository files.

To add a new page in the documentation, just add a new entry at the appropriate place in the 
[toc](manual/toc.md) file.

## <a name="PagesHierarchy"> Pages Hierarchy

As a general rule, we want to avoid deep hierarchies for the ease of navigation. 
As much as possible we recommend you not to go beyond 4 levels of depth.

> Getting Started
>   - Common Topic
>   - Targeted Audience
>      - Topic
> Tutorials
>   - My 2D game
>   - My 3D game
> Samples
>   - Graphics
>     - Material sample
>   - Physics
>     - Raycasting sample
> Section Header
>   - Overview
>   - Topic
>   - Sub-Category
>     - Sub-Topic
>   - HOWTO
>     - Do something

Page naming conventions:
* No prefix need to be added before the Overview and HOWTO pages ('Overview' and not 'Graphic Overview')
* The name of the pages under the HOWTO folder should start with a verb and describe an objective ('Activate post-effects to your game', etc)

## <a name="PagesOrder"> Pages Order

Documentation pages don't necessary need to be alphabetically ordered.

As a general rule, order your new pages as follow:

1. Chronologically when there is a chronological order (Getting started / tutorial pages)
2. Most important subjects first (Overview pages -> References pages -> HOWTOs) 
3. When pages have the same importance, order them alphabetically.

## <a name="FilesHierarchy"> Files Hierarchy

Article files should be organized into folders. As much as possible we will try to respect the
same hierarchy as the documentation. Files corresponding to section header should be included at the 
top of the folder having the same name and be named 'index.md'. Folder and file names should be
composed of only lower case letters, words should be separated by dashes.

Media files (images and videos) referenced in articles should be placed in a dedicated folder
named 'media' and put next to the referencing articles.

Code sample files (C#, scripts, etc) referenced in articles should be placed in a dedicated 
folder named 'code' and put next to the referencing articles.

Hierarchy example:

> graphic
>   - index.md
>   - overview.md
>   - media
>     - overview-image1.png
>     - overview-image2.png
>     - overview-video2.mp4
>   - post-effects
>     - index.md
>     - media
>       - post-effect-image1.png
>     - code
>       - post-effect-code.cs

## <a name="FilesName"> Files Name

File names should consist only of lower case letters and dashes to separate the words.
Also as much as possible, you should give explicit and human-understandable names to files.

Our recommendations are the following:
- Section Header files should always be named 'index.md'
- Article files should be named using the main title of the page (without spaces)
- Media files should have a simple name corresponding to the content of the file

Examples:
> **Appropriate**  
> index.md  
> point-light.md  
> point-light-diagram.png  
>
> **Inappropriate**  
> graphics-index.md  
> PointLightFile1.md  
> Img20150902.png  

#  <a name="Formatting"> Formatting
##  <a name="Definitions"> Definitions

When you write your articles, you should be careful of properly defining all the terms that can be
unknown by the user. We can basically distinguish the following three types of terms.

###  <a name="XenkoTerms"> Xenko Terms

These terms are specific to Xenko and absolutely need to be defined. These are terms like Asset, Material,
Live Scripting, Graphic Compositor, etc. You should create a dedicated page for each term defining and 
explaining the concept. Add an uid to the page and link it at least every first occurrence of the word 
in an article. In addition add a shorter version of the definition as metadata in the page. This will be 
used later to create definition tooltips.

Example
```
Material.md:
---
uid: material
Material: List of properties defining how to render an element.
---

# Material

A material can be considered as a list of properties defining how to render an sprite, particle system, or
model.

blablabla ...

HowtoSetDiffuse.md:
# HOWTO Set the diffuse of a model

1. Select the @material use by your model. (<- first reference of the document) 
```

###  <a name="VideoGameTerms"> Video Game Terms

These terms are specific to the game and graphic industry. They can either be defined and explained in
the Xenko documentation if it makes sense (Example: Forward rendering, etc.) in which case we will follow
exactly the same rules as Xenko terms, or explanation can be passed to an external site (wikipedia, etc) 
in which case we will just provide a short version of the definition for the tooltip and the link to
the external website. Only the first occurrence of the page will be linked.

Example
```
---
Shader: block of code defining how to process and render a triangle. (<- inline definition)
---

# Rendering

In Xenko you can choose between @forward-rendering and @deffered-rendering. (<-link to a dedicated page).

Depending on the rendering model the [Shaders](http://wikipedia/shaders) are completely different. 
(<- external reference)

The more complex shaders are blablabla (<- second reference no link)
```

Note: If the expected audience for the page is 'Intermediate' or 'Advanced' basic term definitions can 
be skipped. 

###  <a name="JobTerms"> Job Specific Terms

These terms are specific to a role in the development process. They need to be defined only the when 
the expected audience for the page is wider than just the specific job. Most of the time we will 
define them by using an link to an external page and adding a tooltip definition. Only the first occurrence
of the page has to be defined.

##  <a name="References"> Page References

We recommend you to add cross reference to other documentation pages as much as possible to ease
to reader navigation. 

To add a cross reference proceed as follow:

1. Add a uid at the top of the destination file
2. Everytimes you want to link the page just reference it using the @uid shortcut.

Example
```
material.md:
---
uid: material
---

# Material
...

sprite.md:
For more information about sprite color, read @material.
```

Note: for more information please refer to DocFX documentation.

## <a name="RelatedTopics"> Related Topics

To encourage readers to learn more about a topic and also to ease their navigation,
we recommand you as much as possible to add links to related topics at the bottom of your articles.

For this use the AAA(TODO Virgile) style, as follow: 
> TODO Virgile  
> TODO Virgile  
> TODO Virgile  

## <a name="APIReferences"> API References

A link to the API reference should be added for EACH mention of an API class, interface, function, etc.
To avoid to add too many times the same links, you can replace the function name by an action verb.

Adding a link to a reference API can be done the following way:
> @'MyNamespace.MyClass.MyFunction'

Example:
```
Use the @'SiliconStudio.Xenko.Audio.SoundEffectInstance.Play' function start playing a sound.
Playing an ongoing sound has no effect. Playing a stop sound restart the sound from beginning.
```

## <a name="CodeReference"> Code References

Code samples should be as small as possible, well commented and be properly formatted when included. 
There are two different ways to insert some code in your article. First add the code content directly in your 
article with the proper formatting or add a reference to an existing code file. 
We recommend you to add the code sample directly in your article except when the code sample is used
in several different places. In that case we recommend you to use a reference to a code file.
It can be much more efficient in term of maintenance.

Example:
> **Code directly included in the article**
> 
> \`\`\`cs  
> Asset.Unload(asset);  
> \`\`\`
>
> **Reference to an external code file**  
> \[\!code-csharp\[Main\]\(index.cs?start=5&end=9\)\]  // add line 5 to 9 of file index.cs


## <a name="Placeholders"> Placeholders

For ease of understanding make all placeholders start by 'My'.

Example:
> Content.Load("MyFolder/MyAsset");

## <a name="Labels"> Labels

Labels are optional info displayed at the top of the page so that readers can quickly understand intended target audience.

Please place them right after the top-level title.

There are several kinds of labels:

* Level (Beginner, Intermediate, Advanced) with `label-doc-level`
* Audience (Artist, Programmer, Designer) with `label-doc-audience`
* Platform (iOS, Android, etc...) with `label-doc-platform`

Example:
```
# Title

<span class="label label-doc-level">Beginner</span>
<span class="label label-doc-audience">Artist</span>

## Overview

Lorem ipsum...
```


## <a name="Remarks"> Remarks

Whenever you have explanations that is not necessary for the understanding of a concept but that
can be very useful in application, add them as remarks so that the reader knows that it is extra information
that can be skipped depending on his objective. We provide several types of remarks such as notes, warnings and
tips to give an addition clue to the reader on what kind of extra information he is going to find.  

You can add note, tip and warnings using the following syntax:

```
> [!NOTE]
> Some useful notes
```

Available types:
* NOTE
* TIP
* WARNING

Note that current styling will be improved.

## <a name="PlatformRemarks"> Platform Specific Remarks

Whenever there are explanations or remarks that are specific to a given platform, you should
use the following formatting style to show the reader that the section can be skipped depending on 
the targeted platform.

TODO Virgile styling Android/iOS + example

## <a name="Notices"> Notices

Whenever your page is missing some key information or is out-of-date, you should  
add a notice at the top of the page to inform the reader and add the 🔧 character the page title.

Example 1
```
> [!NOTE]
> 
> This topic is currently missing the following points:
> * sub-topic 1
> * sub-topic 2
```

Example 2D
```
> [!NOTE]
>
> The following elements on this page are out-of-date:
> * element 1
> * element 2
```

TODO virgile do we really want to have the same formating as the notes? shoudn't we have a 
specific formating for this?

## <a name="Media"> Media

You can add media content to your articles using the following syntax:
> \!\[Graphics Compositor Diagram\]\(media/graphics-compositor.png\)  

'Graphic Compositor Diagram' is the message displayed as fall-back if the image file can't be find.
'media/graphics-compositor.png' is the relative path to the file.

For each media file added, we kindly ask you to always include the 'source' file used to create 
your media file next to it. This will allow us to quickly update the images, diagrams and videos 
after some changes happen on the engine side. By source files we mean photoshop files, visio files, 
adobe premiere files, etc. When you create your media, try as much as possible to use either free
or mainstream tools.

Avoid to resize the source data when you create your media. Even if your media needs to be scaled down
to fit the screen, avoid to create scaled-down media by yourself. Instead keep your image in the
original resolution and let the documentation system automatically adapt it for the user. We are asking 
this because at some point we may decide to change the width of our documentation or to provide 
a way to zoom into images. The only exceptions to this are heavy videos. We would like you to create 
a lighter version of the videos to speed up the loading of the pages.

### <a name="Videos"> Videos

As much as possible, we ask you to use the **MP4** format and the **H265** encryption for videos.

Recommenced software to edit the videos is Adobe Premiere.

### <a name="Images"> Images

We ask you to use the **JPEG** format for heavy high resolution images to reduce the load time and
and the **PNG** format all the others (probably most of the images).

For the source files, we prefer the following formats: Photoshop, GIMP, Paint.net.

### <a name="Diagrams"> Diagrams

Diagrams should be rendered as **PNG** or vector image. Since the documentation system automatically 
adjust the size of the images be careful that all text that you include in diagrams are still
readable after size readjustment. When a diagram is too big and can't be reduced, allow the reader to 
click and open it in full size.

You can make diagrams clickable using the following syntax:
TODO virgile

Diagrams can be created with Visio or standard image editing tools.

## <a name="Tables"> Tables

You can add tables to the documentation by following the markdown syntax. Tables can improve the
way information is display but sometimes does not properly scale down. So be sure to try your page
on small resolution screen like Smartphones before submitting your page.

## <a name="Lists"> Lists

When possible prefer a short phrase than a full sentence for each item of a list. This simplifies and
speeds the reading up. Start each item with a capital letter.

When showing a step by step process or when order matters use ordered list rather of bullet points.

Example. 
> **Appropriate**
> 
> How to use lists:
> - Capitalize each first letter
> - Write short phrases
> 
> **Inappropriate**
> 
> How NOT to use lists:
> - You should capitalize the first letter of each item.
> - You should write short phrases

## <a name="Headers"> Headers

The markdown '#' mark should be used to make headers. Only top title of the page should have the h1 style.
All other titles are sub-titles and should be formated into h2+.

Example
> \# Page Top Title: How to write headers.  
> \___  
> \## This is a sub-folder  
> \### This is a sub-sub-folder  
> \### This is another sub-sub-folder  
> \## This is another sub-folder  

## <a name="Capitalization"> Letter Capitalization

When a title is close to a full sentence you should only capitalize first letter of first work.
When a title is just composed of a few words (1 to 5) you should capitalize the few letter of each 
word.

You should NEVER fully capitalize a word inside a sentence except when you want to strongly insist on 
a fact. Words commonly used for this are: ONLY, DO NOT, YES, NO, MAKE SURE TO, BE CAREFUL (TO/ OF).

