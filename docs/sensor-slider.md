<!--remove-start-->
# Sensor - Slide Potentiometer

Run with:
```bash
node eg/sensor-slider.js
```
<!--remove-end-->

```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {

  var slider = new five.Sensor("A0");

  // "slide" is an alias for "change"
  slider.scale([0, 100]).on("slide", function() {
    console.log("slide", this.value);
  });
});

```


## Breadboard/Illustration


![docs/breadboard/sensor-slider.png](breadboard/sensor-slider.png)
[docs/breadboard/sensor-slider.fzz](breadboard/sensor-slider.fzz)




<!--remove-start-->
## License
Copyright (c) 2012, 2013, 2014 Rick Waldron <waldron.rick@gmail.com>
Licensed under the MIT license.
Copyright (c) 2014, 2015 The Johnny-Five Contributors
Licensed under the MIT license.
<!--remove-end-->
