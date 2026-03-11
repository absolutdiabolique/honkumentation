# Basic

```
{
  "name": "My Custom Level",
  "description": "",
  "version": 1.709,
  "scrollSpeed": 2.4,
  "gravity": 0.4,
  "antigravity": false,
  "yTrack": false,
  "gradientTopColor": "#009dff",
  "gradientBottomColor": "#c2ccff",
  "disableBackgroundMusic": false,
  "midiConfig": {
    "restartOnDeath": false,
    "volume": 100
  },
  "birdStartX": 100,
  "birdStartY": 300,
  "pipes": [],
  "bullets": [],
  "bulletTriggers": [],
  "layers": {
    "currentLayer": 1,
    "maxLayers": 3
  },
  "genericObjects": [

  ],
  "finishLineX": 661.302,
  "completionRequirement": {
    "type": "crossFinishLine"
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
  "z": 5                  // Z index, higher is up front
  "l": 1                  // the layer that the object is in. this does not affect gameplay, but it does help with editing
}
```

# Generic Objects

These objects go in ```"genericObjects"``` in the JSON.

## Dynamic Objects

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
