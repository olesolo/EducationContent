### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Locate the Sample! 

## Step 1
**Пока** агент **осматривает блок внизу** и **не** находит **синий лед**, запрограммируйте агента **уничтожить** и **двигаться вниз**. Когда агент найдет **синий лед**, ему необходимо **уничтожить его** и **собрать** образец.

```ghost 
player.onChat("ice", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != ICE) {
        agent.destroy(DOWN)
        agent.move(DOWN, 1)
    }
    agent.destroy(DOWN)
    agent.collectAll()
    
})
```

