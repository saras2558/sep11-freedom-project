# Entry 6
##### 6/1/2022

## Context 

In my last blog, I talked about my MVP and what I needed to do next. Days have gone by and I finished my touches, presenting it in the Expo and in class. 

In this blog, I will reflect on both presentations, takeaways, and how everything went. I will also talk about what I need to improve for next time and the finishing touches I made.

### Last touches 
Although I did change how much of what my project looked like. I did change the distance between the hearts. 

I wanted to make it look more neat and better. So I changed it a lot…like a lot. I first used ‘math.random’ to make the hearts display at random places with random sizes. 

However, that looked a bit messy and some of the hearts were colliding on top of each other. So I changed the numbers and made it more neat. 

```JS

for (var i=-window.innerWidth/2; i<window.innerWidth/2; i+=100){ // for the wdith 
			    for (var l=0; l<window.innerHeight; l+=120 ){ // up and down
			      addShape( heartShape,  settings, 'red',   i, l, 0, 0.8, 1.9, Math.PI, 0.4 );
			    }
			  }
        
 ```
 
This code simply shows how the heart is being displayed. It’s almost like the setting but different by the numbers. 

This was the most change I made. I did not change the speed or how the heart looked. 

### Takeaways from giving Expo elevator pitch (presenting)

I was sitting at the second table and waiting for my turn. To present my presentation. I did memorize my elevator pitch before but I knew that my mind would go blank as soon as the Judges came to me. 

When it was my turn, I first said hi and began my elevator pitch. First, introducing myself and the tool I used, three.js. 



[Previous](entry05.md) | [Next](entry07.md)

[Home](../README.md)
