### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @explicitHints 1


# Make the area pretty!

## Step 1
Вам нужно посадить **14 одуванчиков** вдоль **4** сторон убежища. Агент может посадить **14** одуванчиков с одной стороны. 

#### ~ tutorialhint 
Не забудьте выбрать счетчик для команды ``||agent:agent set block||``.


```ghost
player.onChat("flower", function () {
    for (let index = 0; index < 4; index++) {
        for (let index = 0; index < 14; index++) {
            agent.setItem(YELLOW_FLOWER, 64, 1)
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.turn(RIGHT_TURN)
    }
})

``` 
