### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Separated Family!

## Step 1
Запрограммируйте агента построить мост через пропасть во льду. Убедитесь, что у Агента есть **64** блока **дубовых досок** в инвентаре.

#### ~ tutorialhint 
Не забудьте использовать **not** в цикле **while**. Подумайте, где вы хотите, чтобы агент расставлял блоки.


```ghost
player.onChat("family", function () {
    agent.setItem(PLANKS_OAK, 64, 1)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
        agent.turn(LEFT_TURN)
    }
})

``` 