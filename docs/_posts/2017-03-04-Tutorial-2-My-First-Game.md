---
layout: default
title:  "Tutorial 2 - My First game"
date:   2017-03-02 16:16:01 -0000
categories: jekyll update
---

# Tutorial 2 - My First game

## Preview the game

<https://www.roblox.com/games/673647904/Island-Bomb>

#### Open project shell

#### Add script

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
