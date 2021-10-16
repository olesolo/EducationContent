### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration false 
### @explicitHints 1


# Mining Quartz!

## Step 1
Напишите код, который **посчитает** сколько **блоков** вам понадобится для постройки оставшихся колонн. Вот некоторые факты: здесь **6 колонн** и высота каждой колонны **6 блоков**. Начните с создания и установки переменных ``||variable:height||``(высота) и ``||variable:qty||``(количество) на правильные числа ``||loops:при начале||``, затем создайте переменную ``|| variable:total||``(всего блоков) .

## Step 2
Задайте условие: ``||logic: если||`` ``||variable:total||``(всего блоков) = ``||variable:height||``(высота) * ``||variable:qty||``(количество), затем делать ``||player:сказать||`` «Collected enough blocks!».

## Step 3
Теперь добавьте команду ``||variable:изменить total||`` на 1 и ``|| player:сказать||`` ``||variable:total||``, чтобы вы знали сколько блоков вы собрали. Не забудьте добавить ``||blocks:при кварцевая колонна сломана||``, чтобы вы видели подсчет при разбивании блоков. Когда вы закончите, вы увидите сообщение "Collected enough blocks!"(Собрано достаточно блоков!).

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
