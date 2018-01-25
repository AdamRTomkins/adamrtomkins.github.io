---
layout: post
title:  Wearable AR with the Aryzon Headset
date: 2018-01-20 12:34:56
description: Unleash yourself from the screen, and build your first AR App with the Aryzon Headset
---

# Wearable AR with the Aryzon Headset

The future of AR isn't looking at the screen, its looking at the world, and having the digital work look back at you. While commercial AR headsets are cost prohibitive for the hobby developer, the Aryzon gives a good entry-level experience to get your toes wet.

The Aryzon headset is powered by your phone, akin to the Google Cardboard, so its not to far from the previous AR examples, using Vuforia and Unity.

## Prerequisites:

1. A Web Browser
2. A Model Viewer (For me, Unity 2017.2)
3. Aryzon Headset

### Quick Steps:
Follow these steps

1. Open a new project
2. Set build settings to Andoid or iOS
3. Download and import the Unity package
4. Using Vuforia? Check out the Vuforia Readme.txt in the Aryzon folder and the Vuforia sample scene.
Open one of the sample scenes in the Aryzon folder or add the Aryzon prefab to the scene and remove the MainCamera.
5. Test it.

### A more in depth walk through.

This project shouldn't take more that 20 minutes to get up and running, we're assuming you have an Aryzon headset, and the supplied target images, we'll be using the big white circle for this one.

[IMAGE: Headset and Target]

#### Start A new Project 

Firlstly, we'll start out with a standard new  project, in 3D, and save it as Aryzon Tutorial. 

<div class="img_row">
	<img style="max-height: 100%"  src="{{ site.baseurl }}/img/Blogs/Tracked_AR_Vuforia/Unity_Sheffield_AR.jpeg" alt=Sheffield in AR" title="Sheffield_in_AR"/>
	
</div>

#### 2. Set the project Build

Open up the build settings and switch the platform to Android. Then we will need to set up some extra settings in the player settings.

First set the Package Name, under Other Settings>Identification, to something recognisable, I'll go for ART.TomkiStudions.AryzonDemo.

Net we have to Enable Vuforia Augmented Reality under XR setting, and disable 'Android TV compatability' under Other Settings.

#### 3. Import Aryzon Package

First you will have to download the Aryzon-Unity package from (here)[http://download.aryzon.com/AryzonUnitypackage.zip], and extract the contents. after this you can import the package using 

Assets > Import Package > Custom Package and locating the extracted AryzonUnitypackage.

this will prompt you to import the package, where you should import the entirety of it. It will appear in your project heirarchy under the Aryzon Folder.

#### 4. Add the Aryzon Camera

The Aryzon package comes with some useful prefabs, the most important is the Aryzon Camera, this subsumes the Vuforia AR Camera. We can add it by opening the Example Scene called 'Vuforia Tracking' in the Aryzon> Sample Scenes Folder, and copying the camera called Aryzon to our main scene. We should now delete the Main Camera.

If we look at the Scene view, we should see a black screen, divided in two by a white line. This corresponds to the doubling of the image required for depth perception in the Aryzon headset. 

#### 5. Add the Tracked Target

While we have the Sample scene open we can copy across the ImageTarget, which comes pre-loaded with the supplied Aryzon tracking disk.

From here on we can add a child object to render when the Image is detected, and Test it out!

5. Fixing Compile errors

At this point, I ran into some compile errors in the Console, which stated:

Assets/Vuforia/Scripts/DefaultSmartTerrainEventHandler.cs(28,12): error CS0246: The type or namespace name `PropBehaviour' could not be found. Are you missing an assembly reference?

There are a few of these, all surrounding the DefaultSmartTerrainEventHandler. As we write this the Aryzon SDK is still in development, and bugs are to be expected. In this case we can fix these errors by removing the DefaultSmartTerrainEventHandler entirety. In your project view, head to Assets/Vuforia/Scripts/ and delete the DefaultSmartTerrainEventHandler.cs file, and try to recompile.

For me I get more errors:

Assets/Vuforia/Editor/Scripts/OpenSourceInitializer.cs(47,48): error CS0246: The type or namespace name `DefaultSmartTerrainEventHandlerPlaceHolder' could not be found. Are you missing an assembly reference?

 This Time its in the OpenSource initializer. So lets go ahead and remove that too from Assets/Vuforia/Editor/Scripts/.


[IMAGE: Scene Screen ]

 
Hopefully now, you can test it! We expect to see a black screen, with the Aryzon overlay until we detect and object. Unlike the traditional AR behaviour, we do not see a pass through, that is because the Aryzon headset has optical pass through with a digital overlay. We will build for a phone next, and give it a whirl.

