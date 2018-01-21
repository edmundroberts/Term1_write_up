# Term1_write_up

For this coursework my teammates and I created a first-person platform game with idea of ascending a wizard's tower. We all did various parts of coding as well as modelling, texturing and design.

## Spike Trap and Fist:

I made a spike trap by making a simple low poly spike in Maya, which I textured trying to give it a dirty metal look I then duplicated the spike to create the trap. In the game I had used a place holder block to represent the spikes, so it was an easy case of swapping meshes. 






For the fist I had to learn a lot about modelling and texturing as it was quite a tricky thing to make. I realised that the best method was to create a simple shape that I could cut into to create fingers and extrude to create the thumb. One the general shape of a closed fist was defined the rest was easy. Texturing, however was tricky, for this I used a numbered checkers texture and split the fist into distinct parts which I cut and sewed as best I could. I used normal, diffuse and speculative maps to create a dark marble like metal that would suit our game’s aesthetics.



The Vase: simple case of extruding and shaping before removing the faces at the top to create a hollow vase. 















Coding:
Sound: 
For the sound of the spikes moving in and out I recorded the sound of scraping metal against metal. This created the desired affect which I added a small amount of reverb to. I then had to change the duration of the audio to match the duration of the spikes’ animation in the game. 

Jump pad:
This was a case of creating a trigger box which upon entering would launch the player a certain distance. I then had to hook the trigger box up to the interface for the fireball receiver. The interface starts the corresponding blueprint depending on whether the correct receiver had been activated by a fireball. 
Moving Platforms:
For the moving platforms I originally made a matinee in which I animated the platforms, I found this method to be buggy and unhelpful for what I wanted to achieve. I decided to move them through blueprints and specifically the timeline feature which allows you to animate vectors. 

Spikes/fists:

Programming and modelling

A write up for my personal contribution to the Game we made.
