### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @flyoutOnly 1
### @explicitHints 1


# Hazing Two

## Step 1
Шаг 1 - убрать маскировку.

## Step 2
Когда закончите, нажмите кнопку **Старт**, чтобы скомпилировать код. Не забудьте запустить свой код в Minecraft.

```blocks
player.onChat("run", function () {
    while (agent.detect(AgentDetection.Block, FORWARD)) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        agent.destroy(UP)
    }
})

``` 
