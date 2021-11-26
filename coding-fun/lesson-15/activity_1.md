### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Mining Quartz!

## Step 1
Напишите код, который **посчитает** сколько **блоков** вам понадобится для постройки оставшихся колонн. Нам нужно построить **6 колонн** и высота каждой колонны **6 блоков**. Начните с создания переменных ``||variable:h||``(высота) и ``||variable:q||``(количество). Далее ``||loops:при начале||`` установите их значения на указанные выше (h = 6, q = 6). Затем создайте переменную ``||variable:total||`` в ней мы будем хранить общее количество блоков которое нам нужно.

## Step 2
Задайте условие: ``||logic:если||`` ``||variable:total||``(всего блоков) = ``||variable:h||``(высота) * ``||variable:q||``(количество), затем делать ``||player:сказать||`` «Good job!».

## Step 3
Не забудьте добавить ``||blocks:при кварцевая колонна сломана||`` и в него команду ``||variable:изменить total||`` на 1 и ``|| player:сказать||`` ``||variable:total||``, чтобы вы знали сколько блоков уже собрали. Теперь когда вы будете ломать блоки кварца, вы увидите подсчет блоков. Когда вы собирете нужное количество, вы увидите сообщение "Good job!".

```ghost
blocks.onBlockBroken(PILLAR_QUARTZ_BLOCK, function () {
    total_blocks += 1
    if (total_blocks == height * quantity) {
        player.say("Collected enough blocks!")
    }
})
let total_blocks = 0
let quantity = 0
let height = 0
height = 6
quantity = 6
```
