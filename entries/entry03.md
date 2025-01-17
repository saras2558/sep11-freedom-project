# Entry 3
##### 2/12/2022

## Context 

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

 <img src="blob:chrome-untrusted://media-app/4c4fb698-2ade-4e17-b33b-d437ced2de3d" alt=""/>![image](https://user-images.githubusercontent.com/73479762/154108737-e7849741-ea49-4b9d-87a8-55b1edff56ca.png)


Although it does have new codes, which I would like to search more, knowing what the code did helped me take the first step. 
Below is also another a screenshot, that explains the code or the structure of `camera.updateProjectionMartix();` 

 <img src="blob:chrome-untrusted://media-app/0467fc9f-0beb-4db5-8a4f-0f506f0122dc" alt=""/>![image](https://user-images.githubusercontent.com/73479762/154108428-a4f1bea7-6874-486e-95ce-b6de44bffc1a.png)

These define the camera's viewing frustum. 

---

## Skills: 

I used the skills on how to google, and organization. I googled and searched for solutions that led me to the video. Then I used organization by organizing my files and making my image show on github. I also used my notes to help me not forget the code I am learning. 

## Ep: 

For my Engineering design process, in my last entries I jumped right 4. However, I really think I am around 1 or 2. I need to do a lot of research and learn many codes. Next, I will learn more of the code I saw and finally take it a step at a time. 


[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
