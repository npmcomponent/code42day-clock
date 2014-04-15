*This repository is a mirror of the [component](http://component.io) module [code42day/clock](http://github.com/code42day/clock). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/code42day-clock`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# clock

  Clock UI component for use in time-picker

  ![Clock](https://gist.github.com/pirxpilot/5011178/raw/9da0b4c2194444a6a3965d71adaf2b8c59f1faba/preview.png)

  Click [here](http://code42day.github.io/clock/) to see online demo.

## Installation

    $ component install code42day/clock

## Example

```js
var Clock = require('clock');
var clock = new Clock;
clock.el.appendTo('body');
clock.select({
	hour: 11,
	minute: 30
});
```

## Events

  - `change` (time, complete) - when the selected time is modified
  	`time` is an object with `hour` and `minute` properties,
  	`complete` is true only if both hours and minutes have been clicked by the user

## API

### Clock#select(time)

Select the given `time` ({ hour, minute }).

### Clock#min(minTime)

Define the minimum time selectable with this clock (inclusive). Time values smaller than `minTime`
are rendered with `invalid` class. All `change` events are generated only for values larger or equal
to `minTime`.

### Clock#max(maxTime)

Define the maximum time selectable with this clock (inclusive). Time values larger than `maxTime`
are rendered with `invalid` class. All `change` events are generated only for values smaller or equal
to `maxTime`.

## License

  MIT
