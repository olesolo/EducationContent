### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# First Flight (Solution)

## Step 1
The below code is the correct solution to the activity. Run the code by pressing the green play button to see it in action.

#### ~ tutorialhint 
Use ``||agent.agent move||`` to send your Agent to the hole. Fill each hole using ``||agent.agent place||`` to PLACE the `Dirt` block we've given the Agent. Repeat ``||agent.agent move||`` and ``||agent.agent place||`` until all the holes are filled.

```ghost
    agent.move(FORWARD, 0)
    agent.place(FORWARD)
    for (let index = 0; index < 4; index++) {
    	
    }
```
```template
for (let index = 0; index < 2; index++) {
    agent.move(FORWARD, 1)    	
    agent.place(DOWN)
}
agent.move(FORWARD, 2)  
agent.move(RIGHT, 2)  
for (let index = 0; index < 2; index++) {
    agent.move(FORWARD, 1)    	
    agent.place(DOWN)    	
}
agent.move(FORWARD, 2)  
agent.move(RIGHT, 2) 
for (let index = 0; index < 2; index++) {
    agent.move(FORWARD, 1)    	
    agent.place(DOWN)    	
}
```
```package
```
