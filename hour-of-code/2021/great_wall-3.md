### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# The Great Wall of China (Solution)

## Step 1
The below code is the correct solution to the activity. Run the code by pressing the green play button to see it in action.

#### ~ tutorialhint 
Use the ``||agent.agent move||`` block to position your Agent and ``||agent.agent place||`` to PLACE the `Bamboo` we've given the Agent.

```ghost
    agent.place(FORWARD)
    agent.move(FORWARD, 0)
    for (let index = 0; index < 4; index++) {
    	
    }
```
```template
for (let index = 0; index < 5; index++) {
    agent.place(DOWN)
    agent.move(FORWARD, 1)
}
```
```package
```
