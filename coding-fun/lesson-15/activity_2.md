### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Columns!

## Step 1
Время строить акведуки! Сначала создайте переменные ``||variable:l||``(длина) и ``||variable:s||``(сегменты). Затем поместите ``||variable:установить l||`` на **5** и ``||variable:установить s||`` на **6** в стартовый блок ``||loops: при начале||``.

## Step 2
Теперь в команде ``||player:при команде чата||`` вам нужно добавить все действия, которые Агент должен выполнить. Чтобы построить **1** часть: ``||agent:ставит блок или предмет - блок кварцевой колонны||`` **64** блока, ``||agent:разместить вниз, влево и вправо||`` и ``||agent:двигаться вперед||``. Вода в Minecraft будет течь, если есть наклон, поэтому Агенту нужно **размещать блоки ступенями**. Поместите все вышенаписанные действия в цикл ``||loops:повторить||``, который **повторяет** ``||variable:l||`` раз, т.е. вместо числа подставить **переменную l**. 

## Step 3
Теперь вложите первый цикл ``||loops:повторить||`` в другой цикл ``||loops:повторить||``, который повторяет ``||variables:s||`` раз. И чтобы получились ступени, добавьте блок ``||agent:агент двигается вниз||`` после первого цикла. И запустите это в Minecraft!

### ~ tutorialHint
Если не вышло, используйте рацию для сброса!

```ghost
player.onChat("build", function () {
    agent.move(DOWN, 1)
    for (let index = 0; index < Segments; index++) {
        for (let index = 0; index < length; index++) {
            agent.setItem(WHITE_CONCRETE, 64, 1)
            agent.place(LEFT)
            agent.place(RIGHT)
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.move(DOWN, 1)
    }
})
let Segments = 0
let length = 0
length = 5
Segments = 6
```
