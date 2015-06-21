---
title: "How it works"
bg: blue
color: white
style: left
---

# How it works
Light a LED on an Arduino board without code.
```html
<web-arduino id="arduino" device-name="DEVICE">
  <pin index="7" mode="OUTPUT" value="HIGH"></pin>
</web-arduino>
```

Blink the above LED.
```js
var arduino = document.querySelector('#arduino');
arduino.addEventListener('connected', function() {
  setInterval(function() {
    arduino.d7 = !arduino.d7;
  }, 300);
});
```
