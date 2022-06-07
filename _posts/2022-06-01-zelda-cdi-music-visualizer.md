---
layout: post
title: Zelda CDI Music Visualizer
subtitle: Davinci Resolve Fusion and video editing
tags: [commtech]
comments: true
---

Do you enjoy the music of the Zelda CDI games despite its questionable gameplay? Here's two audio visualizer videos of the games' soundtracks.

<iframe src="https://drive.google.com/file/d/1BYSdyZmUE9JwOS7pcP4wZXijbNS2g-QA/preview" style="width: 100%; height: 100%; aspect-ratio: 16 / 9"></iframe>

<iframe src="https://drive.google.com/file/d/19COPjAbBfyWIgjdHXh85KGr47pVwBNrE/preview" style="width: 100%; height: 100%; aspect-ratio: 16 / 9"></iframe>

## Overview

I created 2 video composites that visualizes the music of two infamous video games: “Link: The Faces of Evil” and “Zelda: Wand of Gamelon”. I chose Davinci Resolve as the video editor tool as it is free to use with most functions intact, and I want to learn a new piece of video editing software. Davinci Resolve is similar to Adobe Premiere pro with its video editing features, and its Fusion tool is similar to Adobe After Effects in what it can achieve. For each project, I used Davinci Resolve’s Fusion tool to generate the audio spectrum, and to sync animation effects to the audio. 

## Behind The Scenes

### Assets Used

![vidasset1]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/vidasset1.png){: }

The assets used are from Link: Faces of Evil and Zelda: Wand of Gamelon. The sprites are found on spriters-resource.com. Some of the background images were originally animated with overlaid frames, so I used Gimp to recreate the complete backgrounds. The music is originally composed by Tony Trippi for the two games, and was remixed in this project to create a stereo effect. I chose this video game specifically because it has been an internet phenomenon for over a decade now, and I also want to spread the hidden gem that is the soundtrack of both video games.

### Music

![screenshot1]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot1.png){: width="35%" align="right" style="margin:1em"}

The original music from the game is in mono format with no higher quality masters found anywhere. Because of that, I wanted to improve the music somewhat. To “remaster” the music, I used the Audacity software. I combined similar tracks and panned them in opposite directions to create a pseudo stereo image effect. Then, I added a subtle reverb effect to the music, and looped the main section so that I can smoothly fade out the music after the desired number of loops.

For some of the tracks, I used an equalizer effect to reduce excessive loudness in some frequencies that was produced by combining similar tracks. However, there is still room for improvement in terms of making the music sound more clear, especially in some cases where the melody is barely audible over the percussion. Overall, I think the remastered tracks are a good improvement over the original, and is suitable to use in my projects.

![screenshot2]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot2.png){: width="25%" align="right" style="margin:1em"}

### Planning and Designing


As part of pre-production, I created storyboards for the two videos, and noted specific requirements and effects used for each section of the project.

### Audio Visualizer

![screenshot3]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot3.png){: width="40%" align="right" style="margin:1em"}

The audio spectrum visualizer is made in Fusion using an audio visualizer plugin, which I’ve done in my audio visualizer tutorial. This tool produces an audio spectrum, as well as wave amplitude data that can be used to animate other objects to the loudness of the audio. The challenge I faced from using this plugin is finding the right frequency range to use as a driver for animating other objects based on the audio. I spent the bulk of the time making the audio visualizer look good.

![screenshot4]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot4.png){: }

While the plugin produces great-looking results, it was very slow for my liking. So, I decided to render the spectrum at a lower resolution compared to what I did in the tutorial. For the final project, I rendered the audio spectrum at 1/5 of 1080p, and upscaled it in nearest neighbor mode to the appropriate size. This essentially created a pixelation effect on the audio spectrum, which is fitting for depicting a video game soundtrack while improving performance somewhat. The spectrum is then merged with a background gradient to add the chosen color palette for each spectrum. Finally, I added a glowing effect to the spectrum. I placed the audio visualizer to the very front of the layer stack so it is always visible and frames the foreground. 

### Particle Systems

![screenshot6]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot6.png){: height="200em"}
![screenshot7]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot7.png){: height="200em"}

I used a particle system that was animated to the beat of the music in my previous tutorial project. However, similar to the audio spectrum, the particle system took an excessively long time to render. To make the project easier to work with, I decided to limit my use of particle systems, and to make them as simple as possible while achieving its effect. 

![screenshot5]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot5.png){: }

![screenshot8]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot8.png){: }


I spent some time planning where to best use particles, and how it should look. For the Tykogi Tower project, the particles are spawned in a spherical area with upwards velocity, and a rotating force was applied to the particles causing them to spin in a cyclone like fashion. I merged the particles with the audio spectrum, which adds the same pixelation effect and gradient to the particles. The result looks very fitting in my opinion. I reused the effect for the intro of the Ganon project, which contains the same vortex effect but in the horizontal direction and with different parameters.

### Background

