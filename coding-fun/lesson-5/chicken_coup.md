### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Chicken Coup

## Step 1
Агенту необходимо разместить **2** слоя по **9** блоков **железных прутьев**. Все **4** стороны должны быть с **железными прутьями**. Не забудьте использовать ``|| агент: агент двигаться вверх||``, чтобы построить второй уровень.

#### ~ tutorialhint
В конце у вас будут команды **3** ``||цикла: повторить||``, вложенные друг в друга. Убедитесь, что у Агента в инвентаре есть более 64 блоков!

```ghost
player.onChat("chicken", function () {
    for (let index = 0; index < 2; index++) {
        agent.setItem(IRON_BARS, 1, 1)
        for (let index = 0; index < 4; index++) {
            for (let index = 0; index < 9; index++) {
                agent.place(DOWN)
                agent.move(FORWARD, 1)
            }
            agent.turn(RIGHT_TURN)
        }
        agent.move(UP, 1)
    }
})

``` 
