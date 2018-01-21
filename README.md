# Term1_write_up

For this coursework my teammates and I created a first-person platform game. The idea we had was that the player would have to ascend a wizard's tower whilst navigating past various traps and problems. Throughout the ascent the player would spawn fiery orbs that he could throw into receivers and upon doing so unlock a route to the top.  We all did various parts of coding as well as modelling, texturing and overall design.

## Spike Trap and Fist

I made a spike trap that moved horezontelly as well as a crushing fist that moved vertically. For the spike trap I started by making a simple low poly spike in Maya which I textured trying to give it a dirty metal look. I then duplicated the spike to create a bunch of spikes and essentially the trap. In the game I had used a place holder block to represent the spikes, so it was an easy case of swapping meshes. 

![spiketrap1](https://user-images.githubusercontent.com/32567724/35195469-cd3d4610-febb-11e7-8508-28ee968509d6.png)

![textures1](https://user-images.githubusercontent.com/32567724/35198031-a2965bb6-fee0-11e7-8f33-ba18f0a15d46.jpg)



The fist was hard to model than the spikes and I had to use more difficult techniques to get the shape I wanted. After trying several methods I realised that the best way was to create a simple shape that I could cut into to create fingers and extrude from to create the thumb. 

![fist2](https://user-images.githubusercontent.com/32567724/35195494-51f418ac-febc-11e7-8db3-7e47277c5029.png)

Once the general shape of a closed fist was defined it was then easy to define it, smooth it and extrude a wrist/arm. Texturing, however, was also difficult. For this I used a numbered checkers texture and split the fist into many distinct parts which I cut and sewed as best I could. I used normal, diffuse and speculative maps to create a dark marble like metal that would suit our game’s aesthetics.

![fist3](https://user-images.githubusercontent.com/32567724/35196113-ab474fce-fec5-11e7-89e8-ca7e3dd68d01.png)

To animate the spike and the fist I fisrt set the actor's location to be where it was placed and then made a vector timeline in which I moved the actor over a period of time. For the fist it was a simple case of swapping the meshes and rotating the actor so it proppelled down rather than to the side. Neither of the traps got 'activated' as such so it was fine for them to start upon playing the game and neither of them needed to be disabled as the solution to getting past the spikes was with a jump pad, more on that later.   

![fist trap](https://user-images.githubusercontent.com/32567724/35196347-b7f215b2-fec8-11e7-9c8e-937d531a4524.PNG)

Here is a link to the models moving in the game:

https://www.youtube.com/watch?v=j99veTCQmfY

# Vase 
We needed to include destructable objects in the game that the player could destroy as form of stress relief and fun, I decided to make a destructbale vase for this purpose. Making the vase was a simple case of extruding and shaping before removing the faces at the top to create a hollow vase. 


![vases](https://user-images.githubusercontent.com/32567724/35195584-9b63d1c0-febd-11e7-835d-9cdf371f9ed8.png)

It was then a case of making a destructable mesh in UE4. 


## Jump pad
In order to get past the spike traps I wanted the player to have to shoot a fireball into a designated receiver which would enable a jump pad to launch him over the spikes. For this it was a case of creating a trigger box which upon entering would launch the player a certain distance. I then had to hook the trigger box up to the interface for the fireball receiver. The interface starts the corresponding blueprint depending on whether the correct receiver had been activated by a fireball. 

![jump pad](https://user-images.githubusercontent.com/32567724/35196653-e68acea6-fecc-11e7-8f36-06d7bbab5e86.PNG)

Here is a linke to the jump pad and spike being used in game

https://www.youtube.com/watch?v=jr5YGAZpx3w

## Moving Platforms
For the moving platforms I originally made a matinee in which I animated the platforms, I found this method to be buggy and unhelpful for what I wanted to achieve. I decided to move them through blueprints and specifically the timeline feature which allows you to animate vectors. 

![moveing plat](https://user-images.githubusercontent.com/32567724/35196654-e6a61922-fecc-11e7-8516-834307a497d7.PNG)


# Particle Spawn

In order to visualise where the player should stand in order to be launched by the jump pad I created a particle spawner that emitted a runic symbol to show the play where to be. I chose a rune like design because it seemed more in keeping with the fantasy/wizard aesthetic that we were going for than if I used an actual jump pad etc.  

I created a drawing of the rune in photoshop.

![rune](https://user-images.githubusercontent.com/32567724/35196813-3ea52cd8-fecf-11e7-83ef-f804c61f79a7.png)

I then imported it into Unreal and used the particle system to give it a glowing effect in order to make it seem more magical and ethereal.

![runegame](https://user-images.githubusercontent.com/32567724/35198420-a4fb1242-fee6-11e7-8ed1-9335847942bd.PNG)

Using blueprints I made it that the rune would be triggered when the player fires his fire orb into the correct receiver. 

![partical spwan](https://user-images.githubusercontent.com/32567724/35196655-e6bfed5c-fecc-11e7-9f14-f31e2a4e3541.PNG)

## Sound 
For the sound of the spikes moving in and out I recorded the sound of scraping metal against metal. This created the desired affect which I added a small amount of reverb to. I then had to change the duration of the audio to match the duration of the spikes’ animation in the game. 

![force_pull_sfx](https://user-images.githubusercontent.com/32567724/35198191-25a97982-fee3-11e7-8627-75be128e963c.PNG)



