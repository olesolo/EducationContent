### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Iron

## Step 1
Пока агент **проверяет блок внизу** и этот блок не является **железной рудой**, он должен **двигаться вперед**. Если Агент **обнаруживает блок впереди**, ему необходимо **уничтожить блок впереди**. Когда Агент обнаруживает железо, запрограммируйте его **собирать** его. Обратите внимание, что для того, чтобы собрать блок, Агент должен сначала его уничтожить.

```ghost
player.onChat("4", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != IRON_ORE) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(FORWARD)
        }
        agent.move(FORWARD, 1)
    }
    player.say("Found the iron ore!")
    agent.destroy(DOWN)
    agent.collectAll()
})
```
