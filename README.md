# \<arup-chart\>

reusable chart component

## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your element locally.

## Viewing Your Element

```
$ polymer serve
```

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.

(Rough notes to polish)

## Assigning attributes

If your chart is iterating across the y axis, x and y labels will be reversed. Make sure to take this into account when assigning attribute values.

### Scale Factors

You may adjust data values by a scale factor; that axis will automatically be multiplied by the number you provide.
Note that it will always be multiplied by this number, and so if you wish to divide by one you must provide the reciprocal of that number.

__y-axis-scaleFactor__: use this to adjust values for pie charts or line charts that iterate across the x axis.
__x-axis-scaleFactor__: use this only for line charts that iterate across the y axis. Remember that if your chart iterates across the y axis then the x and y axes are swapped, so you will have to assign them accordingly.

__Pie Charts__
Typically, because pie charts display a percentage, we don't care to provide a scale factor because it will not affect the chart.
However, the feature is still enabled in case values do have to change; these values will be displayed in the tooltip when a user hovers over the chart.
