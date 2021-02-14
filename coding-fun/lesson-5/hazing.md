### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Hazing 

## Step 1
Агент должен установить **натяжной датчик**, чтобы волки не могли попасть внутрь. Установите ``||агент: агент получить блок||`` на **натяжной датчик** и установите счетчик на **64**, чтобы получить 64 датчиков . Используйте блок ``||циклы: пока||`` и поместите в него условие.

#### ~ tutorialhint
Remember to use **not** in your condition. 
Не забудьте использовать условие **не** (Логика) в вашем условии.

```blocks
player.onChat("hazing", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
    	
    }
})

``` 
```ghost
player.onChat("hazing", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
})
```
