### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# First Flight

## Step 1
One of the first planes is about to take off, but there are holes in the runway! Code your Agent to fill the holes with `Dirt` blocks we've given it. 

#### ~ tutorialhint 
Use ``||agent.agent move||`` to send your Agent to the hole. Fill each hole using ``||agent.agent place||`` to PLACE the `Dirt` block we've given the Agent. Repeat ``||agent.agent move||`` and ``||agent.agent place||`` until all the holes are filled.

```ghost
    agent.move(FORWARD, 0)
    agent.place(FORWARD)
    for (let index = 0; index < 4; index++) {
    	
    }
```
```template
\\
```
```package
```
