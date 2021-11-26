### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# Mission Moon (Debug)

## Step 1
There's something wrong with the below code. Press the green play button to run it to see what happens, and then debug it to see what's wrong and what changes are needed to make it work.

#### ~ tutorialhint 
Use the ``||agent.agent move||`` and ``||agent.agent turn||`` blocks within the ``||blocks.on start||`` block to deliver the calculations to the space module. Use the Mathematician's calculations to help you determine the path the Agent should take. Forward 25, right 17, and down 3.

```ghost
    agent.move(FORWARD, 0)
    agent.turn(RIGHT_TURN)
```
```template
agent.move(FORWARD, 25)
agent.turn(RIGHT_TURN)
agent.move(FORWARD, 17)
agent.turn(LEFT_TURN)
agent.move(UP, 3)
```
```package
```
