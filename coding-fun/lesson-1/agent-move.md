### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# Program the Agent to move to the gold plate!

## Step 1
Выберите команду `` || player: on chat || '' и переименуйте ее с ** run ** на ** 1 **. Выберите блок `` || agent: agent move forward || '' и перетащите его в команду `` || player: on chat || ``. Измените ** количество ** шагов, которые агент делает, на ** 3 **, чтобы агент мог добраться до золотой пластины. Когда закончите, нажмите кнопку ** Play **, чтобы скомпилировать код, затем перейдите в Minecraft, нажмите ** t ** и введите ** 1 **.

#### ~ tutorialhint 
Вы можете изменить количество шагов, которые будет проходить ваш агент, изменив число внутри блока `` || agent: agent move || ''. Вы также можете использовать блок `` || агент: поворот агента || '', чтобы повернуть агента влево или вправо.



```ghost
player.onChat("1", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})

``` 
