### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# First Flight (Debug)

## Step 1
There's something wrong with the below code. Press the green play button to run it to see what happens, and then debug it to see what's wrong and what changes are needed to make it work.

#### ~ tutorialhint 
Use ``||agent.agent move||`` to send your Agent to the hole. Fill each hole using ``||agent.agent place||`` to PLACE the `Dirt` block we've given the Agent. Repeat ``||agent.agent move||`` and ``||agent.agent place||`` until all the holes are filled.

```ghost
    agent.move(FORWARD, 0)
    agent.place(FORWARD)
    for (let index = 0; index < 4; index++) {
    	
    }
```
```template
for (let index = 0; index < 3; index++) {
    agent.move(FORWARD, 1)    	
    agent.place(UP)
}
agent.move(FORWARD, 2)  
agent.move(RIGHT, 2)  
for (let index = 0; index < 3; index++) {
    agent.move(FORWARD, 1)    	
    agent.place(UP)    	
}
agent.move(FORWARD, 2)  
agent.move(RIGHT, 2) 
for (let index = 0; index < 3; index++) {
    agent.move(FORWARD, 1)    	
    agent.place(UP)    	
}
```
```package
```
