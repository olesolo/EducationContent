### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# Paleontology Puzzle

## Step 1
Someone has removed bones from the dinosaur skeleton and replaced them. Code your Agent to DESTROY the 4 orange blocks and PLACE the `Bone Block` we've given it.
#### ~ tutorialhint 
Use the ``||agent.agent move||`` to move your Agent and then ``||agent.agent destroy||`` in the direction you want the block orange blocks DESTROYED and ``||agent.agent place||`` to PLACE a `Bone Block` we've given the Agent. Repeat this until the right number of blocks are placed.

```ghost
    agent.move(FORWARD, 0)
    agent.destroy(FORWARD)
    agent.place(FORWARD)
    for (let index = 0; index < 4; index++) {
    	
    }
```
```template
\\
```
```package
```
