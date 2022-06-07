---
layout: post
title: "Unreal Engine 5 Landscape Project: Island 2108"
subtitle: Building an island in Unreal Engine 5
tags: [commtech]
comments: true
---

See this cool island I made in Unreal Engine 5.

<iframe src="https://drive.google.com/file/d/1IwrCrxqMTDNhN4nUB7-zJSB5Gj-ueGi1/preview" style="width: 100%; height: 100%; aspect-ratio: 16 / 9"></iframe>

## Landscape Design Process

![map]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/map.png){: width="25%" align="right" style="margin:1em"}

At the beginning of the project, I designed a map to use as the concept of the landscape. I thought of making an island . The map is made of two islands. The main island consists of a  beach area, a forest, a settlement, a swamp, a river, a rocky hill with an overhang. The secondary island is simply a hill with a landmark on it. At the end of the project, I changed the settlement to a desert area with an oasis in order to focus the project more towards natural landscape creation. I also decided to not make an overhang because it would require me to remake the map with a smaller size in order to look realistic while keeping the same proportions.

## Islands

![screenshot1]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot1.png){: height="200em"}
![screenshot2]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot2.png){: height="200em"}

First, I created the base shape of the two islands. This is done using the water plugin for creating an ocean and islands. Then, I sculpted the base elevations structure of the two islands to set up a foundation to build the details of the island. In this process I had to start over to adjust the actual size of the island. My original plan is to make the island decently big (>10 km width), but this setup used too much resources and was difficult to set up right. Plus, the large size destroys the vertical proportions of the island. The final product is much smaller (~1 km width), which is more appropriate for the design of the island, though it is still a little to big to flesh out the details of the design. In hindsight, I should have set a scale to the map in my design process.

## Landscape Material

![screenshot3]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot3.png){: height="150em"}
![screenshot4]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot4.png){: height="150em"}

The landscape material is needed to make the landscape look realistic. As I’ve worked with Blender before, I found the material creation process to be similar in Unreal Engine 5. I used textures from Quixel Bridge, a library that includes free samples of photo scanned 3D assets. The final material handles various types of surfaces, including grass, sand, rock, swamp, and dirt.

My main challenge was to make the landscape surface look more varied and less repetitive. To accomplish this, I used noise to add color variation to the material. I also mixed different landscape types manually to further reduce the repeating grid effect. I think the result looks decently good for most of the landscape, though the rock and swamp surfaces could be made more smoother.

The other part of making the material is to make sharp slopes have a rocky texture for grass surfaces. This is done by assigning different textures based on the slope of the landscape. I found this to be a great way to make the landscape more realistic without doing extra work to paint the slopes manually.

After the material is done, I can simply paint the textures on the surfaces of the map.

## Beach

![screenshot5]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot5.png){: height="200em"}
![screenshot6]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot6.png){: height="200em"}

The beach is the first part I worked on. The contour of the beach against the ocean is created automatically with the water plugin. I used the landscape sculpting to add variation to the land bordering the water, and to make the upwards slope towards inland more apparent. To add detail to the beach, I used the foliage tool to add beach rocks onto the beach in scattered patterns. 


## Forest

![screenshot7]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot7.png){: height="200em"}
![screenshot8]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot8.png){: height="200em"}

The forest is designed to be higher in elevation compared to the nearby landscape. I used sculpting to raise the height of the land and flattened it to a specific height. On top of this, I added smaller hills. I decorated this section with trees from the Black Alder library, as well as rocks and small shrubbery. I used the grass surface for the majority of this section, with some exposed rock in details.

## Lake and River

![screenshot9]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot9.png){: height="200em"}
![screenshot10]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot10.png){: height="200em"}

As part of the design, I added a lake and river to the main island. I added a small island on the lake with a single tree growing on it, as well as some rocks impeding the flow of the river. The water plugin tool was very finicky when I tried to make this part of the landscape. Sometimes the edge of the water would look blocky, which I needed to fix by sculpting part of the shoreline manually. And unfortunately, more realistic water interaction with objects based on fluid simulation is not possible yet with this tool. Still, the lake does not look too bad in my opinion. In the future, I would like to attempt making a waterfall using this tool.

## Swamp

![screenshot11]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot11.png){: height="160em"}
![screenshot12]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot12.png){: height="160em"}

This part of the landscape is fairly straightforward to make. I painted the section with a mixture of the swamp, grass, dirt and rock surfaces, in order to reduce the repeating swamp textures. I made the section the flattest part of the map, with very gentle slopes visible.

## Rocky Hill

