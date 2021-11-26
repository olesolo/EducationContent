### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# First Computer Scientist

## Step 1
Someone filled in the computer scientist's punch cards that contain the instructions for the first algorithm. Code your Agent to DESTROY the BROWN blocks to make the cards work.
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
\\
```
```package
```
