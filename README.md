<img width="200" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/drawlab_icon_1.svg">

## The pitch:  
When you draw a curve on paper its never perfect. But its easy to get things down. When you draw in an illustration app it's easy to draw things, but hard to make things look good. It takes a skilled designer to make things look good. But what if the illustration app helped users to draw things that great designers has used for ages. Symmetry, elliptical shapes, curves that seem to effortlessly meet to make perfect swanlike curves. What makes some illustrations look so good and others not? Bellow are some examples of what DrawLab will solve with simple interactions:

### Sneak-peak video:
Designing iOS icons with DrawLab:  
[<img width="742" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/drawlab_teaser_screen.png">](https://vimeo.com/181233724)

### Chamfering:  
<img width="433" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/star-chamfer-demo-20fps_2.gif">

### C-bridging:  
<img width="440" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/c-bridge-demo.gif">  

### S-bridging:  
<img width="434" alt="img" src="https://dl.dropboxusercontent.com/u/2559476/s-bridge-demo-short-15-fps.gif">

### FileFormat:
A new OpenSource SVG fileformat that supports layers, groups and other features. While also being backwards compatible with SVG 1.1 (The extra features will be added as hidden meta data to the XML structure of the SVG 1.1 format) here is the current incarnation of this format (it will conform to SVG later down the line): 

```xml
<?xml version="1.0"?>
<document x="264" y="42" width="800" height="600">
  <canvas width="800" height="600">
    <selectpath name="rect">
      <commands>1 2 2 2 2</commands>
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

### Early GUI design:  
[here](https://github.com/eonist/DrawLab/wiki/Early-GUI-design) 

[Download the press kit](https://dl.dropboxusercontent.com/u/2559476/drawlab_press_kit.zip) 
