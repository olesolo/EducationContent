### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# 3d Space

## Step 1
Чтобы решить эту задачу, вам нужно запрограммировать Агента, чтобы он дошел до **золотого** блока и забрал его. Агент должен сделать это на уровне земли, а затем **переместиться на 3 блока вверх** и повторить предыдущую процедуру.

```template
player.onChat("3D", function () {
    for (let index = 0; index < 2; index++) {
        
})
``` 
```ghost
player.onChat("3D", function () {
    for (let index = 0; index < 2; index++) {
        while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
            if (!(agent.detect(AgentDetection.Block, FORWARD))) {
                agent.move(FORWARD, 1)
            } else {
                agent.turn(LEFT_TURN)
            }
        }
        agent.destroy(FORWARD)
        agent.collectAll()
        agent.move(UP, 3)
    }
})
```