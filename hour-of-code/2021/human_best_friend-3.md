### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# Human's Best Friends (Solution)

## Step 1
The below code is the correct solution to the activity. Run the code by pressing the green play button to see it in action.
#### ~ tutorialhint 
Move your Agent to the right place using ``||agent.agent move||`` and ``||agent.agent turn||``. At the right point use ``||agent.agent drop||`` to DROP a `Beetroot` we've given the Agent. Repeat this until the right number of `Beetroot` are placed 5 blocks apart.

```ghost
    agent.move(FORWARD, 0)
    agent.drop(FORWARD, 0, 0)
    for (let index = 0; index < 4; index++) {
    	
    }
```
```template
for (let index = 0; index < 6; index++) {
    agent.drop(FORWARD, 1, 1)
    agent.move(FORWARD, 4)
}
```
```package
```
