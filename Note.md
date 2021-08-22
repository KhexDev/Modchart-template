## Note properties
|  Name   |                         Description                          |
| :-----: | :----------------------------------------------------------: |
|  x  | The position of the note on the X Plane |
|  y   | The position of the note on the Y Plane|
| angle | The angle of the note |
| alpha | The transparency of a note|
| strumTime | The time the note is supposed to be hit |
| data | The type of note (0, left, 1 down, 2, up, 3, right)|
| mustPress | If the note should be hit by the player |
| isSustain | If the note is a sustain body |
| isParent | If the note is a parent of a sustain body |
| getSpotInline | The spot in line which the sustain body falls in |
| getParent | Get the name of the parent |
| getChildren | Get an array containing every child's name this note is a parent to |

## Functions
|  Name   |                         Arguments                            |
| :-----: | :----------------------------------------------------------: |
|  tweenPos | (self,x,y,time) |
|  tweenAngle| (self,angle,time) |
|  tweenAlpha | (self,alpha,time) |