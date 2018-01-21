# Term1_write_up

For this coursework my teammates and I created a first-person platform game with idea of ascending a wizard's tower. We all did various parts of coding as well as modelling, texturing and design.

## Spike Trap and Fist

I made a spike trap by making a simple low poly spike in Maya, which I textured trying to give it a dirty metal look I then duplicated the spike to create the trap. In the game I had used a place holder block to represent the spikes, so it was an easy case of swapping meshes. 

![spiketrap1](https://user-images.githubusercontent.com/32567724/35195469-cd3d4610-febb-11e7-8508-28ee968509d6.png)

For the fist I had to learn a lot about modelling and texturing as it was quite a tricky thing to make. I realised that the best method was to create a simple shape that I could cut into to create fingers and extrude to create the thumb. One the general shape of a closed fist was defined the rest was easy. 


![fist2](https://user-images.githubusercontent.com/32567724/35195494-51f418ac-febc-11e7-8db3-7e47277c5029.png)

Texturing, however was tricky, for this I used a numbered checkers texture and split the fist into distinct parts which I cut and sewed as best I could. I used normal, diffuse and speculative maps to create a dark marble like metal that would suit our game’s aesthetics.

![fist3](https://user-images.githubusercontent.com/32567724/35196113-ab474fce-fec5-11e7-89e8-ca7e3dd68d01.png)

To animate the spike and the fist I fisrtly set the actor's location then made a vector timeline in blueprints in which I moved the actors 

![fist trap](https://user-images.githubusercontent.com/32567724/35196347-b7f215b2-fec8-11e7-9c8e-937d531a4524.PNG)

# Vase 
simple case of extruding and shaping before removing the faces at the top to create a hollow vase. 


![vases](https://user-images.githubusercontent.com/32567724/35195584-9b63d1c0-febd-11e7-835d-9cdf371f9ed8.png)


## Sound 
For the sound of the spikes moving in and out I recorded the sound of scraping metal against metal. This created the desired affect which I added a small amount of reverb to. I then had to change the duration of the audio to match the duration of the spikes’ animation in the game. 

## Jump pad
This was a case of creating a trigger box which upon entering would launch the player a certain distance. I then had to hook the trigger box up to the interface for the fireball receiver. The interface starts the corresponding blueprint depending on whether the correct receiver had been activated by a fireball. 

![jump pad](https://user-images.githubusercontent.com/32567724/35196653-e68acea6-fecc-11e7-8f36-06d7bbab5e86.PNG)

## Moving Platforms
For the moving platforms I originally made a matinee in which I animated the platforms, I found this method to be buggy and unhelpful for what I wanted to achieve. I decided to move them through blueprints and specifically the timeline feature which allows you to animate vectors. 

![moveing plat](https://user-images.githubusercontent.com/32567724/35196654-e6a61922-fecc-11e7-8516-834307a497d7.PNG)



# Particle Spawn

In otrder to visualise where the player should stand in order to be launched by the jump pad I created a partical spawner that emitted a runic symbol to show the play where to run. 

I created a drawing of the rune in photoshop.

![rune](https://user-images.githubusercontent.com/32567724/35196813-3ea52cd8-fecf-11e7-83ef-f804c61f79a7.png)

I then imported it into Unreal and used the partical system to give it a glowing effect. Using blueprints I made it that the rune would be triggered when the player fires his fireball into the correct reciever. 

![partical spwan](https://user-images.githubusercontent.com/32567724/35196655-e6bfed5c-fecc-11e7-9f14-f31e2a4e3541.PNG)



