### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Locate the cub!

## Step 1
Запрограммируйте Агента копать путь, не зная, как далеко он зайдет, с помощью команд ``||loops:while||`` и ``||agent:agent detect||``. Агенту нужно ``||agent:destroy forward & up||``, чтобы вы могли пройти через весь снег! Когда закончите, нажмите кнопку **Start**, чтобы скомпилировать код. Не забудьте запустить свой код в Minecraft.

#### ~ tutorialhint 
Посмотрите на формы фрагментов кода, когда вы соедините их вместе. Используйте ``||agent:agent move forward||``.

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
