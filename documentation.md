# Basic
All the values shown here are the default values for the game (except for the coordinates of objects).
```
{
  "name": "My Custom Level",
  "description": "",
  "version": 1.709,
  "scrollSpeed": 2.4,                   // speed 1 is about 62.65 pixels per second (needs verification)
  "gravity": 0.4,
  "antigravity": false,
  "yTrack": false,                      // if this is true, then the camera will follow the player up and down.
  "gradientTopColor": "#009dff",        // the background is a vertical gradient
  "gradientBottomColor": "#c2ccff",
  "disableBackgroundMusic": false,
  "midiConfig": {
    "restartOnDeath": false,            // since there is no sync, it is recommended to keep it this way
    "volume": 100                       // percent
  },
  "birdStartX": 100,
  "birdStartY": 300,
  "pipes": [],                          // i don't even know why this exists
  "bullets": [],
  "bulletTriggers": [],
  "layers": {
    "currentLayer": 1,                  // this doesn't matter. this only decides which layer the editor will start with selected
    "maxLayers": 3                      // i don't see why you need more than 3. one for layout, one for primary decoration, one for background decoration
  },
  "genericObjects": [

  ],
  "finishLineX": 661.302,               // although strange, this is the default value
  "completionRequirement": {
    "type": "crossFinishLine",          // this is the default, but this can also be set to "speedrun"
    "time": 15000                       // time in milliseconds until finish line. if the finish is not reached within this time, the goose will explode and die
  }
}
```

# Universal Attributes

All objects have some universal attributes.

```
{
  "type": "typeOfObject", // type of the object
  "x": 420,               // X coordinate
  "y": 69,                // Y coordinate
  "a": 0.262,             // rotation
  "s": 1.77,              // scale factor
  "fY": true,             // flipped Y?
  "fX": false,            // flipped X?
  "z": 5,                 // Z index, higher is up front
  "l": 1                  // the layer that the object is in. this does not affect gameplay, but it does help with editing
}
```

# Generic Objects

These objects go in ```"genericObjects"``` in the JSON.

## Dynamic Objects

### thwompPipe
A pipe, formed from a rectange on bottom and a rectangle on top.
#### Dimensions
##### Bottom rectangle:
Height: ```245px```

Width: ```50px```
##### Top rectangle:
Height: ```30px```

Width: ```60px```
##### Bounding box:
Height: ```275px```

Width: ```60px```
#### Attributes
```
{
  "type": "thwompPipe",
  "uS": 54,               // up speed in pixels/second
  "dS": 30,               // down speed in pixels/second
  "mR": 75,               // movement range
  "st": "moving_up",      // can be "moving_up" or "moving down." this is starting direction
  "baseX": 230.281,       // idk what this does
  "baseY": 56.668,        // or this either
  "gMR": 100,             // idk
  "direction": "up",      //  can be "up" or "down." it seems that if this conflicts with "st," then it will wait the delay before moving
  "tD": 1000,             // delay at top in milliseconds
  "bD": 1000              // delay at bottom in milleseconds
}
```

### bounceBlock
#### Dimensions
Width: ```60px```

Height: ```60px```
#### Attributes
```
{
  "type": "typeOfObject", // type of the object
  "bF": 5                 // bounce force, the default is 5
}
```
#### Variants
bounceBlockA, bounceBlockB, bounceBlockD, animatedBounceBlock

### teleporter
#### Dimensions
idk too lazy
#### Attributes
When creating a teleporter, you must have two separate objects.
```
{
    "type": "teleporter",
    "x": 420,
    "y": 69,
    "cooldownDuration": 1,              // cooldown for usage, in seconds
    "teleporterPairId": "pair_IPW7",    // the player will be teleported to the portal with the same id
    "teleporterId": "tp_652JN9",        // doesn't matter, just make sure every id is unique
    "transitionDuration": 200,          // amount of time to transition from one portal to the other, in milliseconds
    "color": "#ffffff",                 // the color of the portal
    "syncColorWithPair": true           // if this is selected, then the other portal in the pair will have the same color as this portal
}
```

## Static Objects

### colorBlock

#### Dimensions
Width: ```50px```

Height: ```50px```
#### Attributes
```
{
  "type": "colorBlock",
  "color": "#ff0000"      // the hex code color of the block
}
```

### colorTile

#### Dimensions
Width: ```20px```

Height: ```50px```
#### Attributes
```
{
  "type": "colorTile",
  "color": "#ff0000"      // the hex code color of the tile
}
```
