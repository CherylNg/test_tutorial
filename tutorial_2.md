### @diffs true

# LIGHT UP! 

## Let's get ZOOM:BIT to turn ON its headlights! @unplugged

For this tutorial, we'll program ZOOM:BIT to automatically turn on its headlights when the surrounding is dim, and turn off when it is bright!

![ZOOM:BIT](https://raw.githubusercontent.com/CherylNg/test_tutorial/master/docs/static/ZipZipZoom.png)

```package
zoombit=github:CytronTechnologies/pxt-zoombit
```
```template
soundExpression.hello.playUntilDone()
soundExpression.twinkle.play()
basic.showString("Hello!")
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
    basic.showIcon(IconNames.SmallHeart)
    }
```

## Step 1
Click ``||logic:Logic||`` category and select ``||logic:if-then-else||`` block. 
Snap the block to the ``||basic:forever||`` block. 
Click ``||logic:Logic||`` category again and select ``||logic:0<0||`` block. Snap it to ``||logic:if||`` slot.

```blocks
soundExpression.hello.playUntilDone()
soundExpression.twinkle.play()
basic.showString("Hello!")
basic.forever(function () {
//@hightlight
    if (0 < 0){}
    else {}
    {
    basic.showIcon(IconNames.Heart)
    basic.showIcon(IconNames.SmallHeart)
    }
```

## Step 2
Click ``||input:Input||`` category and then select ``||input:light level||`` block. 
Snap the block to the left slot of the comparison block. 
Change the number on the right slot from 0 to **'50'**.

```blocks
soundExpression.hello.playUntilDone()
soundExpression.twinkle.play()
basic.showString("Hello!")
basic.forever(function () {
//@hightlight
    if (input.lightLevel() < 50){}
    else {}
    {
    basic.showIcon(IconNames.Heart)
    basic.showIcon(IconNames.SmallHeart)
    }
```
## Step 3
Click ``||zoombit:ZOOM:BIT||`` category and select ``||zoombit:set (left) headlight to (on)||`` block. 
Attach to the top slot of the ``||logic:if-then-else||`` block. Click on the setting ``||zoombit:left||`` and change to ``||zoombit:all||``. 

```blocks
soundExpression.hello.playUntilDone()
soundExpression.twinkle.play()
basic.showString("Hello!")
basic.forever(function () {
    if (input.lightLevel() < 50)
    //@hightlight 
    {
        zoombit.setHeadlight(HeadlightChannel.All, zoombit.digitalStatePicker(DigitalIoState.On))
    } else {}
    {
    basic.showIcon(IconNames.Heart)
    basic.showIcon(IconNames.SmallHeart)
    }
```

## Step 4
Right-click on the ``||zoombit:set (all) headlight to (on)||`` block and then select **'duplicate'**. 
Snap the duplicated block to the bottom slot of the ``||logic:if-then-else||`` block and change the setting ``||zoombit:on||`` to ``||zoombit:off||``.

```blocks
soundExpression.hello.playUntilDone()
soundExpression.twinkle.play()
basic.showString("Hello!")
basic.forever(function () {
    if (input.lightLevel() < 50)
    //@hightlight 
    {
        zoombit.setHeadlight(HeadlightChannel.All, zoombit.digitalStatePicker(DigitalIoState.On))
    } else {
        zoombit.setHeadlight(HeadlightChannel.All, zoombit.digitalStatePicker(DigitalIoState.Off))}
    {
    basic.showIcon(IconNames.Heart)
    basic.showIcon(IconNames.SmallHeart)
    }
```