### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Spiral

## Step 1
Пока агент **проверяет блок вперед** и блок **не является** **золотым блоком**, агенту необходимо **двигаться вперед**. Если агент **не** обнаруживает блок впереди, то ему необходимо двигаться вперед, иначе ему нужно **повернуть налево**. Когда агент дойдет до **золотого блока**, ему нужно **уничтожить** и **собрать** его.


```ghost
player.onChat("3", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
        if (!(agent.detect(AgentDetection.Block, FORWARD))) {
            agent.move(FORWARD, 1)
        } else {
            agent.turn(LEFT_TURN)
        }
    }
    agent.destroy(FORWARD)
    agent.collectAll()
})
```
