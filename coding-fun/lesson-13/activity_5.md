### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Make it rain!

## Step 1
Пусть идет дождь, пока вы танцуете в Minecraft! Для этого вам нужно будет использовать несколько обработчиков событий. 1. Создайте свои переменные, например: **walk** (прогулка), **jump** (прыжок) и/или **break** (стоп). 2. Выберите обработчики событий, например ``||игрок: при условии что игрок - падение||``, ``||игрок: при условии что игрок - ходьба||``. 3. Добавьте блок ``||переменные:установить переменную||`` **jump** в событие падения и вместо цифры вставьте внутрь ``||логика: истина||``. Тоже самое проделайте с событием ходьбы и переменной **walk** 4. Используйте блок ``||циклы: всегда||`` и перетащите внутрь него ``||логика:если||``. Установите для всех ваших условий значение ``||логика:истина||`` и добавьте внутрь блок ``|| игровой процесс:погода||``, установленный на **дождь**.

### ~ tutorialHint
```blocks
let walk = false
player.onTravelled(WALK, function () {
    walk = true
})
loops.forever(function () {
    if (walk == true && "" == "") {
    	
    }
})

```

```ghost
let climb = false
let walk = false
let _break = false
player.onTravelled(CLIMB, function () {
    climb = true
})
player.onTravelled(WALK, function () {
    walk = true
})
blocks.onBlockBroken(STONE, function () {
    _break = true
})
loops.forever(function () {
    if (walk == true && climb == (true && _break == true)) {
        gameplay.setWeather(RAIN)
    }
})
```
