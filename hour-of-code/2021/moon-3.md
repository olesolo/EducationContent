### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# Mission Moon (Solution)

## Step 1
The below code is the correct solution to the activity. Run the code by pressing the green play button to see it in action.

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
agent.turn(RIGHT_TURN)
agent.move(DOWN, 3)
```
```package
```
