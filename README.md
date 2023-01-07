# _House of the Dragon_ Datasets and Visualizations

1. [About this Project](#about-this-project)
2. [Visualizations](#visualizations)
    1. [Interfaces](#interfaces)
    1. [Narrative Charts](#narrative-charts)
    2. [Screen Time](#screen-time)
    3. [Cumulative Time](#cumulative-time)
    4. [Wordcount & Language](#wordcount--language)
    5. [Co-Occurrence](#co-occurrence)
    6. [Relationships](#relationships)
    7. [Actor Relationships](#actor-relationships)
    8. [Lands of Ice and Fire Geography](#lands-of-ice-and-fire-geography)
    9. [Prediction](#prediction)
    10. [Other People's](#other-peoples)
3. [Data](#data)
4. [Use, Licensing, Attribution](#use-licensing-attribution)

## About this Project

- View all visualizations at [jeffreylancaster.github.io/game-of-thrones](https://jeffreylancaster.github.io/game-of-thrones/)

### Articles on Medium

- ["The Ultimate Game of Thrones Dataset"](https://medium.com/@jeffrey.lancaster/the-ultimate-game-of-thrones-dataset-a100c0cf35fb)
- ["32 Game of Thrones Data Visualizations"](https://medium.com/@jeffrey.lancaster/32-game-of-thrones-data-visualizations-f4ab6bc978d8)
- ["19 More Game of Thrones Data Visualizations"](https://medium.com/@jeffrey.lancaster/19-more-game-of-thrones-data-visualizations-bb2d2c0981f9)
- ["Introducing Game of Thrones Script Search"](https://medium.com/@jeffrey.lancaster/introducing-game-of-thrones-script-search-8ccb2a1df726)

### Data Visualization Episode Recaps

- ["Winterfell"](https://medium.com/@jeffrey.lancaster/game-of-thrones-s8-e1-data-visualization-recap-9656a97c3df3) (Season 8, Episode 1)
- ["A Knight of the Seven Kingdoms"](https://medium.com/@jeffrey.lancaster/game-of-thrones-s8-e2-data-visualization-recap-3d7336ca975e) (Season 8, Episode 2)
- ["The Long Night"](https://medium.com/@jeffrey.lancaster/game-of-thrones-s8-e3-data-visualization-recap-7843e1d24282) (Season 8, Episode 3)
- ["The Last of the Starks"](https://medium.com/@jeffrey.lancaster/game-of-thrones-s8-e4-data-visualization-recap-20ee28cf2af1) (Season 8, Episode 4)

## Interfaces

#### Episode Viewer: `episode/`

- A compilation of episode-specific data visualizations, including aggregate character time on screen, wordcount, languages, locations, and more.<br>[View the visualizations](https://jeffreylancaster.github.io/house-of-the-dragon/episode/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/episode/index.html)

#### Script Search: `search/mongodb/`

- A simple search interface to explore the words spoken on _House of the Dragon_, including who says each line and text and translations in Dothraki, Valyrian, etc.<br>[Search the database](https://game-of-thrones-script.herokuapp.com) || [Explore the code](https://github.com/jeffreylancaster/game-of-thrones/blob/master/search/mongodb/)

## Visualizations

### Narrative Charts

#### Narrative Chart: `map/`

- A visualization of when each character is on-screen throughout the show, where they are, with whom they are, when they die, and more.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/map/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/map/index.html)
  - `process.html`: Builds `keyValues.json` from `episodes.json` by adding y-values and additional location-specific information and outputs the data for `keyValues.json`.
  - `index.html`: Builds the visualization using d3.js and outputs the _House of the Dragon_ narrative chart.

<!---![House of the Dragon Narrative Chart](/map/house-of-the-dragon-map.png)--->

> Note: map contains spoilers.

---

#### Heatmap / Flattened Narrative Chart: `heatmap/`

- A visualization of how many characters are in locations throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/heatmap/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/heatmap/index.html)
  - includes a `calcData` parameter that pre-processes the data for `data/heatmap.json`.

![House of the Dragon Heatmap](/heatmap/house-of-the-dragon-heatmap.png)

> Inspired by [Hubble Image of Galaxy Cluster Converted Into Sound](https://www.youtube.com/watch?v=IHIwDHsrGOc).</a>

---

### Screen Time

#### Characters On Screen: `scenes-character/`

- A visualization of when each character is on screen throughout the entire show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/scenes-character/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/scenes-character/index.html)

![House of the Dragon Characters On Screen](/scenes-character/house-of-the-dragon-scenes-character.png)

---

#### Locations On Screen: `scenes-location/`

- A visualization of when each location is shown on screen throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/scenes-location/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/scenes-location/index.html)

![House of the Dragon Locations On Screen](/scenes-location/house-of-the-dragon-scenes-location.png)

---

#### More-Specific Locations On Screen: `scenes-sublocation/`

- A visualization of when each more-specific location is shown on screen throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/scenes-sublocation/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/scenes-sublocation/index.html)

![House of the Dragon Sublocations On Screen](/scenes-sublocation/house-of-the-dragon-scenes-sublocation.png)

---

#### Special Scenes On Screen: `scenes-special/`

- A visualization of when special scenes (death, sex, flashback, warging, greensight, etc.) are shown on screen throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/scenes-special/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/scenes-special/index.html)

![House of the Dragon Special Scenes On Screen](/scenes-special/house-of-the-dragon-scenes-special.png)

---

#### Deaths On Screen: `bubble-death/`

- A visualization of when deaths happen throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/bubble-death/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/bubble-death/index.html)

![House of the Dragon Deaths On Screen](/bubble-death/house-of-the-dragon-bubble-death.png)

---

#### Weapons On Screen: `scenes-weapons/`

- A visualization of when weapons show up on screen throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/scenes-weapons/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/scenes-weapons/index.html)

![House of the Dragon Weapons On Screen](/scenes-weapons/house-of-the-dragon-scenes-weapons.png)

---

#### Houses On Screen: `scenes-house/`

- A visualization of when various Houses are represented throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/scenes-house/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/scenes-house/index.html)

![House of the Dragon Houses On Screen](/scenes-house/house-of-the-dragon-scenes-house.png)

---

#### Number of Characters Per Scene: `characters-per-scene/`

- A visualization of how many characters are on-screen at one time.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/characters-per-scene/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/characters-per-scene/index.html)

![House of the Dragon Number of Characters Per Scene](/characters-per-scene/house-of-the-dragon-characters-per-scene.png)

---

#### Continuous Screen Time: `bubble-character/`

- A visualization where each bubble represents a character and the size of the bubble is continuous time on screen.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/bubble-character/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/bubble-character/index.html)

![House of the Dragon Continuous Screen Time](/bubble-character/house-of-the-dragon-bubble-character.png)

> Circles are color-coded by House.

---

### Cumulative Time

#### Supercut Duration: `duration-character/`

- A visualization of how long each character has been on-screen throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/duration-character/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/duration-character/index.html)

![House of the Dragon Supercut Duration](/duration-character/house-of-the-dragon-duration-character.png)

> Based on [Andrew Reid's Horizontal Stacked Bar Chart](https://bl.ocks.org/Andrew-Reid/0aedd5f3fb8b099e3e10690bd38bd458).

---

#### Screen Time Per Season: `duration-per-season/`

- A visualization of how long each character has been on-screen in each season of the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/duration-per-season/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/duration-per-season/index.html)

![House of the Dragon Screen Time Per Season](/duration-per-season/house-of-the-dragon-duration-per-season.png)

> Based on [Andrew Reid's Horizontal Stacked Bar Chart](https://bl.ocks.org/Andrew-Reid/0aedd5f3fb8b099e3e10690bd38bd458).

---

#### Character On Screen Time Per Episode: `episode-character/`

- A visualization of how long each character has been on-screen in each episode throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/episode-character/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/episode-character/index.html)

![House of the Dragon Character On Screen Time Per Episode](/episode-character/house-of-the-dragon-episode-character-tyrion-lannister.png)

> Based on [Harry Stevens's Linear Regression for Scatter Plot](https://bl.ocks.org/HarryStevens/be559bed98d662f69e68fc8a7e0ad097).

---

#### Screen Time Per Location: `duration-per-location/`

- A visualization of how long has been spent in each location throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/duration-per-location/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/duration-per-location/index.html)

![House of the Dragon Screen Time Per Location](/duration-per-location/house-of-the-dragon-duration-per-location.png)

> Based on [Andrew Reid's Horizontal Stacked Bar Chart](https://bl.ocks.org/Andrew-Reid/0aedd5f3fb8b099e3e10690bd38bd458).

---

#### Screen Time Per More-Specific Location: `duration-per-sublocation/`

- A visualization of how long has been spent in each more-specific location throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/duration-per-sublocation/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/duration-per-sublocation/index.html)

![House of the Dragon Screen Time Per More-Specific Location](/duration-per-sublocation/house-of-the-dragon-duration-per-sublocation.png)

> Based on [Andrew Reid's Horizontal Stacked Bar Chart](https://bl.ocks.org/Andrew-Reid/0aedd5f3fb8b099e3e10690bd38bd458).

---

#### Character Time Percentage Per Season: `duration-percent/`

- A visualization of how much of a character's time on screen is spent in each season.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/duration-percent/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/duration-percent/index.html)

![House of the Dragon Character Time Percentage Per Season](/duration-percent/house-of-the-dragon-duration-percent.png)

> Based on [Mike Bostock's Normalized Stacked Bar Chart](https://gist.github.com/mbostock/3886394).

---

#### Overall Character Time (Treemap): `duration-treemap/`

- A visualization of how long each character has been on screen throughout the show in proportion to all other characters.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/duration-treemap/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/duration-treemap/index.html)

![House of the Dragon Overall Character Time (Treemap)](/duration-treemap/house-of-the-dragon-duration-treemap.png)

> Based on [takayuki's Treemap in d3 v4](https://bl.ocks.org/ganezasan/52fced34d2182483995f0ca3960fe228).

----

#### Screen Time Per House: `duration-house/`

- A visualization of how long each House has been on screen throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/duration-house/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/duration-house/index.html)

![House of the Dragon Screen Time Per House](/duration-house/house-of-the-dragon-duration-house.png)

> Based on [Andrew Reid's Horizontal Stacked Bar Chart](https://bl.ocks.org/Andrew-Reid/0aedd5f3fb8b099e3e10690bd38bd458).

---

#### Travelling Characters: `region-percent/`

- A visualization of the various locations characters visit and how much of their time they spend there.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/region-percent/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/region-percent/index.html)

![House of the Dragon Travelling Characters](/region-percent/house-of-the-dragon-region-percent.png)

> Based on [Mike Bostock's Normalized Stacked Bar Chart](https://gist.github.com/mbostock/3886394).

---

#### Screen Time in Locations Per Episode: `location-per-episode/`

- A visualization of how long is spent in each location during each episode.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/location-per-episode/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/location-per-episode/index.html)

![House of the Dragon Screen Time in Locations Per Episode](/location-per-episode/house-of-the-dragon-location-per-episode.png)

> Based on [Andrew Reid's Horizontal Stacked Bar Chart](https://bl.ocks.org/Andrew-Reid/0aedd5f3fb8b099e3e10690bd38bd458).

---

#### Screen Time Per Gender By Season: `duration-gender-season/`

- A visualization of how much time women and men are on screen during each season.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/duration-gender-season/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/duration-gender-season/index.html)

![House of the Dragon Screen Time Per Gender By Season](/duration-gender-season/house-of-the-dragon-duration-gender-season.png)

> Based on [wpoely86's Diverging Stacked Bar Chart](http://bl.ocks.org/wpoely86/e285b8e4c7b84710e463).

---

#### Screen Time Per Gender By Episode: `duration-gender-episode/`

- A visualization of how much time women and men are on screen during each episode.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/duration-gender-episode/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/duration-gender-episode/index.html)

![House of the Dragon Screen Time Per Gender By Episode](/duration-gender-episode/house-of-the-dragon-duration-gender-episode.png)

> Based on [wpoely86's Diverging Stacked Bar Chart](http://bl.ocks.org/wpoely86/e285b8e4c7b84710e463).

---

#### Screen Time Per Gender By Episode (Percent): `duration-gender-percent/`

- A visualization of how much time women and men are on screen during each episode as percentages of the episode length.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/duration-gender-percent/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/duration-gender-percent/index.html)

![House of the Dragon Screen Time Per Gender By Episode (Percent)](/duration-gender-percent/house-of-the-dragon-duration-gender-percent.png)

> Based on [wpoely86's Diverging Stacked Bar Chart](http://bl.ocks.org/wpoely86/e285b8e4c7b84710e463).

---

### Wordcount & Language

#### Character Wordcount: `wordcount-character/`

- A visualization of how many words each character says throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/wordcount-character/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/wordcount-character/index.html)

![House of the Dragon Character Wordcount](/wordcount-character/house-of-the-dragon-wordcount-character.png)

> Based on [Andrew Reid's Horizontal Stacked Bar Chart](https://bl.ocks.org/Andrew-Reid/0aedd5f3fb8b099e3e10690bd38bd458).

---

#### Character Wordcount By Season: `wordcount-per-season/`

- A visualization of how many words each character says during each season.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/wordcount-per-season/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/wordcount-per-season/index.html)

![House of the Dragon Character Wordcount By Season](/wordcount-per-season/house-of-the-dragon-wordcount-per-season.png)

> Based on [Andrew Reid's Horizontal Stacked Bar Chart](https://bl.ocks.org/Andrew-Reid/0aedd5f3fb8b099e3e10690bd38bd458).

---

#### Wordcount Per House: `wordcount-house/`

- A visualization of how many words members of each House say throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/wordcount-house/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/wordcount-house/index.html)

![House of the Dragon Wordcount Per House](/wordcount-house/house-of-the-dragon-wordcount-house.png)

> Based on [Andrew Reid's Horizontal Stacked Bar Chart](https://bl.ocks.org/Andrew-Reid/0aedd5f3fb8b099e3e10690bd38bd458).

---

#### Wordcount Per Gender By Season: `wordcount-gender-season/`

- A visualization of how many words women and men say during each season.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/wordcount-gender-season/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/wordcount-gender-season/index.html)

![House of the Dragon Wordcount Per Gender By Season](/wordcount-gender-season/house-of-the-dragon-wordcount-gender-season.png)

> Based on [wpoely86's Diverging Stacked Bar Chart](http://bl.ocks.org/wpoely86/e285b8e4c7b84710e463).

---

#### Wordcount Per Gender By Episode: `wordcount-gender-episode/`

- A visualization of how many words women and men say during each episode.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/wordcount-gender-episode/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/wordcount-gender-episode/index.html)

![House of the Dragon Wordcount Per Gender By Episode](/wordcount-gender-episode/house-of-the-dragon-wordcount-gender-episode.png)

> Based on [wpoely86's Diverging Stacked Bar Chart](http://bl.ocks.org/wpoely86/e285b8e4c7b84710e463).

---

#### Wordcount Per Gender By Episode (Percent): `wordcount-gender-percent/`

- A visualization of how many words women and men say during each episode as a percentage of the total words spoken per episode.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/wordcount-gender-percent/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/wordcount-gender-percent/index.html)

![House of the Dragon Wordcount Per Gender By Episode (Percent)](/wordcount-gender-percent/house-of-the-dragon-wordcount-gender-percent.png)

> Based on [wpoely86's Diverging Stacked Bar Chart](http://bl.ocks.org/wpoely86/e285b8e4c7b84710e463).

---

#### Languages Spoken Per Character: `language-character/`

- A visualization of the languages spoken by characters throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/language-character/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/language-character/index.html)

![House of the Dragon Languages Spoken Per Character](/language-character/house-of-the-dragon-language-character.png)

> Based on [Andrew Reid's Horizontal Stacked Bar Chart](https://bl.ocks.org/Andrew-Reid/0aedd5f3fb8b099e3e10690bd38bd458).

---

#### Languages Spoken Per Episode: `language-episode`

- A visualization of the languages spoken by characters throughout each episode.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/language-episode/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/language-episode/index.html)

![House of the Dragon Languages Spoken Per Episode](/language-episode/house-of-the-dragon-language-episode.png)

> Based on [Andrew Reid's Horizontal Stacked Bar Chart](https://bl.ocks.org/Andrew-Reid/0aedd5f3fb8b099e3e10690bd38bd458).

---

### Co-Occurrence

#### Character Co-Occurrence Matrix: `matrix/`

- A matrix visualization of how often characters are on screen together.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/matrix/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/matrix/index.html)

![House of the Dragon Co-Occurrence Matrix](/matrix/house-of-the-dragon-matrix.png)

> Based on [Mike Bostock's Les Misérables Co-occurrence](https://bost.ocks.org/mike/miserables/).

---

#### Force-Directed On-Screen Co-Occurrence: `force-directed/`

- A force-directed visualization of characters on-screen together throughout the show.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/force-directed/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/force-directed/index.html)

![House of the Dragon Force-Directed On-Screen Co-Occurrence](/force-directed/house-of-the-dragon-force-directed.png)

> Based on [heybignick's d3 v4 force-directed graph](https://bl.ocks.org/heybignick/3faf257bbbbc7743bb72310d03b86ee8).

---
   
#### Chord Diagram of On-Screen Co-Occurrence: `matrix-chord/`

- A chord diagram visualization where chord width represents time spent on-screen together by the conected characters.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/matrix-chord/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/matrix-chord/index.html)

![House of the Dragon Chord Diagram of On-Screen Co-Occurrence](/matrix-chord/house-of-the-dragon-matrix-chord.png)

> Based on [HenryLau's chord diagram on JSFiddle](https://jsfiddle.net/kLe38tff/).

---

### Relationships

#### Force-Directed Relationships: `relations-force/`

- A force-directed visualization of various relationships between characters (e.g. parents, spouses, who killed whom).<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/relations-force/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/relations-force/index.html)

![House of the Dragon Force-Directed Relationships](/relations-force/house-of-the-dragon-relations-force.png)

> Parent-child (solid gray), spouse (dashed blue), and killed by (solid black arrow) relationships shown. Based on [Mike Bostock's Labeled Force Layout](https://bl.ocks.org/mbostock/950642).

---

#### Circle-based Relationships: `relations-circle/`

- A circle-based visualization of various relationships between characters (e.g. parents, spouses, who killed whom).<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/relations-circle/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/relations-circle/index.html)

![House of the Dragon Circle-based Relationships](/relations-circle/house-of-the-dragon-relations-circle.png)

> Parent-child (solid gray), spouse (dashed blue), and killed by (solid black arrow) relationships shown. Based on an [HBO infographic](http://i.imgur.com/PG0963W.png).

---

#### Force-Directed Sexual Relationships: `relations-force-sex/`

- A force-directed visualization of sexual relationships between characters.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/relations-force-sex/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/relations-force-sex/index.html)

![House of the Dragon Force-Directed Sexual Relationships](/relations-force-sex/house-of-the-dragon-relations-force-sex.png)

> Based on a [Cool Material infographic](https://coolmaterial.com/feature/heres-all-the-sex-from-game-of-thrones-in-an-infographic/).

---

### Actor Relationships

#### Costars List: `costars-list/`

- A list of other films in which _House of the Dragon_ costars, well, costar.<br>[View the list](https://jeffreylancaster.github.io/house-of-the-dragon/costars-list/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/costars-list/index.html)

![House of the Dragon Costars List](/costars-list/house-of-the-dragon-costars-list.png)

> Data last pulled following Season 7.

---
   
#### Costars Matrix: `costars-matrix/`

- A matrix visualization of frequency of other films in which _House of the Dragon_ costars, well, costar.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/costars-matrix/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/costars-matrix/index.html)

![House of the Dragon Costars Matrix](/costars-matrix/house-of-the-dragon-costars-matrix.png)

> Data last pulled following Season 7. Based on [Mike Bostock's Les Misérables Co-occurrence](https://bost.ocks.org/mike/miserables/).

---

### Lands of Ice and Fire Geography

#### Force-Directed Network of Opening Sequence Locations: `opening-locations-force/`

- A force-directed network visualization of the _House of the Dragon_ opening sequence locations.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/opening-locations-force/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/opening-locations-force/index.html)

![House of the Dragon Force-Directed Network of Opening Sequence Locations](/opening-locations-force/house-of-the-dragon-opening-locations-force.png)

> Based on [heybignick's d3 v4 force-directed graph](https://bl.ocks.org/heybignick/3faf257bbbbc7743bb72310d03b86ee8).

---

#### Geographic Network of Opening Sequence Locations: `opening-locations-fixed/`

- A geographic network visualization of the _House of the Dragon_ opening sequence locations.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/opening-locations-fixed/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/opening-locations-fixed/index.html)

![House of the Dragon Geographic Network of Opening Sequence Locations](/opening-locations-fixed/house-of-the-dragon-opening-locations-fixed.png)

> Based on the [A Song of Ice and Fire Wiki](https://vignette.wikia.nocookie.net/iceandfire/images/3/37/Ice_and_Fire_World_Map.png/revision/latest?cb=20130127004523) geography.

---

#### Locations on a Globe: `geography-locations/`

- Various _House of the Dragon_ locations displayed on a globe.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/geography-locations/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/geography-locations/index.html)

![House of the Dragon Locations on a Globe](/geography-locations/house-of-the-dragon-geography-locations.png)

> Adapted from [Jason Davies' "Rotate the World"](https://www.jasondavies.com/maps/rotate/).

---

#### Opening Sequence Locations: `opening-seq-arcs/`

- A geographic visualization of the _House of the Dragon_ opening sequence locations on a globe.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/opening-seq-arcs/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/opening-seq-arcs/index.html)

![House of the Dragon Opening Sequence Locations](/opening-seq-arcs/house-of-the-dragon-opening-seq-arcs.png)

> Adapted from [Andrew Mollica's "World Tour along Flying Arcs"](https://bl.ocks.org/armollica/88ef1c807c4bb4cff6f7e033e25172ee).

---

#### Opening Sequence Locations (with Underlying Matrix): `opening-seq-matrix/`

- A geographic visualization of the _House of the Dragon_ opening sequence locations on a globe with an underlying matrix showing the frequency of opening sequence paths between locations.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/opening-seq-matrix/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/opening-seq-matrix/index.html)

![House of the Dragon Opening Sequence Locations (with Underlying Matrix)](/opening-seq-matrix/house-of-the-dragon-opening-seq-matrix.png)

> Adapted from [Andrew Mollica's "World Tour along Flying Arcs"](https://bl.ocks.org/armollica/88ef1c807c4bb4cff6f7e033e25172ee).

---

#### Character Travel Paths: `character-arcs/`

- A geographic visualization of the paths characters have travelled in the Lands of Ice and Fire.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/character-arcs/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/character-arcs/index.html)

![House of the Dragon Character Travel Paths](/character-arcs/house-of-the-dragon-character-arcs.png)

> Adapted from [Andrew Mollica's "World Tour along Flying Arcs"](https://bl.ocks.org/armollica/88ef1c807c4bb4cff6f7e033e25172ee).

---

### Prediction

#### Simple Cluster Analysis (for Prediction?): `episode-character-scatter/`

- A simple cluster analysis plotting the slope and y-intercept of the linear regression of time spent on-screen in each episode. We'll see whether it's predictive at all.<br>[View the visualization](https://jeffreylancaster.github.io/house-of-the-dragon/episode-character-scatter/) || [Explore the code](https://github.com/jeffreylancaster/house-of-the-dragon/blob/master/episode-character-scatter/index.html)

![House of the Dragon Simple Cluster Analysis (for Prediction?)](/episode-character-scatter/house-of-the-dragon-episode-character-scatter.png)

> Adapted from [Harry Stevens's Linear Regression for Scatter Plot](https://bl.ocks.org/HarryStevens/be559bed98d662f69e68fc8a7e0ad097).

---

### Other People's

- [Timelapse animation](https://www.youtube.com/watch?v=6dUjMo5LOgc) from [Type A Media](https://typeamedia.net/)
- [Viz of Thrones](http://www.vizofthrones.com/): a single interface by [Adam Groner](https://github.com/ahgroner), including a geographic map with characters in locations, sex count, death count, scenes in which characters show up, and more
- [GraphXR demo](https://www.youtube.com/watch?v=ZXxBDPPWwYc) from [Kineviz](https://www.kineviz.com/)
- [Character travels through various regions](https://news.northeastern.edu/2019/04/10/the-many-travels-of-jon-snow-tyrion-lannister-and-the-rest-of-hbos-game-of-thrones-characters/) by Lia Petronio
- [Character Social Network](https://news.northeastern.edu/2019/04/11/the-game-of-thrones-social-network/) by Lia Petronio


## Data

#### `data/episodes.json`
```javascript
{
  "episodes": [
    {
      "seasonNum": integer,
      "episodeNum": integer,
      "episodeTitle": "string", // from imdb
      "episodeLink": "string", // endpoint: www.imdb.com
      "episodeAirDate": "string", // from imdb
      "episodeDescription": "string", // from imdb
      "scenes":[
        {
          "sceneStart": "string",
          "sceneEnd": "string",
          "timeline": integer // years in AC
          "location": "string",
          "subLocation": "string",
          "altLocation": "string",
          "flashback": Boolean,
          "greensight": Boolean,
          "warg": Boolean,
          "characters": [
            {
              "name": "string",
              "title": "Hand | Khal | Khaleesi | King | Queen", // only for wearer of the crown
              "age": "infant | child | adolescent | adult", 
              "alive": Boolean,
              "born": Boolean,
              "weapon": [
                {
                  "action": "string",
                  "name": "string"
                }
              ],
              "sex": {
                "with": [
                  "string"
                ],
                "when": "string",
                "type": "string"
              },
              "married": {
                "to": "string",
                "when": "string",
                "type": "string",
                "consummated": Boolean
              },
              "mannerOfDeath": "string",
              "killedBy": [
                "string"
              ]
            },
            ...
          ]
        },
        ...
      ]
    },
    ...
  ]
}
```

#### `data/characters.json`
```javascript
{
  "characters":[
    {
      "characterName": "string",
      "characterLink": "string", // endpoint: www.imdb.com
      "characterImageThumb": "string",
      "characterImageFull": "string",
      "actorName": "string", // OR actors: []
      "actorLink": "string", // endpoint: www.imdb.com
      "actors": [ // for recast characters
        "age": { // "infant", "child", "adolescent", or "adult" (default)
          "actorName": "string",
          "actorLink": "string", // endpoint: www.imdb.com
          "characterLink": "string", // endpoint: www.imdb.com
          "characterImageThumb": "string",
          "characterImageFull": "string",
          "episodesActive":[
            {
              "s": integer,
              "ep": [ integer, ... ]
            },
            ...
          ]
        },
        ...
     ],
      "houseName": [
        "string"
        ...
      ],
      "side": "string", // "Greens" or "Blacks"
      "nickname": "string",
      "royal": Boolean,
      "kingsguard": Boolean,
      "parents": [
        "string",
        ...
      ],
      "parentOf": [
        "string",
        ...
      ],
      "guardianOf": [
        "string",
        ...
      ],
      "guardedBy": [
        "string",
        ...
      ],
      "siblings": [
        "string",
        ...
      ],
      "marriedEngaged": [
        "string",
        ...
      ],
      "allies":[
        "string",
        ...
      ],
      "abducted":[
        "string",
        ...
      ],
      "killed": [
        "string", 
        ...
      ],
      "killedBy": [
        "string",
        ...
      ],
      "serves": [
        "string",
        ...
      ]
      "servedBy": [
        "string",
        ...
      ],
      "rides": [
        "string",
        ...
      ]
      "riddenBy": [
        "string",
        ...
      ]
    },
    ...
  ]
}

```

#### `data/characters-groups.json`
```javascript
{
  "group": [
    {
      "name": "string",
      "characters": [
        "string",
        ...
      ]
    },
    ...
  ]
}

```

#### `data/characters-include.json`
```javascript
{
  "include":[
    {
      "name": "string",
      "include": Boolean
    },
    ...
  ]
}

```

#### `data/locations.json`
```javascript
{
  "regions":[
    {
      "location": "string",
      "subLocation": [
        "string",
        ...
      ]
    },
    ...
  ]
}

```

#### `data/characters-gender-all.json`
```javascript
{
  "male": [
    "string",
    ...
  ],
  "female": [
    "string",
    ...
  ]
}
```

#### `data/characters-gender.json`
```javascript
{
  "gender": [
    {
      "gender":"male",
      "characters": [
        "string",
        ...
      ]
    },
    {
      "gender":"female",
      "characters": [
        "string",
        ...
      ]
    }
  ]
}
```

#### `data/colors.json`
```javascript
{
  "colors": [
    {
      "name": "string",
      "hexadecimal": "string",
      "webSafe": "string",
      "basic": "string",
      "rgb": "string",
      "class": [
        "string"
      ],
      "css": {
        "stroke-width": "string",
        "stroke-dasharray": "string",
        "stroke-linecap": "string"
      }
    },
    ...
  ]
}
```

#### `data/costars.json`
```javascript
{
  "IMDB_ID": {
    "imdb_id": "string",
    "title": "string",
    "year": "string",
    "actors": [
      {
        "personID": "string",
        "actorName": "string",
        "characterName": "string"
      },
      ...
    ]
  },
  ...
}
```

#### `data/heatmap.json`

A pre-processed file for the `heatmap/` visualization:

```javascript
[
  {
    "name": "string",
    "count": [
      {
        "x1": integer,
        "x2": integer,
        "z": integer
      },
      ...
    ]
  },
  ...
]
```

#### `data/keyValues.json`

A pre-processed file for the `map/` visualization:

```javascript
{
  "characters": {
    "CharacterName": {
      "key": "string",
      "values": [
        {
          "s": integer,
          "e": integer,
          "y": integer
        },
        ...
      ]
    },
    ...
  },
  "episodes": [
    {
      "seasonNum": integer,
      "length": integer,
      "shift": integer,
      "episodes":[
        {
          "episodeNum": integer,
          "length": integer,
          "episodeTitle": "string",
          "shift": integer
        },
        ...
      ]
    },
    ...
  ],
  "locations": [
    {
      "name": "string",
      "max": integer,
      "middle": integer
    },
    ...
  ],
  "sublocations": [
    {
      "name": "string",
      "max": integer,
      "middle": integer
    },
    ...
  ]
}
```

#### `data/lands-of-ice-and-fire.json`

A GeoJSON file for geographic visualizations.

```javascript
// It's better to just go look at the file if you're curious.
```

#### `data/opening-locations.json`

A data file for the `opening-locations-fixed/` visualization:

```javascript
{
  "note": "string",
  "locations": [
    {
      "name": "string",
      "fx": float,
      "fy": float
    },
    ...
  ]
}
```

#### `data/wordcount-gender.json`

```javascript
{
  "male": [
    "string",
    ...
  ],
  "female": [
    "string",
    ...
  ],
  "crowd": [
    "string",
    ...
  ]
}
```

#### `data/wordcount-synonyms.json`

A working file to rename characters in the script.

```javascript
{
  "synonyms": [
    {
      "accepted": "string",
      "alt": [
        "string",
        ...
      ]
    },
    ...
  ],
  "groups": [
    "string",
    ...
  ], 
  "others": [
    "string",
    ...
  ]
}
```

#### `data/wordcount.json`

```javascript
{
  "count": [
    {
      "episodeAlt": "string",
      "seasonNum": integer,
      "episodeNum": integer,
      "episodeTitle": "string",
      "text": [
        {
          "name": "string",
          "count": integer,
          "lang": "string", // optional
          "type": "string" // optional
        },
        ...
      ]
    },
    ...
  ]
} 
```

#### `data/script-bag-of-words.json`

```javascript
{
  "count": [
    {
      "episodeAlt": "string",
      "seasonNum": integer,
      "episodeNum": integer,
      "episodeTitle": "string",
      "text": [
        {
          "name": "string",
          "text": "string",
          "lang": "string", // optional
          "translation": "string", //optional
          "type": "string" // optional
        },
        ...
      ]
    },
    ...
  ]
} 
```

## Use, Licensing, Attribution

Feel free to take an use this data however you'd like. It's provided as is, is a creative work, and is probably not perfectly accurate.

I only ask that you cite this repository if you do post/publish/share something you make using the data, and that you let me know (on Github or by email) about what you've made.
