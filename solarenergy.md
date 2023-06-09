# Solar Panel
```package
fwd-edu-breakout=github:climate-action-kits/pxt-fwd-edu/fwd-breakout
solar=github:climate-action-kits/pxt-fwd-edu
```
## Step 1 @showdialog
Welcome to the Solar Panel Coding Tutorial
![built project](https://raw.githubusercontent.com/mbakhtar/iste-solar-energy-v1/master/project%20-%20solar-400.png)

## Step 2 @showdialog
Plug your USB cable into the micro:bit. 
![breakout board](https://raw.githubusercontent.com/mbakhtar/tree-seeder-v1/master/connect-microbit.gif)

## Step 3 @showdialog
Insert it into the Climate Action Kit board. 
![breakout board](https://raw.githubusercontent.com/mbakhtar/wind-turbine-lesson-tutorial/master/breakout-resized.png)

## Step 4 @showhint
Click three dots besides ``|Download|`` button and follow the steps to pair your micro:bit.
![pair gif](https://raw.githubusercontent.com/mbakhtar/iste-electric-vehicle-v1/master/pair%20microbit-280x203.gif)

## Step 5 
Click ``||Variables:Variables||``. Click on |Make a Variable| to
create a new ``||Variables:Variable||``.
Name it ``||Variables:position||``.

## Step 6
Inside ``||Variables:Variables||`` there is ``||Variables:position||``
and more blocks.

## Step 7 
Click ``||Variables:Variables||``. Drag and drop
``||Variables:set position to 0||`` inside ``||basic:on start||`` block. 
Change ``||Variables:0||`` to ``||Variables:-90||``.
```blocks
let position = -90
basic.forever(function(){
})
```
## Step 8 
Click ``||logic:Logic||`` drag and drop ``||logic:If true then else||``
block inside the ``||basic:forever||`` loop.
```blocks
let position = -90
basic.forever(function(){
    if(true){
    }
    else{
    }
})
```
## Step 9 
Click ``||logic:Logic||`` drag and drop ``||logic:comparison block||`` ``||logic: greater than >||`` to
replace ``||logic:true||`` condition of the ``||logic: if then else||`` loop.
```blocks
let position = -90
basic.forever(function(){
    if(0>0){
    }
    else{
    }
})
```
## Step 10 
Click ``||fwdSensors:Sensors||`` drag and drop ``||fwdSensors:solar1 light level %||``
block to replace ``||0||`` on left side of the ``||logic:comparison||`` block.
```blocks
let position = -90
basic.forever(function(){
    if(fwdSensors.solar1.fwdLightLevel() > 0){
    }
    else{
    }
})
```
## Step 11
Click right side of the ``||logic:comparison||`` block.
Change ``||0||`` to ``||90||``.
```blocks
let position = -90
basic.forever(function(){
    if(fwdSensors.solar1.fwdLightLevel() > 90){
    }
    else{
    }
})
```
## Step 12 
Click ``||basic:Basic||`` drag and drop ``||basic:show icon||`` block 
inside ``||logic:if true then||`` condition. 
Select ``||basic:target||`` icon.
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 90) {
    basic.showIcon(IconNames.Target)
    } 
    else {}
})
```
## Step 13
Click ``||fwdMotors:Motors||`` drag and drop 
``||fwdMotors:set servo1 off||`` block under 
``||basic:show icon target||`` block. 
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 90) {
    basic.showIcon(IconNames.Target)
    fwdMotors.servo1.fwdSetEnabled(false)
    } 
    else {}
})
```
## Step 14 
Click ``||basic:Basic||`` drag and drop ``||basic:show icon||`` block
inside ``||logic:else||`` condition.
Select ``||basic: small diamond icon||``.
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 90) {
        basic.showIcon(IconNames.Target)
        fwdMotors.servo1.fwdSetEnabled(false)
    } else {
        basic.showIcon(IconNames.SmallDiamond)
        }
})
```
## Step 15
Click ``||Variables:Variables||`` drag and drop 
``||Variables:change position by 1||`` block 
under ``||basic:show icon small diamond||`` block.
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 90) {
        basic.showIcon(IconNames.Target)
        fwdMotors.servo1.fwdSetEnabled(false)
    } else {
        basic.showIcon(IconNames.SmallDiamond)
        position += 1
        }
})
```
## Step 16
Change the value of ``||variables:change position by 1||`` to ``||10||``.
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 90) {
        basic.showIcon(IconNames.Target)
        fwdMotors.servo1.fwdSetEnabled(false)
    } else {
        basic.showIcon(IconNames.SmallDiamond)
        position += 10
        }
})
```
## Step 17
Click ``||logic:Logic||`` drag and drop ``||logic:if true then||``
block under the ``||Variables:change position by 10||`` block. 
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 90) {
        basic.showIcon(IconNames.Target)
        fwdMotors.servo1.fwdSetEnabled(false)
    } else {
        basic.showIcon(IconNames.SmallDiamond)
        position += 10
        if (true) {
            }
        }
})
```
## Step 18
Click ``||logic:Logic||`` drag and drop ``||logic:comparison||`` ``||logic: less than <||``
block to replace ``||logic:true||`` condition of ``||logic: if true then||``
block. Change ``||logic: less than < to greater than >||``.
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 90) {
        basic.showIcon(IconNames.Target)
        fwdMotors.servo1.fwdSetEnabled(false)
    } else {
        basic.showIcon(IconNames.SmallDiamond)
        position += 10
        if (0 > 0) {
                }
        
    }
})
```
## Step 19
Click ``||Variables:Variables||`` drag and drop 
``||Variables:position||`` block on left side of the 
``||logic:comparison||`` block. 
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 90) {
        basic.showIcon(IconNames.Target)
        fwdMotors.servo1.fwdSetEnabled(false)
    } else {
        basic.showIcon(IconNames.SmallDiamond)
        position += 10
        if (position > 0) {
        }
        
    }
})
```
## Step 20
Change ``||0||`` to ``||90||`` on right side of the ``||logic:comparison||``
block. 
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 90) {
        basic.showIcon(IconNames.Target)
        fwdMotors.servo1.fwdSetEnabled(false)
    } else {
        basic.showIcon(IconNames.SmallDiamond)
        position += 10
        if (position > 90) {
        }
        
    }
})
```
## Step 21
Click ``||Variables:Variables||`` drag and drop ``||Variables:set position to 0||`` 
inside ``||logic:if||`` ``||variables:position||`` ``||logic: > 90 then||`` block.
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 90) {
        basic.showIcon(IconNames.Target)
        fwdMotors.servo1.fwdSetEnabled(false)
    } else {
        basic.showIcon(IconNames.SmallDiamond)
        position += 10
        if (position > 90) {
        position = 0
        }
        
    }
})
```

