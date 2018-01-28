---
layout: post
title:  How to use custom markers with Vuforia
date: 2018-01-28 15:20:00
description: Learn how to any marker in Vuforia, including maps!
---

### Prerequisites:

1. A Web Browser
2. Unity
4. Vuforia Account

### Quick Steps:

1. Start with a Vuforia Enabled project
2. Create a new Vuforia Target Database
2. Create and Upload an Image
3. Download and Import the Database in Unity
4. Set the AR Camera to use the new database
5. Create a Target Image Asset with the database texture

### A more in depth walk through.

This tutorial will take you from the Vuforia [Tracked Marker Tutorial](http://adamrtomkins.github.io/2018/01/18/Unity_Vuforia.html) unity project,to using your own custom markers in around 5 minutes. 


#### 1. Set up your Project 

We're going to assume that you have already set up the Vuforia package and have a Vuforia Account and License key. 

<div class="img_row">
	<img style="max-height: 100%"  src="{{ site.baseurl }}/img/Blogs/Terrain/Select_Terrain.PNG" alt="Selecting Terrain" title="Terrain Selection"/>
</div>


#### 2. Create your Marker Images

We are going to require a set of visually distinct Marker Images. I am going to take the opportunity to create a set of map images from the wonderful resource, [Stamen Maps](maps.stamen.com/), using the Toner Setting. As I will be using this in a Sheffield based AR project, I'll create a Sheffield map.

<div class="img_row">
	<img style="max-height: 100%"  src="{{ site.baseurl }}/img/Blogs/Custom_Markers/Sheffield_Map.PNG" alt="Sheffield Map" title="Sheffield Map Marker"/>
</div>

 #### Create your Target Database
 
 Once you have your target images, you need to head over to [Vuforia](https://www.vuforia.com), and open up the Developer Pages. You should see a list of your previous projects, you can use a previous one, or start a new one up.
 
 When you're looking at a project, click Target Manager in the Navigation Bar. Here we can add a new Database.
 
 <div class="img_row">
	<img style="max-height: 100%"  src="{{ site.baseurl }}/img/Blogs/Custom_Markers/Create_Database.PNG" alt="Create a new Database" title="Create a new Database"/>
</div>

Click Add Database, Give it a name (Maps for me) and select Device Database. This means the database will be stored on the AR device, and will not require any cloud access. This is faster to recognise, but cant be as easily updated.

Once you're created on, Open it up and click Add Target. Here you will want to select "Single Image", upload your file and set the image scene width. Remember that 1 is 1 meter in the scene, and would require printing a meter squared for your target. I'm going to put 0.1, to enable a 10cm target image. Give your Image a Unique name, and press Add.

<div class="img_row">
	<img style="max-height: 100%"  src="{{ site.baseurl }}/img/Blogs/Custom_Markers/Add_Target.PNG" alt="Add Target" title="Add Target"/>
</div>

This will upload your Image and take you back to the database view. Now if you open up the Image, you can see the marker, and inspect the visual features using Show Features, and see the Augmentable Rank. If you get a low rank, you can change the images with "Update Target".

 <div class="img_row">
	<img style="max-height: 100%"  src="{{ site.baseurl }}/img/Blogs/Custom_Markers/Target_Features.PNG" alt="Inspect the Target Features" title="Target Features"/>
</div>

#### Import the Database into Unity
 
You can go ahead and add as many images as you need now, before downloading the database. You can always re-download the database later if you see you need new images.
 
When you're finished creating you database, you can click "Download Database" and Select the Unity option. This will compile your database, and may take a moment if you've added many images. When its finished, download the package, and import it into your Unity project.

When the database is imported, you can enable it by Clicking on your AR camera, and opening the Vuforia Configuration, and enabling the Database you imported. 

 <div class="img_row">
	<img style="max-height: 100%"  src="{{ site.baseurl }}/img/Blogs/Custom_Markers/Add_Database.PNG" alt="Add Database" title="Add Database"/>
</div>

#### Use your Custom Marker

Finally you can set your Image Target up to use your new Database and Marker by setting the Database and Image target to your new marker, in the inspector window.

 <div class="img_row">
	<img style="max-height: 100%"  src="{{ site.baseurl }}/img/Blogs/Custom_Markers/Use_Marker.PNG" alt="Use Custom Marker" title="Use Custom Marker"/>
</div>
 
And you should now see your custom marker on your target Image. Print out your markers, and git it a shot.

 <div class="img_row">
	<img style="max-height: 100%"  src="{{ site.baseurl }}/img/Blogs/Custom_Markers/Custom_Marker.PNG" alt="Custom Marker" title="Custom Marker"/>
</div>

You can see it running here in Unity, with much better tracking than the astronaut, displaying a Arts Tower Mesh, a famous Sheffield landmark. You can see how to import SketchUp models like the Arts tower, in the next article.

 <div class="img_row">
	<img style="max-height: 100%"  src="{{ site.baseurl }}/img/Blogs/Custom_Markers/ArtsTower.PNG" alt="ArtsTower" title="The Sheffield Arts Tower"/>
</div>