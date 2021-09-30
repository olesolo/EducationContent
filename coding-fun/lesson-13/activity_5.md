### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Make it rain!

## Step 1
Пусть идет дождь, пока вы танцуете в Minecraft! Для этого вам нужно будет использовать несколько обработчиков событий. 1. Создайте свои переменные, например: **walk** (прогулка), **jump** (прыжок) и/или **break** (стоп). 2. Выберите обработчики событий, например ``||player: при условии что игрок - падение||``, ``||player: при условии что игрок - ходьба||``. 3. Добавьте блок ``||variables:установить переменную||`` **jump** в событие падения и вместо цифры вставьте внутрь ``||logic: истина||``. Тоже самое проделайте с событием ходьбы и переменной **walk** 4. Используйте блок ``||loop: всегда||`` и перетащите внутрь него ``||logic:если||``. Установите для всех ваших условий значение ``||logic:истина||`` и добавьте внутрь блок ``|| gameplay:погода||``, установленный на **дождь**.

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
