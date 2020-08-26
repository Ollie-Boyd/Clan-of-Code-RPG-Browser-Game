# Clan of Code
### Screenshots of finished webapp
<p align="center">
<img src="https://raw.githubusercontent.com/Ollie-Boyd/Clan-of-Code-RPG-Browser-Game/master/screenshots/download.gif" width=50% height=auto%>
 <img src="https://raw.githubusercontent.com/Ollie-Boyd/Clan-of-Code-RPG-Browser-Game/master/screenshots/Clan_of_Code.png" width=80% height=auto%>
</p>

## A note on these docs

I try and write the docs for my personal learning projects in an informal way that discusses my thought processes and personal learning points. Of course I appreciate that this isn't an appropriate style for production documentation! I find it valuble for my own benefit to reflect and document in this manner and maybe it's slightly interesting to see how tasks are approached. If you would like any information on anything      

## Brief

>Create a browser game based on an existing card or dice game. Model and test the game logic and then display it in the browser for a user to interact with.
>
>Write your own MVP with some specific goals to be achieved based on the game you choose to model.
>
>You might use persistence to keep track of the state of the game or track scores/wins. Other extended features will depend on the game you choose.

#### We chose as our MVP to:
* Have a branching choose-your-own-adventure style narrative
* Have a player that engages in combat with monsters from the narrative. These should use Fighting Fantasy dice-roll fight logic
* Have a player who could collect items from the storyline
* Have some way of displaying dice-rolls, combat, and items

#### Stretch goals:
* Have an animated storytelling map that would scroll as the narrative changed location
* Have animated fight sequences
* Have sound effects

## Planning
* A couple of the team were very keen that we do a game (other briefs were available) so they had some initial ideas about features they would like to try. Although an RPG game wasn't my natural first choice, I was encouraged by the enthusiasm of my other team members and was on-board. We made a Trello board and brainstormed ideas. It was important to limit scope as we hadn't worked in a group before and weren't sure how much work we could output. 
* On Trello we split the ideas into MVP, and extensions that could be built ontop of the MVP. 
* We all make a wireframe and merged our respective ideas into something somewhat resembling the final project.
* Once the wireframe was done it was time to plan the database. Ed and I got to work with a prototype of the DB structure but we weren't clear on exactly how the branching nature of the dialogue would be best achieved (with some 'chapters' triggering fight scenes, and items) but after sleeping on it I was able to modify Ed's initial MongoDB object structure and allow for narrative branching options to be contained within the DB. 

## What I learned along the way
### Sharing knowledge
To be a good team member sometimes you just need to help your team mates by paired programming. I was quite confident with Vue and JavaScript as I had been practicing a lot outside the course but not everyone on the team was so comfortable. I had to learn that it was ok to just chill and help someone by pair programming without worrying about the lack of code-output that having a team-member tied to a partner might cause. Sharing knowledge felt good and it meant towards the end we were much better able to work independently. 

### How to create an XYZ tile-server with an image. 
I found a cool Python script that allowed me to use the pixels of the image as Lat/Lon coordinates so mapping software like Leaflet.js can display them, pan to coordinates, zoom etc.

first install python-gdal https://medium.com/@vascofernandes_13322/how-to-install-gdal-on-macos-6a76fb5e24a4

then create an XYZ tile-server from your image https://github.com/commenthol/gdal2tiles-leaflet

finally install the Leaflet.js plugin Raster Coords https://github.com/commenthol/leaflet-rastercoords

## What I would do differently
Overall we were pretty pleased with the project but there are things I would do differently again. 
Firstly, refactor before chasing features!!! Human ego took over and we wanted to present a slick looking app but it was horrible towards the end as so many people were contributing code to the fight.js file. It became very bloated and it was mentally taxing to read through the many long functions. 

## To run

### /client/

```
npm install
```
```
npm run serve
```

### /server/

```
npm install
```
```
npm run seeds
```
```
npm run server:dev
```

### Folder structure

* client/ - the frontend vue web application
* server/ - the backend mongodb part that serves an API
* planning/ - notes of the overall system



