### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Locate the cub!

## Step 1
Запрограммируйте Агента копать тунель, не зная, как далеко он зайдет, с помощью команд ``||loops:пока||`` и ``||agent:агент обнаружить||``. Агенту нужно ``||agent:уничтожить вперед и вверх||``, чтобы вы могли пройти через весь снег! Когда закончите, нажмите кнопку **Start**, чтобы скомпилировать код. Не забудьте запустить свой код в Minecraft.

#### ~ tutorialhint 
После того как разобьете лед перед собой незабудьте сделать шаг вперед для движения дальше. Используйте ``||agent:агент переместиться вперед||``.

```template
player.onChat("cub", function () {
    while (agent.detect(AgentDetection.Block, FORWARD)) {
    	
    }
})
```

```ghost
player.onChat("cub", function () {
    while (agent.detect(AgentDetection.Block, FORWARD)) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        agent.destroy(UP)
    }
})

``` 