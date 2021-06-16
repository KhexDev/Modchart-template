You can use each by just doing

```lua
function name(arguments)

end
```

|  Name   |   Arguments    |                         Description                          |
| :-----: | :------------: | :----------------------------------------------------------: |
|  start  |   Song Name    |              Gets called when the song starts               |
| update  | Elapsed frames |       Gets called every frame (after the song starts)       |
| stepHit |  Current Step  | Gets called when ever a step hits (steps are in between beats, aka 4 steps are in a beat) |
| beatHit |  Current Beat  |              Gets called when ever a beat hits              |
| keyPressed | Key Pressed | Gets called when a key just got pressed (up, down, left, right, accept) |