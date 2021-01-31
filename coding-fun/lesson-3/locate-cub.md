### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Locate the cub!

## Step 1
Program the Agent to dig a path without knowing how far it goes by using ``||loops:while||`` & ``||agent:agent detect||`` commands. The Agent needs to ``||agent:destroy forward & up||`` for you to be able to walk through all the snow! When done, press the **Play** button to compile the code. Don't forget to run your code in Minecraft. 

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
