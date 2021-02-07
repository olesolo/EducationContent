### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Secure the Area

## Step 1
Запрограммируйте Агента построить **дубовый забор**. Агенту нужно расставить блоки **дубовый забор** справа, разрушать препятствия перед собой и двигаться вперед. Забор должен быть **17 блоков** в длину.
#### ~ tutorialhint
Убедитесь, что агент размещает блоки справа и уничтожает блоки перед собой.

```blocks
player.onChat("fence", function () {
    agent.setItem(OAK_FENCE, 64, 1)
    for (let index = 0; index < 17; index++) {
            }
})
```
```ghost
player.onChat("fence", function () {
    agent.setItem(OAK_FENCE, 64, 1)
    for (let index = 0; index < 17; index++) {
        agent.place(RIGHT)
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
``` 

