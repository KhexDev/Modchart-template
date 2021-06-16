Kade Engine modcharts use a very simple actor id system, this is based on these premade ids:
| Sprite Id  |                  Value                   |
| :--------: | :--------------------------------------: |
|    0-7     |         Represents Receptor 0-7          |
| boyfriend  | Represents the Boyfriend Actor (player1) |
|    dad     |    Represents the Dad Actor (player2)    |
| girlfriend |     Represents the Girlfriend Actor      |

Or it can also be any object in [PlayState.hx](https://github.com/KadeDev/Kade-Engine/blob/stable/source/PlayState.hx)

Example:
```lua
setActorX(0,'healthBarBG') -- sets the health bar's background x position
```

