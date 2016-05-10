# Polygonal Map Generator

###### Polygonal map generator for games. Generates island maps with a focus on mountains, rivers, coastlines.

## About

Procedural Content Generation for Polygonal Maps.

The main idea behind the algorithm is taken from [Amit's Polygonal Map Generation for Games](http://www-cs-students.stanford.edu/~amitp/game-programming/polygon-map-generation/).

The main code of this repository is based on [Rellikiox's Map Generator](https://github.com/Rellikiox/MapGenerator).

## Features

### To-do

* Using OpenGL or DirectX to represent 3D terrain (consider biomes, moistures, and elevations).
* Implement math library for Vector3 to structure 3-dimensional points.
* Add parameters to control map generation (e.g. the number of islands, maximum heights of map, and so on).
* Add polygonal map generator for basement (e.g. lava, mineral, cave, ground water, and so on).

### Doing

* Code refactoring - No warning messages at warning level 4. 

### Done

* Place a number of random but uniformly distributed points (using Poisson Disk Sampling).
* Calculate the Voronoi diagram of the points.
* Using Perlin Noise determine which cells are land and which are water.
* Calculate the elevation of each point as its distance to the sea. Normalize all the heights.
* Place river sources in random spots and let them flow downwards.
* Calculate the moisture od each point given its distance to the sea (less moisture) and rivers (more moisture).

## Screenshots

### Biomes

<img src="https://github.com/utilForever/PolyMapGenerator/blob/master/Screenshots/Biome%20-%20Version%201.jpg"/>

### Moistures

<img src="https://github.com/utilForever/PolyMapGenerator/blob/master/Screenshots/Moisture%20-%20Version%201.jpg"/>

### Elevations

<img src="https://github.com/utilForever/PolyMapGenerator/blob/master/Screenshots/Elevation%20-%20Version%201.jpg"/>

## Dependencies

* libnoise
* SFML