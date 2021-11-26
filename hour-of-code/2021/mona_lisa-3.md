### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# The Mona Lisa (Solution)

## Step 1
The below code is the correct solution to the activity. Run the code by pressing the green play button to see it in action.

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
for (let index = 0; index < 5; index++) {
    agent.move(FORWARD, 1)
    agent.place(DOWN)
}
agent.turn(RIGHT_TURN)
for (let index = 0; index < 5; index++) {
    agent.move(FORWARD, 1)
    agent.place(DOWN)    	
}
```
```package
```
