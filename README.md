<img width="200" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/drawlab_icon_1.svg">

## Introduction:  
A new type of vector app for OSX. Follow the progress on: [twitter](https://twitter.com/DrawLabApp)   

<img width="742" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/drawlab_teaser_screen.png">




[Video via Vimeo](https://vimeo.com/181233724)   
[Video via Dropbox](https://dl.dropboxusercontent.com/u/2559476/final.mov) 

<img width="444" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/drawlab_rulers.mov.gif">  

### Layer Item Property Prompt:
This prompt lets you set the name of an Layer Item, lock, hide or attach a color tag to the layer. The color tag system will aid in visualy grouping together different layer items.  

<img width="378" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/Screen Shot 2016-06-02 at 13.32.47.png">  

### Create Arc Prompt:    
The "Create Arc Prompt" lets you create an "Arc Path" instance at the point of click. Arc Path instances are first class citizens in DrawLab. They retain their properties even after merging with other path elements like the bezier curve, and also after being sliced and diced with the boolean geometry tools.   

<img width="378" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/Screen Shot 2016-05-31 at 19.54.09.png">  

### Gradient panel:  
The gradient panel lets you pick a gradient (Linear or Radial) based on the colors you pick in the Color panel. Focal point and Ratio can also be set numerically. 

<img width="226" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/drawlab_gradient_panel.png">

### Color panel:   
The color panel lets you select between the colortypes: RGB, HSL, HSB, HSV. And lets you seemlessly switch between these color types. You can also specify a hex color. The color panel will work in conjunction with the gradient panel.  

<img width="226" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/drawlab_color_panel.png">  

### Line panel: 
The line panel lets you select: LineType (Color,Gradient or None), Thickness, ScaleMode, CapStyle, JointStyle, StrokeAlign and Miter-limit:  

<img width="226" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/Screen Shot 2016-05-26 at 13.34.06.png">  

### Fill panel:  
The fill panel lets you select: The fill-type, blend-mode and texture-type. The Fill-types are: Color, Gradient and None. The Blend mode consists of: Normal, Multiply, Overlay, Screen etc. The Texture consits of: Noise, Interference, Turbulence, Pattern and None. 

<img width="226" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/Screen Shot 2016-05-25 at 13.26.44.png">   

### Orientation panel:  
The orientation panel can be used to Arrange, Distribute and Align objects. Align supports Aligning objects either to the Canvas or to other objects. Distribute enables you to lay objects in a row with a specified gap. Arrange enables you to move Objects in-front or behind other objects.   

<img width="226" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/drawlab_orientation_panel.png">    

### FileFormat:
A new OpenSource SVG fileformat that supports layers, groups and other features. While also being backwards compatible with SVG 1.1 (The extra features will be added as hidden meta data to the XML structure of the SVG 1.1 format) here is the current incarnation of this format (it will conform to SVG later down the line): 


```xml
<?xml version="1.0"?>
<document x="264" y="42" width="800" height="600">
  <canvas width="800" height="600">
    <selectpath name="rect">
      <commands>2 2 2 2</commands>
      <pathdata>100 100 200 100 200 200 100 200</pathdata>
      <linestyle color="#000000" alpha="1" thickness="1" capStyle="none" jointStyle="miter" miterLimit="1.414"/>
    </selectpath>
    <layer name="layer" isLocked="false"/>
    <selectpath name="b">
      <commands>1 2 2 2 2</commands>
      <pathdata>497.5 544 503 477.5 607.5 477 627.5 541 719.5 540</pathdata>
      <linestyle color="#000000" alpha="1" thickness="1" capStyle="none" jointStyle="miter" miterLimit="1.414"/>
      <fillstyle color="#00FF00" alpha="1"/>
    </selectpath>
  </canvas>
</document>
```

### Why use SVG? 
1. SVG is viewable in OSX
2. SVG is OpenSource
3. SVG is Version Control friendly (GIT)
4. SVG has Human readable syntax
5. SVG Works in Sketch and Illustrator
6. SVG can be viewed in any internet browser

### Optimizing
The current idea is to utilize SQLite to store SVG data in the app. SQLite handles large amount of data faster than reading and writing to a .svg file. When you save the drawing to disk. The SQlite will export only the new values to the SVG file. 

[Download the press kit](https://dl.dropboxusercontent.com/u/2559476/drawlab_press_kit.zip) 
