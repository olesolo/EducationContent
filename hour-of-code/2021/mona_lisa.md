### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# The Mona Lisa

## Step 1
The Mona Lisa lost her famous smile. You will need to place the `White Glazed Terracotta` blocks we've given the Agent to form a square outline which is 6 blocks in length by 6 blocks in width.

#### ~ tutorialhint 
Use the ``||agent.agent move||`` to move your Agent and then ``||agent.agent place||`` to PLACE the `White Glazed Terracotta` we've given the Agent. Repeat ``||agent.agent move||`` and ``||agent.agent place||`` until the right number of blocks are placed.

```ghost
    agent.move(FORWARD, 0)
    agent.place(FORWARD)
    agent.turn(RIGHT_TURN)
    for (let index = 0; index < 4; index++) {
    	
    }
```
```template
\\
```
```package
```
