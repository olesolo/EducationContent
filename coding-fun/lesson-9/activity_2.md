### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Deep Stone 

## Step 1
Исправьте этот фрагмент кода. Вот цель агента: копать и перемещаться вниз, пока не наткнется на **золотой блок** **внизу**. Спускаясь вниз, если Агент обнаружит, что перед ним **камень**, то разбить его и соберать.

```template
player.onChat("dig", function () {
    while (agent.inspect(AgentInspection.Block, LEFT) == AIR) {
        agent.destroy(DOWN)
        agent.move(DOWN, 1)
            if (agent.inspect(AgentInspection.Block, FORWARD) != GRASS) {
                player.say("Found the stone!")
                agent.destroy(FORWARD)
                agent.collectAll()
        }
    }
})
```


