### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Cattle

## Step 1
Посмотрите на стартовый код и попробуйте запустить его. Этот код позволяет вам перемещать агента, не считая пройденные блоки. Посмотрите на путь, который должен пройти агент, и убедитесь, что вы выставили правильные повороты для агента. Убедитесь, что агент может добраться до **золотой пластины**.  

```template
player.onChat("sheep", function () {
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.move(FORWARD, 1)
    }
    agent.turn(LEFT_TURN)
})

``` 

