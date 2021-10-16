### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Pretty things!

## Step 1
Ваша задача состоит в том, чтобы построить чередующийся(через один) узор из блоков **кварцевой колонны** и **лазурита** вдоль края пола ванны. Начните с создания переменных ``||variable:blockA||`` и ``||variable:blockB||``. Установите для параметра ``||variable:blockA переменная||`` значение **блока кварца** и ``||variable:blockB переменная||`` для **блока из лазурита**. Добавьте команды в блок ``||loops:при начале||``.

## Step 2
``||logic: If||`` ``||count||`` = **0**, then agent needs to set ``||variable:blockA||``, ``||agent:destroy down||``, ``||agent:place down||`` and ``||variable:change the count by 1||``. ``||logic: Else||`` the Agent needs to set ``||blockB||``, place blocks and ``||change count by -1||``.  

## Step 3
The Agent needs to place blocks in a row ``||loops: while||`` it does ``||logic:not||`` ``|| detect||`` a block **forward**. 

## Step 4
There are **4** sides of reservoir that the Agent needs to complete, so add a ``||loops: repeat||`` block. Set the ``||count||`` to **0** before sending the Agent to place blocks.

```template
let count = 0
player.onChat("floor", function () {
    count = 0
})
```


```ghost
player.onChat("floor", function () {
    count = 0
    for (let index = 0; index < 4; index++) {
        while (!(agent.detect(AgentDetection.Block, FORWARD))) {
            if (count == 0) {
                agent.setItem(blockA, 1, 1)
                agent.destroy(DOWN)
                agent.place(DOWN)
                count += 1
            } else {
                agent.setItem(blockB, 1, 1)
                agent.destroy(DOWN)
                agent.place(DOWN)
                count += -1
            }
            agent.move(FORWARD, 1)
        }
        agent.turn(RIGHT_TURN)
    }
})
let count = 0
let blockB = 0
let blockA = 0
blockA = BLOCK_OF_QUARTZ
blockB = LAPIS_LAZULI_BLOCK
```
