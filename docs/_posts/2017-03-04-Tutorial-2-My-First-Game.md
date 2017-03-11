---
layout: default
title:  "Tutorial 2 - My First game"
date:   2017-03-04 10:16:01 -0000
categories: tutorials
---

# Tutorial 2 - My First game

## Preview the game
Here is a preview of the finished game.

<https://www.roblox.com/games/673704119/bomb-on-us>

### Open project shell
To begin this project you need to download the project shell. This contains the platform and the spawn point for players in the game.

<a href="{{site.baseurl}}/assets/tut2/IslandBomb-ProjectShell.rbxl">Project Shell</a>

Once you have downloaded the project shell, double click on the file and it will open in Roblox.

When you open the file you should see a platform and a spawn point.

To see you player in the game you need to go to the Test menu at the top and press the play button. ![]({{site.baseurl}}/assets/tut2/play.png?raw=true)

![]({{site.baseurl}}/assets/tut2/clickplay.png?raw=true)

You should see the platform with the player on the spawn point.

![]({{site.baseurl}}/assets/tut2/world.png?raw=true)

The game we are making have balls falling from the sky and exploding and random points. To make this happen we need to add a script to the game - this is like adding a script to the background in Scratch.

To add a script in Roblox go to the explorer menu and click ServerScriptService -> Insert Object -> Script.

![]({{site.baseurl}}/assets/tut2/addscript.png?raw=true)

Now that you have you script we need to add code. Below are the steps you should use to build the game. Following each step and press play after you complete a step to see how the world changes.

### Step 1

#### add your name

```
print("made by essygamer")
```


### Step 2

#### add a part

```
print("made by essygamer")

local ball = Instance.new("Part", workspace)
```

### Step 3

#### make the part into a ball

```
print("made by essygamer")

local ball = Instance.new("Part", workspace)
ball.Shape = Enum.PartType.Ball
```

### Step 4

#### add the ball at a random position on the platform

```
print("made by essygamer")

math.randomseed(os.time())

local ball = Instance.new("Part", workspace)
ball.Shape = Enum.PartType.Ball

ball.Position = Vector3.new( math.random()*100 - 50, 10, math.random()*100 - 50)
```

### Step 5

#### make the ball move a bit when it lands

```
print("made by essygamer")

math.randomseed(os.time())

local ball = Instance.new("Part", workspace)
ball.Shape = Enum.PartType.Ball

ball.Position = Vector3.new( math.random()*100 - 50, 10, math.random()*100 - 50)
ball.Velocity = Vector3.new( math.random()*50-25, 10, math.random()*50 - 25)
```

### Step 6

#### make an explositon at the ball position

```
print("made by essygamer")

math.randomseed(os.time())

local ball = Instance.new("Part", workspace)
ball.Shape = Enum.PartType.Ball


ball.Position = Vector3.new( math.random()*100 - 50, 10, math.random()*100 - 50)
ball.Velocity = Vector3.new( math.random()*50-25, 10, math.random()*50 - 25)

local explosion = Instance.new("Explosion", workspace)
explosion.Position = ball.Position
```

### Step 7

#### remove the ball after the explosion

```
print("made by essygamer")

math.randomseed(os.time())

local ball = Instance.new("Part", workspace)
ball.Shape = Enum.PartType.Ball


ball.Position = Vector3.new( math.random()*100 - 50, 10, math.random()*100 - 50)
ball.Velocity = Vector3.new( math.random()*50-25, 10, math.random()*50 - 25)

local explosion = Instance.new("Explosion", workspace)
explosion.Position = ball.Position
ball:Remove()
```

### Step 8

#### add a loop

```
print("made by essygamer")

math.randomseed(os.time())

while true do
    local ball = Instance.new("Part", workspace)
    ball.Shape = Enum.PartType.Ball
    ball.Position = Vector3.new( math.random()*100 - 50, 10, math.random()*100 - 50)
    ball.Velocity = Vector3.new( math.random()*50-25, 10, math.random()*50 - 25)
    wait(0.5)
    local explosion = Instance.new("Explosion", workspace)
    explosion.Position = ball.Position
    ball:Remove()
    wait(0.5)
end
```

That's the game finished. If you want you can add houses, trees and other objects to make you world more interesting.

Enjoy.
