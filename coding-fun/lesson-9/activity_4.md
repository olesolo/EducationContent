### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Repair the Rover 

## Step 1
Исправьте этот фрагмент кода. Вот цель: **исследуя** на наличие **блока воздуха** и **не** находя его, агент должен **перемещатся вправо**. Если агент находит блок **лазурита** **впереди**, ему нужно **переместится вправо**, **повернуть налево**, а затем **переместится вправо**. После этого агент должен сказать: «Нашел разрыв!»(Found the break!) и **поместите вперед блок красного камня**.


```template
player.onChat("repair", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) == AIR) {
        agent.move(RIGHT, 1)
        if (agent.inspect(AgentInspection.Block, FORWARD) == LAPIS_LAZULI_BLOCK) {
            agent.move(RIGHT, 1)
            agent.turn(RIGHT_TURN)
            agent.move(LEFT, 1)
        }
    }
    player.say("Found the break!")
    agent.setItem(GRASS, 1, 1)
    agent.place(FORWARD)
})
```
