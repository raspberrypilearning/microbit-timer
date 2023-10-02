There may be times when you need to time something.

You could show a timer on the LEDs.

```microbit
input.onGesture(Gesture.Shake, function () {
    for (let second = 0; second <= 4; second++) {
        basic.showNumber(second + 1)
        basic.pause(1000)
    }
    basic.showIcon(IconNames.EighthNote)
    basic.clearScreen()
})
```

In this code:

The `second`{:class='microbitvariables'} variable takes on each value from `0` to the end number (`4` in our example) and counts up by one each time.

The value of the `second`{:class='microbitvariables'} variable is added to `1` and displayed on the LEDs for one second (the length of time set in the `pause`{:class='microbitbasic'} block).

After the last number (`5`) is displayed, the `show icon`{:class='microbitbasic'} block is used to show a musical note and then the LEDs are turned off using `clear screen`{:class='microbitbasic'} block.


The example shows the timer starting when the micro:bit is shaken, but you can set it to happen on other events, for example when a button is pressed. You could also put it in a function if you want to call it from different places in your code.

### Change the timer length

You can change the timer length by altering the second number in the `for`{:class='microbitloops'} block. Set it to one less than the number you want to end on (remember the `+`{:class='microbitmath'} block is used)

### Countdown, not count up

To create a countdown, you will need to delete the value of the `second`{:class='microbitvariables'} variable from the end number (`4` in this example) plus one (so `5` in this example).

Here is how you would change the code.

```microbit
input.onGesture(Gesture.Shake, function () {
    for (let second = 0; second <= 4; second++) {
        basic.showNumber(5 - second)
        basic.pause(1000)
    }
    basic.showIcon(IconNames.EighthNote)
    basic.clearScreen()
})
```