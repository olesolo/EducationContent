### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# First Computer Scientist (Solution)

## Step 1
The below code is the correct solution to the activity. Run the code by pressing the green play button to see it in action.

#### ~ tutorialhint 
Use ``||agent.agent move||`` and ``||agent.agent turn||`` to move your Agent to each BROWN block. Then use ``||agent.agent destroy||`` in the direction you want the block destroyed to remove the BROWN block. Repeat this until all the BROWN blocks are destroyed.

```ghost
    agent.move(FORWARD, 0)
    agent.destroy(FORWARD)
    agent.turn(RIGHT_TURN)
    for (let index = 0; index < 4; index++) {
    	
    }
```
```template
agent.move(FORWARD, 1)
agent.destroy(DOWN)
agent.move(FORWARD, 2)
agent.destroy(DOWN)
agent.move(FORWARD, 2)
agent.destroy(DOWN)
agent.turn(RIGHT_TURN)
agent.move(FORWARD, 2)
agent.turn(RIGHT_TURN)
agent.destroy(DOWN)
agent.move(FORWARD, 2)
agent.destroy(DOWN)
agent.move(FORWARD, 2)
agent.destroy(DOWN)
```
```package
```
