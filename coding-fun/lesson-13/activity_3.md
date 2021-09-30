### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Building

## Step 1
``||mobs:Дать цели||`` себе не менее **34 изумрудных** блоков. Создайте новую ``||переменную||`` и назовите ее **count**. Возьмите стартовый блок условие ``||blocks: при условии, что блок размещен||`` и выберите в нем значение **изумруд**. Перетащите блок ``||variables:изменить значение||`` внутрь ``||blocks: при условии, что блок размещен||``. Еще добавьте блок ``||player: сказать||`` и в него вставьте круглый блок переменной ``||count||``. Теперь, когда вы ставите блоки, игра будет считать, сколько блоков вы разместили.

### ~ tutorialhint 

Вы можете выбрать железо, золото, изумруд или алмаз.

```blocks
let count = 0
blocks.onBlockPlaced(EMERALD_BLOCK, function () {
    count += 1
    player.say(count)
})

```

```ghost
blocks.onBlockBroken(STONE, function () {
    count += 1
    player.say(count)
})
let count = 0
mobs.give(
mobs.target(NEAREST_PLAYER),
STONE,
1
)
})
```


