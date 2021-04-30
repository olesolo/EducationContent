### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Locating stone 

## Step 1
Исправьте этот фрагмент кода. Вот что нужно сделать агенту: **переместиться влево 4 раз**, **уничтожить вниз**, **переместиться вниз**. Если агент обнаруживает **камень** впереди, он должен сказать: «Камень нашел!»(Found stone!), **уничтожить вперед** и **собрать все**. Если камень **не обнаружен**, агент должен сказать: «Здесь камня нет!»(No stone here!). Каждый раз после спуска Агент должен **переместиться вверх на 1 блок**. Эти все действия нужно повторить **4** раза.



```template
player.onChat("stone", function () {
    for (let index = 0; index < 3; index++) {
        agent.move(RIGHT, 4)
        agent.destroy(DOWN)
        agent.move(DOWN, 1)
        if (agent.inspect(AgentInspection.Block, FORWARD) != STONE) {
            player.say("Found the stone!")
            agent.destroy(FORWARD)
            agent.collectAll()
        } else {
            player.say("No stone here!")
        }
        agent.move(UP, 1)
    }
})
```
