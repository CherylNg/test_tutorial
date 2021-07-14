# Let's get ZOOM:BIT to turn ON its headlights!

## Light UP! @unplugged

For this tutorial, we'll program ZOOM:BIT to automatically turn on its headlights when the surrounding is dim, and turn off when it is bright!

![ZOOM:BIT](https://raw.githubusercontent.com/CherylNg/test_tutorial/master/docs/static/ZipZipZoom.png)


## Step 1
Click ``||logic:Logic]||`` category and select ``||logic:[if-then-else]||`` block and ``||logic:[ __<__ ]||`` comparison block. 
Place the comparison block in the "if" slot.

```template
soundExpression.hello.playUntilDone()
soundExpression.twinkle.play()
basic.showString("Hello!")
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
    basic.showIcon(IconNames.SmallHeart)
    }
```
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

 