# Actions on Element

Detox uses **Matchers** to find UI `elements` in your app, **Actions** to emulate user interaction with those `elements` and **Expectations** to verify values on those `elements`.


## Actions
Actions are functions that emulate user behavior. They are being performed on matched elements.

### Methods

- [`.tap()`](#tap)
- [`.longPress()`](#longpress)
- [`.multiTap()`](#multitaptimes)
- [`.typeText()`](#typetexttext)
- [`.replaceText()`](#replacetexttext)
- [`.clearText()`](#cleartext)
- [`.scroll()`](#scrollpixels-direction)
- [`.scrollTo()`](#scrolltoedge)
- [`.swipe()`](#swipedirection-speed)


### `tap()`
Simulate tap on an element.

```js
await element(by.id('tappable')).tap();
```

### `longPress()`
Simulate long press on an element.

```js
await element(by.id('tappable')).longPress();
```

### `multiTap(times)`
Simulate multiple taps on an element.

```js
await element(by.id('tappable')).multiTap(3);
```

### `typeText(text)`
Use the builtin keyboard to type text into a text field.

```js
await element(by.id('textField')).typeText('passcode');
```

### `replaceText(text)`
Paste text into a text field.

```js
await element(by.id('textField')).replaceText('passcode again');
```

### `clearText()`
Clear text from a text field.

```js
await element(by.id('textField')).clearText();
```

### `scroll(pixels, direction)`
Scroll amount of pixels.<br>
pixels - independent device pixels.<br>
direction - left/right/top/bottom

```js
await element(by.id('scrollView')).scroll(100, 'down');
await element(by.id('scrollView')).scroll(100, 'up');
```

### `scrollTo(edge)`
Scroll to edge.

edge - left/right/top/bottom

```js
await element(by.id('scrollView')).scrollTo('bottom');
await element(by.id('scrollView')).scrollTo('top');
```

### `swipe(direction, speed)`

direction - left/right/up/down<br>
speed - fast/slow

```js
await element(by.id('scrollView')).swipe('down', 'fast');
```
