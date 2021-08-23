To get started navigate to a chart's .json file. (ex: assets/data/**songName**/)

Now after that create a file called **modchart.lua** and then copy and paste this template in.

```lua
-- this gets called starts when the level loads.
function start(song) -- arguments, the song name

end

-- this gets called every frame
function update(elapsed) -- arguments, how long it took to complete a frame

end

-- this gets called every beat
function beatHit(beat) -- arguments, the current beat of the song

end

-- this gets called every step
function stepHit(step) -- arguments, the current step of the song (4 steps are in a beat)

end
```

Now that we've gotten done with our template file, we can start talking about how our modcharts work. 

Our modcharts work based on lua which is what you're going to be programming in, and an editor we recommend is [Visual Studio Code](https://code.visualstudio.com/)

## Full Examples

Here are some examples that you can base your code on.

```lua
function start(song)
    spinLength = 0
end


function update(elapsed)

    if difficulty == 2 and curStep > 400 then
        if spinLength < 32 then
            spinLength = spinLength + 0.2
        end


        local currentBeat = (songPos / 1000)*(bpm/60)
	for i=0,7,1 do
            local receptor = _G['receptor_'..i]
            receptor.angle = (spinLength / 7) * -math.sin((currentBeat + i*0.25) * math.pi)
	    receptor.x = receptor.defaultX + spinLength * math.sin((currentBeat + i*0.25) * math.pi)
	    receptor.y = receptor.defaultY + spinLength * math.cos((currentBeat + i*0.25) * math.pi)
        end
    end
end

function playerTwoTurn()
    camGame:tweenZoom(1.3,(crochet * 4) / 1000)
end

function playerOneTurn()
    camGame:tweenZoom(1,(crochet * 4) / 1000)
end
```


Getting every note on screen:

```lua
for i = 0, getNumberOfNotes() do
    local note = _G['note_' ..i]
    -- mess with property's
    -- note.x = 1, note.y = 30, etc.
end

```

Getting receptors:

```lua
for i=0,7,1 do
   local receptor = _G['receptor_'..i]
   -- mess with property's
   -- receptor.x = 1, receptor.y = 30, etc.
end
```

Changing characters:

```lua
-- you can just type dad, gf, boyfriend in the code and modify them from anywhere!
dad:changeCharacter("mom",30,30) -- changes to mom at x30 and y30
```

Window Position:

```lua
window.x = 10
window.y = 25

-- set to the games res
window.height = 720
window.width = 1280
```

Creating sprites:

```lua
makeSprite("pogImage","sprite",true) -- path (without the .png, relative to the chart path), what the variable will be called, and if you want to draw it behind the characters

-- and now you can modify it 👯 
sprite.x = 90
sprite.y = 90
```

Something to note, almost every property has a "tweenPos", "tweenAngle", and "tweenAlpha" functions. Exceptions to the window class.

If you want to look at what a class has, go check out it's page!