### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Bamboo Hideaway

## Step 1
Запрограммируйте Агента посадить **3** блока бамбука с каждой стороны песчаного участка. Добавьте команду ``||agent: агент поворот||``, в конце цикла, чтобы агент мог завершить действие.

#### ~ tutorialhint
Должно быть 2 **повторяющихся** цикла, один вложенный в другой.
 
```ghost
player.onChat("bamboo", function () {
    for (let index = 0; index < 3; index++) {
        agent.setItem(BAMBOO, 64, 1)
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
    agent.turn(RIGHT_TURN)
})
```


