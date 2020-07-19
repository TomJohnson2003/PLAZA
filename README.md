# python-2d-game

This is a simple 2D action RPG game that lets you control a character and fight against 
different monsters, using potions and abilities to your advantage.

#### In-game footage (YouTube):

[![in-game footage](https://img.youtube.com/vi/4FijOSF_O6o/0.jpg)](https://www.youtube.com/watch?v=4FijOSF_O6o)

#### Screenshots:

<img src="https://github.com/JonathanMurray/python-2d-game/blob/master/screenshots/gameplay.png" height="300" />
<br/>

_Choose your hero:_

<img src="https://github.com/JonathanMurray/python-2d-game/blob/master/screenshots/heroes.png" height="300" />
<br/>


_Master different abilities:_

<img src="https://github.com/JonathanMurray/python-2d-game/blob/master/screenshots/abilities.png" height="300" />
<br/>

<img src="https://github.com/JonathanMurray/python-2d-game/blob/master/screenshots/abilities_2.png" height="300" />
<br/>

_Equip powerful items:_

<img src="https://github.com/JonathanMurray/python-2d-game/blob/master/screenshots/items.png" height="300" />
<br/>

<img src="https://github.com/JonathanMurray/python-2d-game/blob/master/screenshots/items_2.png" height="300" />
<br/>

_Customize your character with talents:_

<img src="https://github.com/JonathanMurray/python-2d-game/blob/master/screenshots/talents.png" height="300" />
<br/>

<img src="https://github.com/JonathanMurray/python-2d-game/blob/master/screenshots/talents_2.png" height="300" />
<br/>

<img src="https://github.com/JonathanMurray/python-2d-game/blob/master/screenshots/talents_3.png" height="300" />
<br/>


_Interact with NPCs:_

<img src="https://github.com/JonathanMurray/python-2d-game/blob/master/screenshots/dialog.png" height="300" />
<br/>


## Installation

This project uses Python3. 
 
The library [Pygame](https://www.pygame.org) is also used. 

To install pygame:
```
pip install -r requirements.txt
```

## Playing the game

Simply run
```
./run.py
```

## Generating an executable file
To generate an executable that can be run without having Python installed:
```
pyinstaller run.spec
```
(The file `run.spec` has been generated by pyinstaller and then manually modified 
to include a resource directory.) 

The executable has to be run from the terminal, and you have to cd into the
directory before executing it.

## Launching the map editor

Simply run
```
./map_editor.py
```
or to edit a specific map
```
./map_editor.py --map test.json
```

## Gameplay basics

* Use arrow keys to move
* Use keys shown in UI to use abilities and consumables
* Use spacebar to interact with NPCs and other entities in the environment
* Press 'Enter' to pause the game
* Press 'S' to save your progress

### Advanced usage
To play a specific map, run
```
./run.py --map test.json
```

or with a specific hero
```
./run.py --hero MAGE
./run.py --hero ROGUE
./run.py --hero WARRIOR
```

There may be more flags to use for debugging purposes.

## Profiling the game:
To profile the game code, run:
```
./profile_game.sh
```
You will be running the game through `cProfiler`, and when you're done
stats will be printed and saved to a file.

If you're using a mac and the game is running at a very low framerate, 
it may be due to an issue with Pygame and Retina displays. Follow these
instructions to open Python in low-resolution mode: 
https://support.apple.com/en-us/HT202471. (For me it led to a big
performance improvement.)