![vidasset2]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/vidasset2.png){: }

![screenshot9]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot9.png){: width="30%" align="right" style="margin:1em"}

The original textures of the background are often much wider than the 16:9 frame. To solve the issue of the background not fitting entirely on screen, I cropped the image. After seeing that having the background in one place looks pretty boring, I decided to animate the cropped section to oscillate back and forth over time using a sine function. The result is that the background moves around over time in the video, which makes the background look a lot less static.

![screenshot10]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot10.png){: width="30%" align="right" style="margin:1em"}

As part of visualizing audio, I added a camera shake effect and a scaling effect with their intensities tied to the audio. This combines with the moving background to make the scene look decently lively.

![screenshot11]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot11.png){: }

### Foreground

#### Tykogi Tower Project

![screenshot12]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot12.png){: }

I took 3 foreground sprites from a cutscene from the game. They were animated in Fusion, and was driven with the same method as the background for syncing to the audio. As just having the sprites there does not add much to the scene, I made the sprites cycle between their respective frames in the cutscene. The original animation was not in 60 fps, so I slowed down the animation to match the original speed.

![screenshot13]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot13.png){: }

To distinguish the foreground and background, I made the audio-based effects more intense than the background.

#### Ganon Project

![screenshot14]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot14.png){: }

For each scene, I chose 2 frame ranges in the cutscene animation with the same character in a different pose, and switched the 2 animations based on the audio. The result is that the sprite moves according to the beat or bassline of the music.  I used the same driver for the scaling effect on the sprites.

One problem I’ve ran into with animating in this way is the excessively flashing images caused by switching the animation too fast, which although I desired, it was too distracting. To resolve this, I added a frame blending node to tween adjacent frames. This does not solve the entire problem, but it makes the animation slightly smoother to watch.

![screenshot15]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot15.png){: }

In the last scene, I added a glow effect to accentuate the bright colors (lightning bolt) on the subject.

### Color Grading

![screenshot16]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot17.png){: }

As the video composite still look somewhat “normal”, I experimented with color grading tools in Davinci Resolve to give each scene a more distinct look. Similar to what I’ve done in the tutorial, I used compositing to add a specific colored tint to each scene. This was done mostly by adjusting the options surrounding the primary color wheel. As an example, I shifted the color temperature towards warmer colors in scenes that contains lava in the background to make the clip feel warmer, and I boosted the blue color in the last scene of the Ganon project to emphasize the lightning bolts. I kept the color grading effects subtle to ensure it does not look overdone. For basic coloring like what I did for my projects, I did not find color grading to be too difficult.

![screenshot17]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot18.png){: }

### Combining and Editing The Video

![screenshot19]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot19.png){: }

After I finished creating the scenes, I sequenced them with the video editor, which I learned how to use in the tutorials. I added transitions between clips, and subtitles for each scene to show the name of the music being played.

![screenshot18]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/screenshot18.png){: }

To draw all the text in the video, I used the basic text effect I used in my tutorials to show the main title and track titles. For the font, I chose Palatino Linotype, a serif font that is appropriate to the theme of the video game. When necessary, I used drop shadows to ensure best visibility of the text.

For each project, I added an elaborate intro and/or outro. These consists of a short animation that composes part of the cutscenes. Overall, the whole process of editing the video was fairly straightforward compared to making the audio visualizer itself. After the project is finished, I exported the video in 1080p 60fps format.

### Conclusion

![morshu]({{ site.baseurl}}/assets/img/2022-06-01-zelda-cdi-music-visualizer/morshu.gif){: width="35%" align="right" style="margin:1em"}

This project is overall a success despite the relatively short time frame I had to work on the project. The results were much better than my expectations, which looks pretty clean for the effect I was trying to accomplish. I especially enjoyed making the Ganon project. I made each scene give off a somewhat different vibe by altering every effect slightly, some with more camera shake or blur than others. Although audio visualization is not a novel idea, I came up with ways to make the project more distinct, namely using a moving background and animating character movements.

The tutorials I worked with for this project were generally pretty good. I ended up using all the skills I learned in basic video editing and Fusion, creating the audio visualizer and using effects. In addition, I worked with other software including Audacity and Gimp to . If I had more time to work on this project, I would work to improve the transition between the scenes, as well as creating stylistic intros and outros. I feel there is more room to polish up the project, and some scenes can certainly be made cleaner by tweaking the audio visualizer. I could also spend some time to make more design ideas for the audio visualizer. From what I’ve found, Davinci Resolve is definitely not the best way to make audio visualizers because of its poor performance. If I were to make another audio visualizer, I’ll find another software than can handle this better, then put the exported renders in Davinci Resolve.

Overall, I learned a lot about how to use all aspects Davinci Resolve, from sequencing video, adding effects to both video and audio, and using Fusion to its fullest potential. In addition to video editing, I also learned how caching works in Davinci Resolve to drastically speed up working with video. The skills I learned from doing this project will help me make better video composites in the future.
