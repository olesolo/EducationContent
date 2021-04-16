### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Reach magma

## Step 1
Запрограммируйте агента **двигаться вперед**. Пока агент **проверяет** блок **внизу** и это **не магма**, агенту необходимо **двигаться вниз** уничтожая все препятствия под собой.


```ghost
player.onChat("magma", function () {
    agent.move(FORWARD, 1)
    while (agent.inspect(AgentInspection.Block, DOWN) != MAGMA_BLOCK) {
        agent.move(DOWN, 1)
    }
})
```

