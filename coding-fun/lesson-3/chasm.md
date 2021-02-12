### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# The great chasm!

## Step 1
Запрограммируйте агента **построить мост** через ледяную пропасть. Используйте команду ``||agent:выдать блок или вещь||``, чтобы убедиться, что у Агента есть необходимые материалы в инвентаре. Выберите **дуб** в качестве строительного материала и **64** для **количества блоков**. ``||loops:пока||`` Агент **не** обнаруживает блоки вниз, запрограммируйте Агента, чтобы он поместил дубовые доски **вниз**(под собой) и двигался **вперед**, чтобы построить мост.


```template
player.onChat("chasm", function () {
    agent.setItem(PLANKS_OAK, 1, 1)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, DOWN))) {
    	
    }
})
```

```ghost
player.onChat("chasm", function () {
    agent.setItem(PLANKS_OAK, 64, 1)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
})

``` 