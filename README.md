<img width="200" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/drawlab_icon_1.svg">
# DrawLab 
Technical vector drawing app for OSX [drawlab.io](http://drawlab.io) 
<img width="452" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/drawlab_custom_shape.mov.gif">

## Notes:

A new OpenSource SVG fileformat that supports layers, groups and other features. While also being backwards compatible with SVG 1.1 (The extra features will be added as hidden meta data to the XML structure of the SVG 1.1 format) here is the current incarnation of this format (it will conform to SVG later down the line): 


```xml
<?xml version="1.0"?>
<document x="264" y="42" width="800" height="600">
  <canvas width="800" height="600">
    <selectpath name="rect">
      <commands>2 2 2 2</commands>
      <pathdata>100 100 200 100 200 200 100 200</pathdata>
      <linestyle color="#000000" alpha="1" pixelHinting="true" lineScaleMode="normal" capStyle="none" jointStyle="miter" miterLimit="1.414"/>
    </selectpath>
    <layer name="layer" isLocked="false"/>
    <selectpath name="b">
      <commands>1 2 2 2 2</commands>
      <pathdata>497.5 544 503 477.5 607.5 477 627.5 541 719.5 540</pathdata>
      <linestyle color="#000000" alpha="1" lineScaleMode="normal" capStyle="none" jointStyle="miter" miterLimit="1.414"/>
    </selectpath>
  </canvas>
</document>
```

## Why use SVG? 
1. SVG is viewable in OSX
2. SVG is OpenSource
3. SVG is Human readable
4. SVG is Version Controls friendly (GIT)

## Optimizing
The current idea is to utilize SQLite to store SVG data in the app. SQLite handles large amount of data faster than reading and writing to a .svg file. When you save the drawing to disk. The SQlite will export only the new values to the SVG file. 
