### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# Paleontology Puzzle (Solution)

## Step 1
The below code is the correct solution to the activity. Run the code by pressing the green play button to see it in action.
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
for (let index = 0; index < 4; index++) {
    agent.move(FORWARD, 2)    
    agent.destroy(DOWN)
    agent.place(DOWN)
}
```
```package
```
