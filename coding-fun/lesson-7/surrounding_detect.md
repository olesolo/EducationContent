### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Surroundings 

## Step 1
Пока агент **осматривает блок внизу** и этот блок - **камень**, агенту необходимо **двигаться вперед**. Если агент **не** обнаруживает блок впереди, агент **двигается вперед**, иначе ему нужно **повернуть налево**.


```template
player.onChat("inspect", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == STONE) {
        
    }
})
```

```ghost
player.onChat("inspect", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == STONE) {
        if (!(agent.detect(AgentDetection.Block, FORWARD))) {
            agent.move(FORWARD, 1)
        } else {
            agent.turn(LEFT_TURN)
        }
    }
})
```

