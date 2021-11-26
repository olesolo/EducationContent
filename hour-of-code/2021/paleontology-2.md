### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# Paleontology Puzzle (Debug)

## Step 1
There's something wrong with the below code. Press the green play button to run it to see what happens, and then debug it to see what's wrong and what changes are needed to make it work.
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
for (let index = 0; index < 3; index++) {
    agent.move(FORWARD, 2)    
    agent.destroy(DOWN)
    agent.place(UP)
}
```
```package
```
