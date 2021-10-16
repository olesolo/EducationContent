### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Columns!

## Step 1
Время строить акведуки! Сначала создайте переменные ``||variable:length||``(длина) и ``||variable:segments||``(сегменты). Затем ``||variable: установить length||`` на **5** и ``||variable:установить seg||`` на **6** ``||loops: при начале||``.

## Step 2
Теперь в команде ``||player: при команде чата||`` вам нужно добавить все действия, которые Агент должен выполнить. Чтобы построить **1** часть: ``||agent:получить блок кварцевой колонны||`` **64** блока, ``||agent:разместить||`` и ``||agent:двигаться вперед||``. Вода в Minecraft будет течь, если есть наклон, поэтому Агенту нужно **размещать блоки влево, вправо и вниз**. Поместите все эти действия в цикл ``||loops: повторить||``, который **повторяет** ``||variable:length||`` раз, т.е. вместо числа подставить **переменную**.

## Step 3
Теперь вложите первый цикл ``||loops:повторить||`` в другой цикл ``||loops:повторить||``, который повторяет ``||variables:segments||`` раз. Попробуйте это в Minecraft!

### ~ tutorialHint
Добавьте блок ``||agent: агент двигается вниз||`` перед внутренним циклом, чтобы код заработал!

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
