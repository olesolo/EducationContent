### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# Mission Moon

## Step 1
Send your agent to the space module to deliver the calculations. Use the Mathematician's calculations to determine how many moves the agent must make. Forward 25, right 17, and down 3.

#### ~ tutorialhint 
Use the ``||agent.agent move||`` and ``||agent.agent turn||`` blocks within the ``||blocks.on start||`` block to deliver the calculations to the space module. Use the Mathematician’s calculations to help you determine the path the Agent should take.

```ghost
    agent.move(FORWARD, 0)
    agent.turn(RIGHT_TURN)
```
```template
\\
```
```package
```
