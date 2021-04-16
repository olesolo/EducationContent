### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Surroundings 

## Step 1
Пока агент **обнаруживает блок внизу (под собой)**, ему нужно двигаться вперед. Если агент **осматривает блок внизу** и находит **воздух**, используйте команду ``||игрок: сказать||``, чтобы сказать **Кратер найден!**.



```template
player.onChat("crater", function () {
            player.say("Crater found!")
})
```
```ghost
player.onChat("1", function () {
    while (agent.detect(AgentDetection.Block, DOWN)) {
        agent.move(FORWARD, 1)
    }
    if (agent.inspect(AgentInspection.Block, DOWN) == AIR) {
        player.say("Crater found!")
    }
})
```