![screenshot13]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot13.png){: height="200em"}
![screenshot14]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot14.png){: height="200em"}

I planned for a few ways to create the hill, such as using enlarged models of rocks to make up the base of the hill, but this takes too much effort for one section of the map. My final plan is to just use the landscape tool to make the hill, then add various types of rock on top of it. In order to do, I raised the section up considerably. To add more variation to the design, I split up the design of the two parts of the hill.  For the part west of the river, I made the top jagged. And for the east part, I created a plateau and added large rocks to decorate the landscape.

## Desert

![screenshot15]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot15.png){: height="200em"}
![screenshot16]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot16.png){: height="200em"}

This is the section that replaces the settlement in the original design. I first extended the beach inlands, and added large ridge-like slopes. I created the oasis using a lake, and surrounded the area with sparse trees and grass surface. I added cacti around the desert since it is thematic, as well as some rocks spread on the surface. In the end, I thought the area looks a little flat in color, such as how the hills are barely visible at a low angle. If I am to make a desert landscape in the future, I will find more ways to vary the sand surface while keeping the looks of a desert, or look for some way to improve the contrast of the landscape in the distance.

## Island 2

![screenshot17]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot17.png){: height="200em"}
![screenshot18]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot18.png){: height="200em"}

I thought to incorporate a landscape design on the secondary island that would complement the main island. To do this, I added a high-up grassy plateau with two rabbit statues on top, with position that overlooks the entire main island. On the north side of the island, I made the statues in Blender, which I imported into UE5. The humanoid figures are there as a reference for the scale of the landscape. I experimented with adding a rocky hill on this island, but it does not really look right when there is already a plateau here. I decided to leave a slightly rock surface on the north side of the island.

## Lighting and Water Material

![screenshot19]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot19.png){: width="30%" align="right" style="margin:1em"}

Lighting is quite important for the map in order tune to details and shadows for the objects on the island. I experimented with different kinds of outdoor lighting, including noon, dawn, dusk, and nighttime. I ended up using an afternoon lighting scheme, because it yielded decently looking shadows that was not intrusive, and the scene is all well-lit. In addition to the sun, I added a fog effect to the scene to improve the look of the landscape from a farther distance.

![screenshot20]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot20.png){: width="30%" align="right" style="margin:1em"}

The original presets of the water material looks pretty good to me as oceanic waters. I tweaked the parameters when I needed the effect to be more realistic. For example, I modified the material for the oasis lake to reduce the blue tint caused by light absorption.

## "Filming"

![screenshot21]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot21.png){: height="200em"}

The format of the product of the project is a video that showcases the landscape. I found that UE5 has a animation tool specific for this purpose, To use that tool, I need to animate cameras to “shoot” a video of the landscape.

My design is to have a opening shot of looking around the beach on the ground, as if they just arrived on the island. Then, in specific locations around the map, the camera will move in spline paths while looking around the world. Finally, there will be a shot that captures the entire landscape in a panning motion around a point.

I implemented my design in the editor, and the result looks pretty good. I put the scenes together, and exported them into one video which I can split apart and edit in the next step.

## Sequencing Video

![screenshot22]({{ site.baseurl}}/assets/img/2022-06-06-ue5-landscape/screenshot22.png){: height="200em"}

To make the video presentation, I used Davinci Resolve, which I learned how to use in the last ISU. I split the sections in rendered video, and added titles and transitions. I performed color correction to give the video a colder colored stylization. I also added some music by C418 from Minecraft, with attribution at the end of the video. I modified the music slightly, by changing the pitch and speed to create a good feeling of scale. As I already learned to edit down a video from ISU 2, I didn’t have any trouble in making the video itself, and the final product looks great to me.

## Conclusion

Overall, the landscape project is a success. I was able to make a decent looking island in Unreal Engine, involving putting together different kinds of landscapes such as forests, deserts, and hills.

There was a lot of bumps in the process however, with technical issues of the landscape corrupting in some occasions and Unreal Engine crashing, which sometimes destroyed my work in the last 10 minutes or forced me to repair part of the landscape. Because of how I set up the base of the landscape, there are some parts of the landscape I didn’t get to make, such as the rock arch across the river. For what I did get to create, I find to be satisfactory. I enjoyed sculpting the shape of the landscape and painting different surfaces onto it, as well as making the showcase video.

Through the project, I learned a lot about using Unreal Engine 5 to create landscapes, and the process of using Unreal Engine to make a cinematic video. I also learned more about the process of 3D modelling and texturing from using Unreal Engine in combination with Blender. Skills I learned for using UE5 will come in handy If I want to make video games in the future.
