### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# Big Band Jazz (Solution)

## Step 1
The below code is the correct solution to the activity. Run the code by pressing the green play button to see it in action.

#### ~ tutorialhint 
Drag ``||agent.agent move||`` into ``||blocks.on start||`` to give instructions to your agent on how to move. Count how far and in what 
direction the agent needs to move and use the agent move block direction (UP, DOWN, LEFT, RIGHT) and distance to move to the trumpet. At the end of your code use ``||agent.agent collect all||`` to collect the trumpet.
```ghost
    agent.move(FORWARD, 0)
    agent.collectAll()
```
```template
agent.move(FORWARD, 3)
agent.move(UP, 1)
agent.move(FORWARD, 2)
agent.move(DOWN, 2)
agent.move(FORWARD, 2)
agent.move(UP, 2)
agent.move(FORWARD, 1)
agent.collectAll()

```
```package
```
