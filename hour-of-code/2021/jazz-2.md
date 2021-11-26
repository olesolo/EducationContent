### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# Big Band Jazz (Debug)

## Step 1
There's something wrong with the below code. Press the green play button to run it to see what happens, and then debug it to see what's wrong and what changes are needed to make it work.

#### ~ tutorialhint 
Drag ``||agent.agent move||`` into ``||blocks.on start||`` to give instructions to your agent on how to move. Count how far and in what 
direction the agent needs to move and use the agent move block direction (UP, DOWN, LEFT, RIGHT) and distance to move to the trumpet. At the end of your code use ``||agent.agent collect all||`` to collect the trumpet.
```ghost
    agent.move(FORWARD, 0)
    agent.collectAll()
```
```template
agent.move(FORWARD, 2)
agent.move(UP, 1)
agent.move(FORWARD, 2)
agent.move(DOWN, 3)
agent.move(FORWARD, 2)
agent.move(UP, 2)
agent.move(FORWARD, 1)
agent.collectAll()
```
```package
```
