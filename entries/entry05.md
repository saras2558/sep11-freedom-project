# Entry 5
##### 4/25/2022

## Context 

In my last blog, I talked about learning the texture of the shape and how I wanted---needed--- to start coding. For my MVP (The bare minimum), I created 3D heart shapes that go across the screen, while slowly spinning around. 

Although I don’t like how it looks now, I am still working on making it better till the deadline. 

My code took forever!! There were errors, challenges, and lack of understanding of some of the code. 

### Let’s break the code apart: 

Before I could start coding and shaping my shape. I needed to create an index file with the starter code. I had trouble finding the “script src” for three.js code. I asked Mr. Mueller and he suggested this [website](https://cdnjs.com/libraries/three.js/r128) which was so helpful (because if I put all this [lines of code](https://threejs.org/build/three.js), the IDE would literally crash) 

Then, I needed to create a scene (the first code of three.js). In three.js, I needed a div, an append child (for the container or box), THREE.Scene(), THREE.PerspectiveCamera(), and much more that I was not expecting. 

I used this [page](https://threejs.org/docs/index.html#manual/en/introduction/Creating-a-scene), which was the most helpful in learning what I needed to start coding. It explains what each code meant and it adds a cube (that I showed in my last blog). 

I took the knowledge of the code of what I read on that page and created this: 

``` JS
	var container;
	var camera;
	var scene;
    init(); 

function init(){
	 container = document.createElement( 'div' );
	 document.body.appendChild( container );
	 scene = new THREE.Scene();
	 camera = new THREE.PerspectiveCamera( 50, window.innerWidth / window.innerHeight, 1, 1000 );
	 camera.position.set( 0, 150, 500 );
	 scene.add( camera );
} 

```

I added a function because of all the videos that I watched, they said that using a function is more organized. 

There is perspectiveCamera, camera.position, scene.add() to position the camera and how the scene or the view is going to look like. 

After creating the first step of coding three.js, I could not start with shaping the heart. 

### This was on challenge I had: 

Creating or shaping the heart when I did not understand which code to use was difficult. Although I did learn shapes and geometry, I had a hard time understanding the math and code. 

I watched this [video](https://www.youtube.com/watch?v=3eGeh_aJxMI) which helped a lot!!! 

The video was showing different types of shapes and how each one is shaped by code. They demonstrate the code and show the results. 

One thing I noticed was this line of code:

` JS .bezierCurveTo()  `

I searched it up and found the whole explanation on [three.js website](https://threejs.org/docs/#api/en/extras/core/Path.bezierCurveTo). 

There were so many methods but this one looked the easiest when creating a heart shape. 

```JS
.bezierCurveTo ( cp1X : Float, cp1Y : Float, cp2X : Float, cp2Y : Float, x : Float, y : Float );

 ```

This was how it should be written. Then we write the numbers inside the parentheses. 

"This creates a bezier curve from .currentPoint with (cp1X, cp1Y) and (cp2X, cp2Y) as control points and updates .currentPoint to x and y.” According to three.js explanation. 

There was no easy way to create this shape by writing whatever number comes to mind and hope for a heart. And thankfully for me, I know p5js which is similar to three.js. SO, I knew it had something to do with y and x. I used a graph to try to understand the x and y for each corner of the heart. 

Then, I had to create hearts. 

First I did: 

``` JS
var settings = { amount: 1, bevelEnabled: true, bevelSegments: 20, steps: 2, bevelSize: 10, bevelThickness: 50 };

```

To make the size and the thickness of the heart. Then I created a for loop. 

This for loop was a bit challenging for me but since I knew or was introduced from p5js, it wasn’t as difficult. 

I used many sources from the three.js website and finally did: 

``` JS
	for (var i=-window.innerWidth/2; i<window.innerWidth/2; i+=60){
	    	for (var l=0; l<window.innerHeight; l+=60){
	    	 addShape( heartShape,  settings, '#f71e1e', i, l, 0, 0.8, 0.8, 3.14, 0.4 ); // or Math.PI for 3.14
	    	
			 }
		 }
```
This code is to make a loop of hearts all over the screen. I also learned about another Math.something(). It’s called math.pi(), this is similar to 3.14… or pie in math. 

After all of that, I had to do the light direction or make it reflect in a way. 

``` JS
// the light reflected on the shape
			  var light = new THREE.DirectionalLight(0x9955ff, 2);
			  light.position.x = -500;
			  light.position.y = 500;
			  camera.add( light );

			  var light = new THREE.DirectionalLight(0x9955ff, 10);
			  light.position.x = 500;
			  light.position.y = -500;
			  light.position.z = -150;
			  camera.add( light );

			  scene.background = new THREE.Color( '#c70e1d' ); // for the background color

```

This is just for light position and light reflecting the hearts. 

After that I wanted the hearts to move. 

``` JS
var x = -25;
			  var y = -250;
			  var heartShape = new THREE.Shape();
			  heartShape.moveTo( x + 25, y + 25 );
```

Making the heart move in circular motions. 

``` JS

function addShape( shape, settings , color, x, y, z, rx, ry, rz, s ) {
			  var geometry = new THREE.ExtrudeGeometry( shape, settings );
			  var mesh = new THREE.Mesh( geometry, new THREE.MeshPhongMaterial( { color: color } ) );
			  mesh.position.set( x+25, y-50, z );
			  mesh.rotation.set( rx, ry, rz );
			  mesh.scale.set( s, s, s );
			  shapes.push({shape: mesh, x, y, z});
			  scene.add(mesh);
			}


			// the movement
			function animate() {
			  var theSpeed = 0.0001;
			  shapes.forEach(el => {
			    el.shape.rotation.y += el.y * theSpeed; // the rotation
			  });
			}


			// needed for the scene
			function render() {
			    requestAnimationFrame(render);
			    animate();
			    renderer.render(scene, camera);
			}
```

Above shows the rest of the code. Adding the shape, setting the position, the movement and the speed. Render is to craft the creation or scenes using WebGL. 

I did have a challenge creating and coding this. But so many videos helped and three.js websites did as well. Also, examples of code helped understand what I needed to write. 

---

## skills


I learned how to organize my time and other keyboard shortcuts, such as command + Z to undo, which helped a lot because I would accidentally delete a line of code. And, I used what I learned from p5js to help me code three.js since it’s a bit similar. 

Organizing my time was just as important. I took each day on the spring break, to work on a piece of code that needed to be completed. I gave myself at least 3 hours a day to work on the code. I also learned to give myself time to think and calm down before getting more stressed and giving up. 



## Engineering design process:


I think I am around 6 or 7 in my engineering design process because I have my mvp done but it needs major improvements to my liking. Next time or as of now, I am trying to learn other types of code such as shadows and other effects to make my presentation more beautiful. 

I am thinking of fading the heart on the back and creating one big one in the front but I’m still unsure. I also need to comment my code :) 




[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
