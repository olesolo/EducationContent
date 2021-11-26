### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# The Great Wall of China (Debug)

## Step 1
There's something wrong with the below code. Press the green play button to run it to see what happens, and then debug it to see what's wrong and what changes are needed to make it work.

#### ~ tutorialhint 
Use the ``||agent.agent move||`` block to position your Agent and ``||agent.agent place||`` to PLACE the `Bamboo` we've given the Agent.

```ghost
    agent.place(FORWARD)
    agent.move(FORWARD, 0)
    for (let index = 0; index < 4; index++) {
    	
    }
```
```template
for (let index = 0; index < 3; index++) {
    agent.place(UP)
    agent.move(BACK, 1)
}
```
```package
```
