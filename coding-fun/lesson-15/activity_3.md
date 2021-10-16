### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Pretty things!

## Step 1
Ваша задача состоит в том, чтобы построить чередующийся(через один) узор из блоков **кварца** и **лазурита** покругу, вдоль края пола ванны. Начните с создания переменных ``||variable:blockA||`` и ``||variable:blockB||``. Установите для параметра в переменной ``||variable:blockA||`` значение **блока кварца** и для переменной ``||variable:blockB||`` **блок лазурита**. Добавьте команды в блок ``||loops:при начале||``.

## Step 2
``||logic:Если||`` ``||count||`` = **0**, тогда Агент должен получить (команда ставит блок или предмет) 1 ``||variable:blockA||``, ``||agent:уничтожить вниз||``, ``||agent:разместить вниз||`` и ``||variable:изменить count на 1||``. ``||logic:Иначе||`` Агент должен установить `` ||blockB||``, уничтожить и разместить блок вниз, и ``||variable:изменить счетчик на -1||``.

## Step 3
Агенту необходимо размещать блоки один за другим ``||loops:пока||`` он ``||logic:не||`` ``||обнаружит||`` блок **впереди**.

## Step 4
Агенту необходимо заполнить все **4** стороны ванны, поэтому добавьте блок ``||loops:повторить||``. Установите для параметра ``||count||`` значение **0** перед отправкой Агента для размещения блоков.

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
