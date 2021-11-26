### @flyoutOnly true
### @hideIteration true
### @explicitHints true

# Great Pyramid at Giza

## Step 1
Help the Architect finish the triangle, a design that will stand the test of time. Think how to create a triangle. There are 2 more levels needed: 3 blocks on the bottom, and 1 block on the top.

#### ~ tutorialhint 
Think about how the Agent needs to move to place the right number of blocks for each level of the pyramid. Use the ``||agent.agent move||`` block to move your agent forward and for each step use ``||agent.agent place||`` to PLACE the `Smooth Sandstone` we've given the Agent.

```ghost
    agent.move(FORWARD, 0)
    agent.place(FORWARD)
    agent.turn(LEFT_TURN)
    for (let index = 0; index < 4; index++) {
    	
    }
```
```template
\\
```
```package
```
