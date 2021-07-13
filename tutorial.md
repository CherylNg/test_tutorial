# Let's get ZOOM:BIT to say Hello!

## Hello World @unplugged

For this tutorial, we'll program ZOOM:BIT to say Hello when powered up.

![ZOOM:BIT](/docs/static/ZipZipZoom.png)


## Step 1
From the ``||music:Music||`` category, get a ``||music:play sound (giggle) until done||`` block. 
Click and snap the block to the ``||basic:on start||`` container. 

```blocks 
//@highlight
soundExpression.giggle.playUntilDone()
```
## Step 2
Click on ``||music:giggle||`` and select ``||music:hello||`` from the dropdown list.

```blocks 
//@highlight
soundExpression.hello.playUntilDone()
```

## Step 3
From the ``||music:Music||`` category, get a ``||music:play sound (giggle)||`` block. 
Click and snap the block to the ``||basic:on start||`` container. 

```blocks 
soundExpression.hello.playUntilDone()
//@highlight
soundExpression.giggle.play()
```

## Step 4

Click on ``||music:(giggle)||`` and select ``||music:(twinkle)||`` (or any other sound expression that you like) from the dropdown list.

```blocks 
soundExpression.hello.playUntilDone()
//@highlight
soundExpression.twinkle.play()
```

## Step 5

Click ``||basic:Basic||`` and add a ``||basic:showString (Hello!)||`` block to your code.

```blocks 
soundExpression.hello.playUntilDone()
soundExpression.twinkle.play()
//@highlight
basic.showString("Hello!")
```

## Step 6

From the ``||basic:Basic||`` category, get two ``||basic:show icon (heart)||`` blocks. 
Snap both blocks to the ``||basic:forever||`` container. 

```blocks 
soundExpression.hello.playUntilDone()
soundExpression.twinkle.play()
basic.showString("Hello!")
//@highlight
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
    basic.showIcon(IconNames.Heart)
    }
```

## Step 7

Click the ``||basic:(heart)||`` icon of the bottom block and then select the ``||basic:(small heart)||`` icon.

```blocks 
soundExpression.hello.playUntilDone()
soundExpression.twinkle.play()
basic.showString("Hello!")
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
    //@highlight
    basic.showIcon(IconNames.SmallHeart)
    }
```

## Step 8

Download the code to your ZOOM:BIT and power it up by sliding the power switch to **ON**.
Check out this **[demo video](https://youtu.be/-FZ8yTnoozY)** if you're not sure how to download the code. 

## Congratulations!! You have taught ZOOM:BIT to say hello~ @unplugged

Do you hear ZOOM:BIT greeting you? Do you see "Hello!" scroll across the LED matrix? If you missed it, you can slide the power switch to OFF, and then turn it ON again to reset.

![ZOOM:BIT](/docs/static/ZipZipZoom.png)


<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
