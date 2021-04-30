### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Track Down the Rover 

## Step 1
Исправьте этот фрагмент кода. Вот цель: **исследуя блок** **впереди** и **не** находя **кварца**, Агент должен **переместится вперед**. Если он **обнаруживает** **золотой** блок **внизу**, ему нужно **повернуть направо**. Если он обнаруживает **железный блок** **внизу**, ему нужно **повернуть налево**. В конце агент должен сказать: «Нашел марсоход!»(Found rover!)


```template
player.onChat("rover", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) != BLOCK_OF_QUARTZ) {
            if (agent.inspect(AgentInspection.Block, UP) == GOLD_BLOCK) {
            agent.turn(LEFT_TURN)
        }
            if (agent.inspect(AgentInspection.Block, RIGHT) == IRON_BLOCK) {
            agent.turn(RIGHT_TURN)
        }
        agent.move(FORWARD, 1)
    }
    player.say("Found the rover!")
})
```

