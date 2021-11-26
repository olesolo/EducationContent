### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# Human's Best Friends

## Step 1
Dogs have been friends with people for thousands of years. But, something has scared the dogs away. Code your Agent to DROP the `Beetroot` items we've given it 5 blocks apart to help the people tame the wolves into dogs.
#### ~ tutorialhint 
Move your Agent to the right place using ``||agent.agent move||`` and ``||agent.agent turn||``. At the right point use ``||agent.agent drop||`` to DROP a `Beetroot` we've given the Agent. Repeat this until the right number of `Beetroot` are placed 5 blocks apart.

```ghost
    agent.move(FORWARD, 0)
    agent.drop(FORWARD, 0, 0)
    for (let index = 0; index < 4; index++) {
    	
    }
```
```template
\\
```
```package
```
