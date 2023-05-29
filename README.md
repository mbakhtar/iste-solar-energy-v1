# Solar Energy - The Solar Savvy Adventure
```package
fwd-edu-breakout=github:climate-action-kits/pxt-fwd-edu/fwd-breakout
solar=github:climate-action-kits/pxt-fwd-edu
```
## Step 1 
Plug your USB cable into the micro:bit and insert it into the 
Climate Action Kit board. Click on the button to the right of 
download and follow the steps to pair your micro:bit.

## Step 2 
Create a ``||Variables:Variable position||`` 
and nest ``||Variables:set position to -90||`` 
under ``||basic:on start||`` block
Now nest an ``||logic:If true then else||`` 
block under the ``||basic:forever||`` loop
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
``||logic:Logic drawer||`` place it in the true
condition of the ``||logic: if then else||`` loop
Insert the block ``||fwdSensors:solar1 light level %||`` on the left side
and insert ``||75||`` on the right side of the ``||logic:comparison block||``
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
If the condition is true add ``||basic:show icon||`` block and 
select ``||basic:target icon||``. 
To stop the ``||Solar Array||`` from scanning 
for the sunlight, go to ``||fwdMotors:set servo1 off||``. 
This indicates the ``||Solar Array||`` 
is facing the sun and receiving maximum light
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
If the condition is false add ``||basic:show icon||`` block under the 
``||logic:else||`` and select ``||basic: small diamond icon||``.
Now add ``||Variables:change position by 10||`` block under 
the ``||basic:small diamond icon||``
Add ``||logic:if true then||`` block under the 
``||logic:else||`` condition below the 
``||Variables:change position by 10||``
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
For the true condition replace it by a ``||logic:comparison||`` block
For the comparison add ``||Variables:position||`` on the left side and 
compare with ``||90||``
For the true condition add ``||Variables:set position to -90||`` 
nested under the ``||logic:if position>90 then||``
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
Add ``||fwdMotors: set servo1 angle to||`` block and insert 
``||Variables:position||`` block in it. This is placed
after the ``||logic:if then||`` block 
Also add a ``||basic:pause||`` block and set it to ``||basic:20ms||``
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
## Step 8 
This is the final code
```blocks
let position = -90
fwdMotors.servo1.fwdSetEnabled(false)
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
Congratulations, you did it!


> Open this page at [https://mbakhtar.github.io/iste-solar-energy-v1/](https://mbakhtar.github.io/iste-solar-energy-v1/)

## Use as Extension

This repository can be added as an **extension** in MakeCode.

* open [https://makecode.microbit.org/](https://makecode.microbit.org/)
* click on **New Project**
* click on **Extensions** under the gearwheel menu
* search for **https://github.com/mbakhtar/iste-solar-energy-v1** and import

## Edit this project ![Build status badge](https://github.com/mbakhtar/iste-solar-energy-v1/workflows/MakeCode/badge.svg)

To edit this repository in MakeCode.

* open [https://makecode.microbit.org/](https://makecode.microbit.org/)
* click on **Import** then click on **Import URL**
* paste **https://github.com/mbakhtar/iste-solar-energy-v1** and click import

## Blocks preview

This image shows the blocks code from the last commit in master.
This image may take a few minutes to refresh.

![A rendered view of the blocks](https://github.com/mbakhtar/iste-solar-energy-v1/raw/master/.github/makecode/blocks.png)

#### Metadata (used for search, rendering)

* for PXT/microbit
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
