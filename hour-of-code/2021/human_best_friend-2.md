### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# Human's Best Friends (Debug)

## Step 1
There's something wrong with the below code. Press the green play button to run it to see what happens, and then debug it to see what's wrong and what changes are needed to make it work.
#### ~ tutorialhint 
Move your Agent to the right place using ``||agent.agent move||`` and ``||agent.agent turn||``. At the right point use ``||agent.agent drop||`` to DROP a `Beetroot` we've given the Agent. Repeat this until the right number of `Beetroot` are placed 5 blocks apart.

```ghost
    agent.move(FORWARD, 0)
    agent.drop(FORWARD, 0, 0)
    for (let index = 0; index < 4; index++) {
    	
    }
```
```template
for (let index = 0; index < 5; index++) {
    agent.drop(FORWARD, 1, 1)
    agent.move(FORWARD, 1)
}
```
```package
```
