### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Higher Ground!

## Step 1
Program the Agent to build a tower with **oak** blocks that is **10** blocks high. First, ensure that the Agent has **64** blocks of **oak plank**  using ``||agent:set block or item||`` command. Program the Agent to place oak planks **forward**, **left** & **right** by using ``||agent:agent place||`` block. The Agent needs to **move up** after placing the blocks.  

Запрограммируйте агента построить башню из **дубовых** блоков высотой **10** блоков. Во-первых, убедитесь, что у Агента есть **64** блока **дубовой доски**, используя команду ``||agent:set block or item||``. Запрограммируйте агента на размещение дубовых досок **вперед**, **влево** и **вправо** с помощью блока ``||agent:agent place||``. Агент должен **двигаться вверх** после размещения блоков.

#### ~ tutorialhint 
Попробуйте использовать блок ``||loops:repeat||`` и измените число на **10**.

## Step 2
Запрограммируйте агента спуститься **вниз** с башни и построить **лестницу** высотой **10** блоков. Вам нужна лестница, чтобы вы могли подняться наверх!

#### ~ tutorialhint 
Не забудьте выбрать **64** блока **лестницы** в инвентаре Агента с помощью ``||agent: agent set block||``, чтобы Агент мог разместить лестницу.


```ghost
player.onChat("tower", function () {
    agent.move(FORWARD, 1)
    agent.setItem(LADDER, 64, 1)
    for (let index = 0; index < 10; index++) {
        agent.place(FORWARD)
        agent.move(UP, 1)
    }
    agent.move(DOWN, 10)
})

``` 


