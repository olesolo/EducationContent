
### @hideIteration false 
### @flyoutOnly 1
### @explicitHints 1


# Hazing One

## Step 1
Установите для параметра ``||агент: агент получить блок||`` значение **натяжной датчик** и установите счетчик на **64**.

## Step 2
Используйте блок ``||циклы: пока||`` и поместите условие внутрь блока ``||циклы: пока||``.

#### ~ tutorialhint

```blocks
player.onChat("hazing", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
    	
    }
})

``` 
## Step 3
Add ``||agent: agent place||`` and ``||agent: agent move||`` blocks inside the ``||loops:while||`` block. 

```blocks
player.onChat("run", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
})
```