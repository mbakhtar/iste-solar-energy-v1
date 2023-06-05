# Solar Panel
```package
fwd-edu-breakout=github:climate-action-kits/pxt-fwd-edu/fwd-breakout
solar=github:climate-action-kits/pxt-fwd-edu
```
## Step 1 @showdialog
Plug your USB cable into the micro:bit and insert it into the 
Climate Action Kit board. Click on the button to the right of 
download and follow the steps to pair your micro:bit.
![pair microbit](https://github.com/mbakhtar/iste-solar-energy-v1/assets/109742973/d2cd404c-58e7-4462-ae22-8859cc74273e)
![breakout image](https://raw.githubusercontent.com/mbakhtar/wind-turbine-lesson-tutorial/master/breakout-resized.png)

## Step 2 
Create a ``||Variables:Variable||`` called ``||Variables:position||``
and nest ``||Variables:set position to -90||`` 
under ``||basic:on start||`` block.
Now nest an ``||logic:If true then else||`` 
block under the ``||basic:forever||`` loop.
```blocks
let position = -90
basic.forever(function(){
    if(true){
    }
    else{
    }
})
```
## Step 3 
Add a ``||logic:comparison block||`` from the 
``||logic:Logic drawer||``. Place it in the true
condition of the ``||logic: if then else||`` loop.
Insert the block ``||fwdSensors:solar1 light level %||`` on the left side
and insert ``||75||`` on the right side of the ``||logic:comparison block||``.
```blocks
let position = -90
basic.forever(function(){
    if(fwdSensors.solar1.fwdLightLevel() > 75){
    }
    else{
    }
})
```
## Step 4 
Under the true condition, add the ``||basic:show icon||`` block and select the ``||basic:target||``icon.
To stop the ``||Solar Array||`` from scanning 
for the sunlight, go to ``||fwdMotors:set servo1 off||``. 
This indicates the ``||Solar Array||`` 
is facing the sun and receiving maximum light.
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 75) {
    basic.showIcon(IconNames.Target)
    fwdMotors.servo1.fwdSetEnabled(false)
    } 
    else {}
})
```
## Step 5 
If the condition is false, add ``||basic:show icon||`` block under the 
``||logic:else||`` and select ``||basic: small diamond icon||``.
Add the ``||Variables:change position by 10||`` block under this icon.
Add the``||logic:if true then||`` block under the 
``||logic:else||`` condition below the 
``||Variables:change position by 10||``.
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 75) {
        basic.showIcon(IconNames.Target)
        fwdMotors.servo1.fwdSetEnabled(false)
    } else {
        basic.showIcon(IconNames.SmallDiamond)
        position += 10
        if () {
            }
        }
})
```
## Step 6 
For the true condition, replace it by a ``||logic:comparison||`` block.
For the comparison, add ``||Variables:position||`` on the left side and 
add ``||90||``to the right side.
For the true condition, add ``||Variables:set position to -90||`` 
nested under the ``||logic:if position>90 then||``.
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 75) {
        basic.showIcon(IconNames.Target)
        fwdMotors.servo1.fwdSetEnabled(false)
    } else {
        basic.showIcon(IconNames.SmallDiamond)
        position += 10
        if (position > 90) {
            position = -90
        }
        
    }
})
```

## Step 7 
Add ``||fwdMotors: set servo1 angle to||`` block and add the 
``||Variables:position||`` block into it. This is placed
after the ``||logic:if then||`` block.
Add a ``||basic:pause||`` block and set it to ``||basic:20ms||``.
Congratulations on completing your Solar Panel Project! - Go back to the lesson for more activities and extensions.
```blocks
let position = -90
basic.forever(function () {
    if (fwdSensors.solar1.fwdLightLevel() > 75) {
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
