### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# First Computer Scientist (Debug)

## Step 1
There's something wrong with the below code. Press the green play button to run it to see what happens, and then debug it to see what's wrong and what changes are needed to make it work.

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
agent.destroy(UP)
agent.move(FORWARD, 2)
agent.destroy(UP)
agent.move(FORWARD, 2)
agent.destroy(UP)
agent.turn(LEFT_TURN)
agent.move(FORWARD, 2)
agent.turn(LEFT_TURN)
agent.destroy(UP)
agent.move(FORWARD, 2)
agent.destroy(UP)
agent.move(FORWARD, 2)
agent.destroy(UP)
```
```package
```