## Step 22
Click ``||fwdMotors:Motors||`` drag and drop ``||fwdMotors:set servo 0 '||``
block under ``||logic:if then||`` condition.
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 90) {
        basic.showIcon(IconNames.Target)
        fwdMotors.servo1.fwdSetEnabled(false)
    } else {
        basic.showIcon(IconNames.SmallDiamond)
        position += 10
        if (position > 90) {
            position = -90
        }
        fwdMotors.servo1.fwdSetAngle(0)
    }
})
```
## Step 23
Click ``||Variables:Variables||`` drag and drop ``||Variables:position||`` block 
to replace ``||0||`` in ``||fwdMotors:set servo 1 to 0 '||`` block.
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 90) {
        basic.showIcon(IconNames.Target)
        fwdMotors.servo1.fwdSetEnabled(false)
    } else {
        basic.showIcon(IconNames.SmallDiamond)
        position += 10
        if (position > 90) {
            position = -90
        }
        fwdMotors.servo1.fwdSetAngle(position)
        }
})
```
## Step 24
Click ``||basic:Basic||`` drag and drop ``||basic:pause||`` block under
``||fwdMotors:set servo1 to||`` ``||Variables:position||`` block. Change
``||basic:(ms) 100||`` to ``||basic:(ms) 20||``.
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 90) {
        basic.showIcon(IconNames.Target)
        fwdMotors.servo1.fwdSetEnabled(false)
    } else {
        basic.showIcon(IconNames.SmallDiamond)
        position += 10
        if (position > 90) {
            position = -90
        }
        fwdMotors.servo1.fwdSetAngle(position)
        basic.pause(20)
    }
})
```
## Step 25
``|Download|``and test your code.
Congratulations on completing your Solar Panel Project! - Go back to the lesson for more activities and extensions. Want to check your code click [here](https://makecode.microbit.org/S90884-23579-70629-38871).
