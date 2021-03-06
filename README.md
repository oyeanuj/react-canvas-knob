# react-canvas-knob

[jQuery Knob](https://github.com/aterrien/jQuery-Knob) rebuilt with React (no jQuery). This is an HTML5 Canvas-based component that serves as a circular range input. Accepts mouse, touch, scrollwheel, and keyboard input.

## Installation
`npm install react-canvas-knob --save`

## Example usage
Please note that react-canvas-knob must be used as a [controlled input](https://facebook.github.io/react/docs/forms.html#controlled-components).
```js
import React from 'react';
import Knob from 'react-canvas-knob';

class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: 50};
  }
  handleChange = (newValue) => {
    this.setState({value: newValue});
  };
  render() {
    return (
      <Knob
        value={this.state.value}
        onChange={this.handleChange}
      />
    );
  }
}
```

## Properties
| name | description | default |
|------|-------------|---------|
|`value`|numeric value of knob|n/a|
|`onChange`|function to be called on user input|n/a|
|`min`|min value|`0`|
|`max`|max value|`100`|
|`step`|step size|`1`|
|`log`|enable logarithmic scale (must use non-zero `min` and `max`, `step` > 1)|`false`|
|`width` or `height`|dimension of square (px)|`200`|
|`thickness`|gauge thickness|`0.35`|
|`lineCap`|gauge stroke ending style (`butt` or `round`)|`'butt'`|
|`bgColor`|background color|`'#EEE'`|
|`fgColor`|foreground color|`'#EA2'`|
|`inputColor`|text color|`fgColor`|
|`font`|font family|`'Arial'`|
|`fontWeight`|font weight|`'bold'`|
|`clockwise`|direction of progression|`true`|
|`cursor`|use cursor display mode - give width value or `true` which uses the default cursor width (30)|`false`|
|`stopper`|stop at min & max on keydown/mousewheel|`true`|
|`readOnly`|disable all user input|`false`|
|`disableTextInput`|disable manual text input only|`false`|
|`displayInput`|show numeric input box|`true`|
|`angleArc`|arc size in degrees|`360`|
|`angleOffset`|starting angle in degrees|`0`|
|`disableMouseWheel`|disable changes on mouse wheel use|`false`|

## Todo
- [ ] Port `displayPrevious` feature
- [ ] Downwards compatibility
- [ ] Implement some of the existing [pull requests](https://github.com/aterrien/jQuery-Knob/pulls)
- [ ] Improve manual text input
