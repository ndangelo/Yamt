---
id: 2038
title: 'Chapter 4: Casting Shadows Using Layers with CINEWARE'
date: '2017-01-07T14:18:31-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=2038'
permalink: /chapter-4-casting-shadows-using-layers-with-cineware/
categories:
    - 'DMET 355 ADVANCED WEB DESIGN'
---

<div>[**CHAPTER 4**](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/004_9781315772325_contents.html#con_ch4)

![]()

[**Casting Shadows Using Layers with CINEWARE**](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/004_9781315772325_contents.html#con_ch4)

**Using CINEMA 4D layers offers greater compositing control with CINEWARE. This chapter explores how to use a layer-based workflow to composite realistic shadows created from lighting in CINEMA 4D Lite**

</div><span class="label">![]()</span>[Lights and Shadows in CINEMA 4D](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#ch4.1)

<span class="label">![]()</span>[Creating a Shadow Catcher in After Effects](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#ch4.2)

<span class="label">![]()</span>[Adding Shadows in CINEMA 4D](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#ch4.3)

<span class="label">![]()</span>[Setting Up Layers and Compositing Tags](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#ch4.4)

<span class="label">![]()</span>[Compositing Layers with CINEWARE](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#ch4.5)

<div>## <a id="p106"></a>[Lights and Shadows in Cinema 4D](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/004_9781315772325_contents.html#con_ch4.1)

</div>Light is what illuminates our world. Lighting in CINEMA 4D mimics the properties of light by simulating depth through shading, casting shadows, and interacting with surface materials to produce highlights and reflections. The previous chapters exposed you to adding light objects to a scene, and even a three-point lighting system. Understanding lighting is crucial in producing professional 3D models and animation.

In CINEMA 4D Lite there are four main light types (omni, spot, infinite, and area) and three basic shadow types (shadow maps, raytraced, and area). Each is designed to be used in different lighting situations to simulate a desired real world effect. This chapter focuses on the basics of 3D lighting and shadows.

As you learned, when you add a light object to a CINEMA 4D scene, it appears in the viewport as a starburst icon that has lines pointing in all directions. The icon represents the default light, an **omni light**. This light acts like an exposed light bulb that shines equally in all directions. When rendered, the omni light illuminates in a spherical area, all around the 3D objects. There is also a falloff region of light where it transitions from bright to dark ([Figure 4.1](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_1)).

<div class="center"><div class="display" id="fig4_1">![]()</div></div>**Figure 4.1:** *An omni light appears as a starburst icon and shines equally in all directions*.

The omni light can be changed to a directional, or **spot light**, in the Attributes Manager. This type of light spreads out in a cone shape similar to an actual spot light used in theater and movie productions. A spot light appears as a cone of light in the viewport with nothing outside of the cone illuminated ([Figure 4.2](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_2)). The spread and shape of the light can be controlled using its interactive orange handles in the viewport or modifying its properties in the Attributes Manager.

<div class="center"><div class="display" id="fig4_2">![]()</div></div>**Figure 4.2:** *A spot light is a directional light and appears as a cone of light.*

The third type of light is an **infinite light**. This simulates sunlight that illuminates a 3D model in one direction from an infinite distance with no falloff. An infinite light appears as a point with a single line in the viewport ([Figure 4.3](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_3)). When rendered, it produces a parallel wall of light that shines in all directions.

The last type of light is called an **area light**. This light is basically a rectangle of light, similar to a window in a room ([Figure 4.3](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_3)). The default shape can be changed to whatever you want. Area lights take the longest to render but produce the most realistic lighting on a model in CINEMA 4D.

<div class="center"><div class="display" id="fig4_3"><a id="p107"></a>![]()</div></div>**Figure 4.3:** *An infinite light (left) simulates sunlight and an area light (right)produces a rectangular area of light similar to a window*.

<a id="p108"></a>Shadows help define depth and detail in your 3D scene. By default, lights in CINEMA 4D do not cast any shadows, but you can turn on shadows for light objects in the Attributes Manager. CINEMA 4D has three different types of shadows, and each impact the overall rendering time. These shadow options are located under the **General** tab for a light object ([Figure 4.4](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_4)).

<span class="label">![]()</span>**Shadow Maps (Soft)** produces a nice soft edge around the shadow.

<span class="label">![]()</span>**Raytraced (Hard)** is the simplest type of cast shadow to render producing a rather harsh shadow.

<span class="label">![]()</span>**Area** shadows produce the most realistic shadow but takes a considerably longer time to render.

<div class="center"><div class="display" id="fig4_4">![]()</div></div>**Figure 4.4:** *There are three types of shadows: Shadow Maps (left image), Raytraced (middle image), and Area (right image).*

All shadow options can be modified using the **Shadow** channel in the Attributes Manager. Notice that the Area shadow is a little pixilated. To fix the graininess, increase the **Minimum Samples** value. Keep in mind that each time you increase this number, it costs you in terms of rendering time. You can also adjust the density, which is how dark the shadow is. Notice that the default density value is 100% producing a pitch black shadow. Decreasing this value to around 90% can help your projects look a little bit more realistic ([Figure 4.5](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_5)). Just keep in mind that any of these options impact the rendering time.

<div class="center"><div class="display" id="fig4_5">![]()</div></div>**Figure 4.5:** *The Shadow channel in the Attributes Manager allows you to controlthe shadow*’*s density, color, and accuracy in the final rendered image*.

<div>## <a id="p109"></a>[Creating a Shadow Catcher in After Effects](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/004_9781315772325_contents.html#con_ch4.2)

</div>In the previous chapter, you used the 3D Camera Tracker effect to accurately composite 3D objects from CINEMA 4D Lite over 2D video footage. The only element that was missing was a cast shadow. The following exercise builds on the previous two exercises from [Chapter 3](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/008_9781315772325_ch3.html#ch3). You will use the 3D Camera Tracker to create a **Shadow Catcher** object. This object is created specifically for accepting and compositing shadows with video footage.

<span class="label">![]()</span>*Download ([­h­t­t­p­:­/­/­w­w­w­.f­o­c­a­l­p­r­e­s­s­.c­o­m­/­9­7­8­1­1­3­8­7­7­7­9­3­4­](http://www.focalpress.com/9781138777934)) the* **Chapter\_04.zip** *fileto your hard drive. It contains all the files needed to complete the exercises*.

Locate and play the **Checkerboard.mov** file in the **Completed** folder inside **Chapter\_04** ([Figure 4.6](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_6)). The following exercise provides an introduction to creating a Shadow Catcher object using the 3D Camera Tracker effect. This will enable you to composite realistic shadows created from lights in a CINEMA 4D file onto video footage in After Effects using CINEWARE. Let’s get started.

<div class="center"><div class="display" id="fig4_6">![]()</div></div>**Figure 4.6:** *The 3D model of the pawn casts a shadow using the Shadow Catcher object.*

<div>### Exercise 1: Exporting a Shadow Catcher from After Effects

</div>The first step is to track the camera motion in the video directly in After Effects and then export the tracked data to CINEMA 4D Lite.

<span class="label">**1.**</span>Launch **Adobe After Effects**. It opens an empty project by default. Save the project as **Checkerboard.aep** inside the downloaded **Chapter\_04** folder.

<span class="label">**2.**</span>Double-click in the Project panel to open the Import File dialog box. Locate the **Checkerboard.mov** QuickTime movie in the **Footage** folder inside **Chapter\_04**. Click **Open** to import the footage into the Project panel ([Figure 4.7](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_7)).

<span class="label">**3.**</span>Click and drag the imported file to the**Create a new Composition** icon at the bottom of the Project panel ([Figure 4.8](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_8)). A new composition is created.

<div class="center"><div class="display" id="fig4_7">![]()</div></div>**Figure 4.7:** *Import the QuickTime movie into After Effects.*

<span class="label">**4.**</span>To track the motion, make sure the video layer is selected in the Timeline.

<span class="label">**5.**</span>Select **Animation &gt; Track Camera**. The 3D Camera Tracker effect is applied to the layer and it automatically begins analyzing each frame of the video. Once the automatic analysis is complete, tiny cross track points appear on top of the video.

<div class="center"><div class="display" id="fig4_8">![]()</div></div>**Figure 4.8:** *Create a new Composition in the Project panel using the imported QuickTime movie.*

<span class="label">**6.**</span>To position the bullseye target, you need to select at least three track points. For this exercise, hold down the Shift key and Shift-select the track points around the middle dark square on the checkerboard ([Figure 4.9](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_9)).

<div class="center"><div class="display" id="fig4_9">![]()</div></div>**Figure 4.9:** *Select the track points to position the bullseye target.*

<span class="label">**7.**</span>To move the target, position the mouse cursor over the center of the bullseye. Click and drag the target to center it better on the checkerboard ([Figure 4.10](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_10)).

<div class="center"><div class="display" id="fig4_10"><a id="p110"></a>![]()</div></div>**Figure 4.10:** *Position the bullseye target within the dark square on the checkerboard.*

<span class="label">**8.**</span><a id="p111"></a>The center of the bullseye target will become the origin point for the 3D Camera Tracker. With the target positioned, right-click (Windows) or Control-click (Mac OS) on the bullseye target and choose **Set Ground Plane and Origin** ([Figure 4.11](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_11)).

<div class="center"><div class="display" id="fig4_11">![]()</div></div>**Figure 4.11:** *Record a ground plane and origin point for the 3D Camera Tracker effect.*

<span class="label">**9.**</span>Right-click (Windows) or Control-click (Mac OS) on the bullseye target again. This time select **Create Shadow Catcher, Camera, and Light** ([Figure 4.12](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_12)). After Effects creates a 3D camera and light layer in the Timeline. The light is positioned at a location similar to the light source used to shoot the video. A Shadow Catcher layer is also added to the Timeline. This is a solid layer that will be used to accept the cast shadows ([Figure 4.13](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_13)).

<div class="center"><div class="display" id="fig4_12">![]()</div></div>**Figure 4.12:** *Create a Shadow Catcher, Camera, and Light layer in the Timeline.*

<div class="center"><div class="display" id="fig4_13">![]()</div></div>**Figure 4.13:** *Create a Shadow Catcher layer using the 3D Camera Tracker effect.*

<span class="label">**10.**</span><a id="p112"></a>As you learned in [Chapter 3](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/008_9781315772325_ch3.html#ch3), not only can you import CINEMA 4D files into tracked video footage, but you can also export your composition from After Effects as a CINEMA 4D file. To do this, select**File &gt; Export &gt; MAXON CINEMA 4D Exporter**.

<span class="label">**11.**</span>Save the project as **AE\_ShadowCatcher.c4d** in the **Footage** folder inside the **Chapter\_04** folder. Click **Save** ([Figure 4.14](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_14)).

<div class="center"><div class="display" id="fig4_14">![]()</div></div>**Figure 4.14:** *Export the After Effects project as a CINEMA 4D file.*

<span class="label">**12.**</span>In order to match the lighting and shadows in the video, let’s export the current frame from After Effects. Select**Composition &gt; Save Frame As &gt; Photoshop Layers** ([Figure 4.15](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_15)). In the Save dialog box, save the file in the **Footage**folder. Click **Save**.

<div class="center"><div class="display" id="fig4_15">![]()</div></div>**Figure 4.15:** *Save the current frame of the composition as a Photoshop file.*

<span class="label">**13.**</span><a id="p113"></a>Save your After Effects project file.

<span class="label">**14.**</span>Double-click in the Project panel to open the Import File dialog box.

<span class="label">**15.**</span>Locate the **AE\_ShadowCatcher.c4d** exported file in the **Footage** folder inside **Chapter\_04**. Click **Open** to import the footage into the Project panel.

<span class="label">**16.**</span>To open this file in CINEMA 4D Lite, single-click on the footage to highlight it in the Project panel. Select**Edit &gt; Edit Original** ([Figure 4.16](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_16)).

<div class="center"><div class="display" id="fig4_16">![]()</div></div>**Figure 4.16:** *Open the exported CINEMA 4D file.*

<div>## [Adding Shadows in CINEMA 4D](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/004_9781315772325_contents.html#con_ch4.3)

</div>Let’s jump over to CINEMA 4D Lite and take a look at the exported file from After Effects. In the Objects Manager there is a null object with the same name as the After Effects composition. Inside the null object is a **3D Tracker Camera, Shadow Catcher 1**, and **Light 1** object ([Figure 4.17](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_17)). The viewport is automatically set to display what the exported camera object is seeing. The Shadow Catcher appears as a 2D plane set at the recorded origin point.

<div class="center"><div class="display" id="fig4_17">![]()</div></div>**Figure 4.17:** *The exported data is displayed in the Objects Manager.*

<div>### Exercise 2: Lights and Shadows

</div><span class="label">**1.**</span>Let’s add the 3D model of the pawn chess piece to the scene. This model has already been created in a separate CINEMA 4D file.

<span class="label">![]()</span>In the Objects Manager, select **File &gt; Merge Objects**.

<span class="label">![]()</span>Locate and select the **Pawn.c4d** file inside the **Footage** folder in **Chapter\_04**.

<span class="label">![]()</span>Click**Open** ([Figure 4.18](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_18)).

<div class="center"><div class="display" id="fig4_18">![]()</div></div>**Figure 4.18:** *Merge the 3D chess piece into the exported CINEMA 4D file.*

The object is added to the Objects Manager and appears at the origin point in the viewport ([Figure 4.19](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_19)). The pawn is a lathed object. As you learned in [Chapter 2](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/007_9781315772325_ch2.html#ch2), a Lathe NURB is created by rotating a spline around an axis to produce a solid, symmetrical object.

<div class="center"><div class="display" id="fig4_19">![]()</div></div>**Figure 4.19:** *The merged Lathe NURB appears at the origin point in the viewport.*

<span class="label">**2.**</span>The scale of the pawn chess piece is a little small for the scene. Go to the Attributes Manager and click on the **Coord**. tab. Increase the scale of the object to **2** for X, Y, and Z ([Figure 4.20](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_20)).

<div class="center"><div class="display" id="fig4_20"><a id="p114"></a>![]()</div></div>**Figure 4.20:** *Increase the scale of the 3D object in the Attributes Manager.*

<span class="label">**3.**</span><a id="p115"></a>Go to the Objects Manager and click and drag the **Lathe NURBS** into the **Checkerboard** Null object.

<span class="label">**4.**</span>Go to the Materials Manager. A material for the Shadow Catcher was created when the file was exported from After Effects. Select **Create &gt; New Material** to add a new material to the manager’s panel. This will be the background reference image used to match the cast shadows in the video footage.

<span class="label">**5.**</span>Double-click on the**Mat** icon to open the Material Editor dialog box.

<span class="label">**6.**</span>In the **Color** channel, make the following changes ([Figure 4.21](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_21)):

<span class="label">![]()</span>Click on the **Texture** arrow and select **Load Image** from the pop-up menu.

<span class="label">![]()</span>Locate the **Checkerboard.psd** file in the **Footage** folder in **Chapter\_04**. Click **Open**.

<span class="label">![]()</span>Rename the texture to **Background** and press **Return**.

<span class="label">![]()</span>When you are done, close the Material Editor dialog box.

<div class="center"><div class="display" id="fig4_21">![]()</div></div>**Figure 4.21:** *Load an image as a material using the texture parameter*.

<span class="label">**7.**</span>Locate the Floor icon above the viewport window and left-click on the **Background** icon to add the object to the Objects Manager ([Figure 4.22](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_22)).

<div class="center"><div class="display" id="fig4_22">![]()</div></div>**Figure 4.22:** *Add a Background object to the Objects Manager.*

<span class="label">**8.**</span>Click and drag the **Background material** from the Materials Manager and drop it onto the **Background name** in the Objects Manager.

![]()

<span class="label">**9.**</span><a id="p116"></a>Click on the **Render View** icon above the viewport to render the scene in the viewport window. This is a quick preview of what the render will look like in CINEWARE ([Figure 4.23](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_23)). Notice that the exported light is automatically set to cast a shadow onto the Shadow Catcher surface.

<div class="center"><div class="display" id="fig4_23">![]()</div></div>**Figure 4.23:** *Render a preview of the scene in the viewport.*

The shading on the pawn is calculated based on the angle of its surface. The exported light from After Effects provides a simple lighting setup with a key light illuminating one side of the object. While this creates the strong shading and definition of volume for the object, the contrast is too great. The dark side of the pawn is completely black since no light is hitting it.

In reality this side of the pawn would still be illuminated, just not as much as the brightly lit side, because of light bouncing around the room and hitting the dark side of the object. Bounce light is not calculated in CINEMA 4D, so you have to create it yourself. To do this, you need to add additional light objects pointing in the opposite direction to illuminate the shadow areas.

![]()

<span class="label">**10.**</span>Click on the **Light** icon to add a light source to your 3D scene. In the Objects Manager, rename the light to **Side Light**. Click and drag the object into the **Checkerboard** Null object.

<span class="label">**11.**</span>With the **Side Light** object selected in the Objects Manager, go to the Attributes Manager and click on the**General** tab.

<span class="label">![]()</span>Change the **RGB Color** values to R = **255**, G = **230**, B = **205**.

<span class="label">![]()</span>Decrease the **Intensity** value to**90%**.

<span class="label">**12.**</span>In the Attributes Manager, click on the**Coord**. tab.

<span class="label">![]()</span>Set the **X-Position** to **−1000 cm**.

<span class="label">![]()</span>Set the **Y-Position** to **1000 cm**.

<span class="label">![]()</span>Set the **Z-Position** to **−1500 cm**.

![]()

<span class="label">**13.**</span><a id="p117"></a>Click on the **Light** icon to add a third light source to your 3D scene. In the Objects Manager, rename the light to **Rim Light**. Click and drag the object into the **Checkerboard** Null object.

<span class="label">**14.**</span>With the **Rim Light** object selected in the Objects Manager, go to the Attributes Manager and click on the **General** tab.

<span class="label">![]()</span>Increase the Intensity value to 110%.

<span class="label">![]()</span>Set the Shadows property to Shadow Maps (Soft).

<span class="label">**15.**</span>In the Attributes Manager, click on the **Coord**. tab.

<span class="label">![]()</span>Set the **X-Position** to **400 cm**.

<span class="label">![]()</span>Set the **Y-Position** to **2000 cm**.

<span class="label">![]()</span>Set the **Z-Position** to **1100 cm**.

![]()

<span class="label">**16.**</span>Click on the **Render View** icon again to render the scene ([Figure 4.24](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_24)). The shading on the pawn’s surface now simulates how light bouncing around the room would affect it. The cast shadow under the pawn will be used to mimic the reflection of the checkers seen in the video footage.

<div class="center"><div class="display" id="fig4_24">![]()</div></div>**Figure 4.24:** *Add more light objects to simulate bounce light in the scene.*

<span class="label">**17.**</span>Go to the Materials Manager. Select **Create &gt; New Material**. A preview of the new material appears in the manager’s panel.

<span class="label">**18.**</span>Double-click on the **Mat** icon to open the Material Editor dialog box.

<span class="label">**19.**</span>In the **Color** channel, make the following changes:

<span class="label">![]()</span>Change the **RGB Color** values to R = **247**, G = **219**, B = **173**.

<span class="label">![]()</span>Rename the texture to **Pawn** and press **Return**.

You will also need to adjust the specular highlights. **Specular light** refers to the highlights on reflective objects, such as billiard balls. They appear as bright spots on a surface, at a point where the light source hits it direct

<span class="label">**20.**</span><a id="p118"></a>In the **Specular** channel make the following changes ([Figure 4.25](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_25)):

<span class="label">![]()</span>Decrease the **Width** value to **30%**.

<span class="label">![]()</span>Increase the **Height** value to **40%**.

<span class="label">![]()</span>Increase the **Inner Width** value to **10%**.

<div class="center"><div class="display" id="fig4_25">![]()</div></div>**Figure 4.25:** *Adjust the specular highlight settings in the Material Editor*.

<span class="label">**21.**</span>When you are done, close the Material Editor panel.

<span class="label">**22.**</span>Click and drag the **Pawn** material from the Materials Manager and drop it onto the **Lathe NURBS name** in the Objects Manager ([Figure 4.26](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_26)).

<div class="center"><div class="display" id="fig4_26">![]()</div></div>**Figure 4.26:** *Apply the texture to the Lathe NURBS object in the Objects Manager*.

![]()

<span class="label">**23.**</span><a id="p119"></a>Click on the **Render View** icon again to render the scene ([Figure 4.27](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_27)). When compared to the specular highlights on the checkers, there are too many highlights on the 3D model. Each highlight comes from a placed light object. Fortunately, you can turn off the specular highlights for a light object.

<div class="center"><div class="display" id="fig4_27">![]()</div></div>**Figure 4.27:** *Render the image to view the new material added to the pawn model.*

<span class="label">**24.**</span><a id="p120"></a>Go to the Objects Manager and select the **Rim Light** object.

<span class="label">**25.**</span>In the Attributes Manager, go to the**General** tab. Uncheck the checkbox for **Specular** to deactivate the highlight created by this light object ([Figure 4.28](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_28)).

<div class="center"><div class="display" id="fig4_28">![]()</div></div>**Figure 4.28:** *Turn off the specular highlights for the Rim Light object.*

<span class="label">**26.**</span>Go to the Objects Manager and select the**Side Light** object.

<span class="label">**27.**</span>In the Attributes Manager, go to the **General** tab. Uncheck the checkbox for **Specular** to deactivate the highlight created by this light object.

![]()

<span class="label">**28.**</span>Click on the **Render View** icon again to render the scene ([Figure 4.29](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_29)).

<div class="center"><div class="display" id="fig4_29">![]()</div></div>**Figure 4.29:** *Render the scene in the viewport.*

<span class="label">**29.**</span>With the specular highlight set correctly, let’s also smooth out the wireframe mesh of the pawn chess piece a little. Go to the Objects Manager and select the**Lathe NURBS** object.

<span class="label">**30.**</span>Hold down the Option key and select the**HyperNURBS** from the NURBS object palette above the viewport ([Figure 4.30](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_30)). Holding down the Option key automatically makes the Lathe NURBS a child of the HyperNURBS.

<div class="center"><div class="display" id="fig4_30">![]()</div></div>**Figure 4.30:** *Add a HyperNURBS object to the scene.*

<span class="label">**31.**</span>Locate the three clapboard icons in the top center of the user interface. Click on the icon to the right that has the sprocket to open the Render Settings.

![]()

<span class="label">**32.**</span>Click on Anti-Aliasing to modify its render settings on the right side of the dialog box. Change the **Anti-Aliasing** setting from **Geometry** to **Best**.

<span class="label">**33.**</span><a id="p121"></a>Even though the Background object does not render in CINEWARE, it can produce a white fringe around the 3D model due to the anti-aliasing. To prevent this, go to the Objects Manager and double-click on the bottom gray circle next to**Background** to change its color to red ([Figure 4.31](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_31)).

<span class="label">**34.**</span>Save your CINEMA 4D Lite file. Select **File &gt; Save**.

<span class="label">**35.**</span>Jump back to After Effects.

<span class="label">**36.**</span>Click and drag the **AE\_ShadowCatcher.c4d** file from the Projects panel to the Timeline. Position it at the top of the layers in the Timeline.

<div class="center"><div class="display" id="fig4_31">![]()</div></div>**Figure 4.31:** *Turn off the Background object’s render view button in the Objects Manager.*

<span class="label">**37.**</span>Turn off the visibility for the **Light 1, Shadow Catcher 1**, and the **3D Tracker Camera** layers in the Timeline. Those objects and keyframes are now stored inside the CINEMA 4D layer ([Figure 4.32](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_32)).

<div class="center"><div class="display" id="fig4_32">![]()</div></div>**Figure 4.32:** *Position the CINEMA 4D layer at the top of the Timeline. Turn off the visibility for the Light 1, Shadow Catcher 1, and 3D Tracker Camera layers.*

<span class="label">**38.**</span>Change the CINEWARE **Renderer** to **Standard (Final)** in the Effect Controls panel ([Figure 4.33](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_33)). The next exercise focuses on adding layers in CINEMA 4D.

<div class="center"><div class="display" id="fig4_33">![]()</div></div>**Figure 4.33:** *Change the render settings in the CINEWARE Effect Controls panel.*

<div>## <a id="p122"></a>[Setting Up Layers and Compositing Tags](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/004_9781315772325_contents.html#con_ch4.4)

</div>Your project is almost done. The only problem is the Shadow Catcher renders as a white solid in the Composition panel. To solve this, you need to create layers to separate the Shadow Catcher from the actual 3D model of the pawn. CINEMA 4D provides a layer system that is both very powerful and easy to use. When combined with CINEWARE, layers offer even more flexibility in compositing and adding effects to your motion graphics.

<div>### Exercise 3: Creating New Layers

</div><span class="label">**1.**</span>Save your After Effects project. Jump back to CINEMA 4D Lite.

<span class="label">**2.**</span>Click on the **Layers** tab directly under Attributes on the right side of the interface. This opens the Layers Manager on top of the Attributes Manager ([Figure 4.34](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_34)).

<div class="center"><div class="display" id="fig4_34">![]()</div></div>**Figure 4.34:** *Open the Layers Manager in CINEMA 4D.*

<span class="label">**3.**</span>In the Layers Manager select **File &gt; New Layer**. Rename the new layer **Pawn**.

<span class="label">**4.**</span>Select **File &gt; New Layer** again. Rename the new layer **Shadow** ([Figure 4.35](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_35)).

<div class="center"><div class="display" id="fig4_35">![]()</div></div>**Figure 4.35:** *Create two new layers: one for the 3D object and one for the Shadow Catcher object in the Layers Manager.*

<span class="label">**5.**</span>Go to the Objects Manager. Select the **Shadow Catcher 1** object to highlight it.

<div class="center"><div class="display" id="fig4_36">![]()</div></div>**Figure 4.36:** *Add the Shadow Catcher object to the Shadow layer.*

<span class="label">**6.**</span>In the Objects Manager, select **Edit &gt; Add to Layer &gt; Shadow** ([Figure 4.36](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_36)).

<span class="label">**7.**</span>Select the **HyperNURBS** object to highlight it. When assigning layers, it is important to include all children. In the Objects Manager, select **Edit &gt; Select Children** to select the HyperNURBS children.

<span class="label">**8.**</span>In the Objects Manager, select **Edit &gt; Add to Layer &gt; Pawn**. Each layer is color coded and the assigned layer appears to the right of each object’s name in the Objects Manager ([Figure 4.37](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_37)).

<div class="center"><div class="display" id="fig4_37">![]()</div></div>**Figure 4.37:** *Add the HyperNURBS object and all of its children to the Pawn layer.*

Now that you have successfully separated the 3D object from the Shadow Catcher using layers in CINEMA 4D, there is still a problem that needs to be solved when using CINEWARE. In order for CINEWARE to render the cast shadows on the Shadow Catcher, it needs the shadow-casting object (pawn) to exist on the same layer. So how do you solve this since you just placed the pawn model on a separate layer?

<span class="label">**9.**</span>Select the **HyperNURBS** object in the Objects Manager to highlight it.

<span class="label">**10.**</span>Click and hold the array icon above the viewport to reveal the pop-up palette of modeling objects. While this palette is open, left-click on the **Instance** icon to add a copy of the pawn 3D model to the Objects Manager ([Figure 4.38](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_38)).

<div class="center"><div class="display" id="fig4_38">![]()</div></div>**Figure 4.38:** *Create a copy of the 3D object using the Instance generator.*

<span class="label">**11.**</span>Click and drag the **HyperNURBS Instance** object into the **Checkerboard** null object. Position it above the **Shadow Catcher 1** object.

<span class="label">**12.**</span><a id="p123"></a>In the Objects Manager, select **Edit &gt; Add to Layer &gt; Shadow** ([Figure 4.39](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_39)). We don’t want the Instance to render in the After Effects composition, only the shadow it casts. To fix this, you need to add a **Compositing Tag** to the object in the Objects Manager. Compositing tags provide additional settings that allow you to control how an object is rendered in the final image.

<div class="center"><div class="display" id="fig4_39">![]()</div></div>**Figure 4.39:** *Add the instance object to the Shadow layer.*

<span class="label">**13.**</span>Make sure the **HyperNURBS Instance** is still selected in the Objects Manager.

<span class="label">**14.**</span>Select **Tags &gt; CINEMA 4D Tags &gt; Compositing** ([Figure 4.40](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_40)).

<div class="center"><div class="display" id="fig4_40">![]()</div></div>**Figure 4.40:** *Add a Compositing Tag to the instance object.*

<span class="label">**15.**</span><a id="p124"></a>Make sure the **Compositing Tag** is selected in the Objects Manager.

<span class="label">**16.**</span>Click on the **Attributes** tab directly above Layers to open the Attributes Manager on top of the Layers Manager.

<span class="label">**17.**</span>In the Attributes Manager, uncheck the checkbox for **Seen by Camera** to remove the object from the final render, but keep its cast shadow ([Figure 4.41](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_41)).

<div class="center"><div class="display" id="fig4_41">![]()</div></div>**Figure 4.41:** *Change the compositing settings for the instance object.*

<span class="label">**18.**</span>Before you jump back to After Effects, select the **HyperNURBS Instance** again in the Objects Manager.

<span class="label">**19.**</span>Go to the Attributes Manager and click on the checkbox for **Render Instance**. This will assist in speeding up the rendering time by rendering the instance rather than keeping it in RAM ([Figure 4.42](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_42)).

<div class="center"><div class="display" id="fig4_42">![]()</div></div>**Figure 4.42:** *Render instance to save on RAM*.

<span class="label">**20.**</span>Save your CINEMA 4D Lite file. Select **File &gt; Save**.

With the CINEMA 4D layers and compositing tags in place, the last stage in this workflow is to use CINEWARE to effectively blend the shadows with the video footage. CINEWARE offers the ability to isolate each layer in the CINEMA 4D file within the After Effects composition.

<div>## <a id="p125"></a>[Compositing Layers with CINEWARE](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/004_9781315772325_contents.html#con_ch4.5)

</div>In After Effects you will use CINEWARE and Blending Modes to effectively composite the cast shadow with the video background.

<div>### Exercise 4: Separating Layers Using CINEWARE

</div><span class="label">**1.**</span>Jump back to After Effects. Go to the Timeline and select the **AE\_ShadowCatcher.c4d** layer.

<span class="label">**2.**</span>In CINEWARE, click on the checkbox for **CINEMA 4D Layers** under the Project Settings. Click on the **Set Layers** button.

<span class="label">**3.**</span>Uncheck the checkbox for the **Pawn** layer ([Figure 4.43](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_43)). Click **OK**. The pawn 3D model disappears in the Composition panel leaving only the Shadow Catcher shape layer and the cast shadow visible.

<div class="center"><div class="display" id="fig4_43">![]()</div></div>**Figure 4.43:** *Turn off the Pawn layer in CINEWARE.*

<span class="label">**4.**</span>In the Timeline, click on the **Toggle Switches/Modes** button to display the Mode options. Change the layer’s mode from**Normal** to **Multiply** ([Figure 4.44](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_44)). The white shape vanishes leaving only the cast shadow blended on top of the video.

<div class="center"><div class="display" id="fig4_44">![]()</div></div>**Figure 4.44:** *Change the layer’s blending mode to Multiply.*

<span class="label">**5.**</span>Click and drag another copy of the **AE\_ShadowCatcher.c4d** file from the Projects panel to the Timeline. Position it at the top of the layers in the Timeline.

<span class="label">**6.**</span>In CINEWARE, click on the checkbox for **CINEMA 4D Layers** under the Project Settings. Click on the **Set Layers** button.

<span class="label">**7.**</span>Uncheck the checkbox for the **Shadow** layer. Click **OK**.

<span class="label">**8.**</span><a id="p126"></a>Change the CINEWARE **Renderer** to **Standard (Final)** ([Figure 4.45](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_45)).

<div class="center"><div class="display" id="fig4_45">![]()</div></div>**Figure 4.45:** *Composite a copy of the Pawn layer on top of the Shadow layer.*

<span class="label">**9.**</span>The 3D object is a little too crisp and clean for the composite. Select **Effect &gt; Blur &amp; Sharpen &gt; Gaussian Blur** to add a small blur to the edges.

<span class="label">**10.**</span>Increase the **Blurriness** value a small increment to **0.5** ([Figure 4.46](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_46)).

<div class="center"><div class="display" id="fig4_46">![]()</div></div>**Figure 4.46:** *Add a small blur to the edges of the 3D object.*

<span class="label">**11.**</span><a id="p127"></a>Let’s do the same for the layer that holds the cast shadow. Select the CINEMA 4D layer in the Timeline.

<span class="label">**12.**</span>Select **Effect &gt; Blur &amp; Sharpen &gt; Gaussian Blur** to add a blur to the edges.

<span class="label">**13.**</span>Increase the **Blurriness** value to **2.0** ([Figure 4.47](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_47)).

<div class="center"><div class="display" id="fig4_47">![]()</div></div>**Figure 4.47:** *Add a blur to the cast shadow layer in the Timeline.*

Since the CINEMA 4D file becomes a 2D layer in a composition, effects can be applied to it just like any other layer. Experiment with other effects to visually change the pawn’s and cast shadow’s composite. Experiment using the Hue/ Saturation effect to completely change the colors. Use the Curves or Levels effect to adjust each layer’s contrast. When you are done, render the project.

<span class="label">**14.**</span>Make sure the Timeline or Composition panel is highlighted.

<span class="label">**15.**</span>Select **Composition &gt; Add to Render Queue**. This opens the Render Queue. It is a new tab that sits on top of the Timeline panel.

<span class="label">**16.**</span>In the Output To dialog box select the **Chapter\_04** folder on your hard drive as the final destination for the rendered movie. If this dialog box does not appear, click on**Checkerboard.mov** next to Output To.

<span class="label">**17.**</span>Click on **Lossless** next to Output Module.

<span class="label">**18.**</span>Set the format to **QuickTime** movie.

<span class="label">**19.**</span>Under Format Options, set the compression setting to **H.264** or **MPEG-4 Video**.

<span class="label">**20.**</span>Set the Audio setting to **Audio Output Off** using the drop-down menu.

<span class="label">**21.**</span><a id="p128"></a>Click **OK** to close the Output Module Settings dialog box.

<span class="label">**22.**</span>Click the **Render** button.

<span class="label">**23.**</span>When the render is done, go to the**Chapter\_04** folder on your hard drive. Launch the QuickTime movie ([Figure 4.48](https://jigsaw.vitalsource.com/books/9781317678045/epub/OEBPS/009_9781315772325_ch4.html#fig4_48)).

<div class="center"><div class="display" id="fig4_48">![]()</div></div>**Figure 4.48:** *The final rendered QuickTime movie.*

<div>## Summary

</div>This chapter explored how to use a layer-based approach in compositing CINEMA 4D files inside of After Effects. You used the 3D camera tracking effect in After Effects to create a Shadow Catcher object. The benefit of using this feature is the ease which you can composite realistic shadows onto video footage. What makes this work is the use of layers in CINEMA 4D. Layers are very powerful and quite useful in compositing 3D models into your After Effects projects. CINEWARE allows you to isolate each layer within a CINEMA 4D file opening up endless possibilities for applying effects.