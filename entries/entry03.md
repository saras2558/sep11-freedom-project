# Entry 3
##### 2/12/2022

### Contact 

During these past few weeks, I have been learning more about three.js. I am realizing now that it is not an easy thing to learn. So I decided to start fresh, since I couldn’t understand what I was learning. 

First, I began with the basics of three.js. And turns out there are so many codes that I needed to learn before jumping to the hard ones. This [page](https://threejs.org/manual/#en/fundamentals) helped me a lot. It explained the height, the point of view and how to shape or resize the shape. The code `PerspectiveCamera` which is a projection mode is designed to mimic the way the human eye sees.
A code example: 
```Javascript 
const camera = new THREE.PerspectiveCamera( 45, width / height, 1, 1000 );
scene.add( camera );
```
I didn’t understand this, so I scrolled down and this is how it’s constructed: 
```Javascript 
PerspectiveCamera( fov : Number, aspect : Number, near : Number, far : Number )
```

I still researched more about this. I didn’t understand it as much. I searched online and found this [video](https://www.youtube.com/watch?v=KyTaxN2XUyQ) which explains it better. Plus it’s a more visual explanation. 

During the video they also mentioned a new code `camera.updateProjectionMartix();` 

They said that it has three js to evaluate these parameters and form a new projection matrix. However before, they said that if you need to change the values itself on the camera, such as near views or far planes, I would have to use `camera.updateProjectionMartix();` 

---

Now I wanted to see it in action so I tried to edit some of the code that was already written. The screenshot below shows the code and the result: 



[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
