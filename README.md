[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/rubisc/arup-chart)
# \<arup-chart\>

polymer reusable chart component

## Example:
```
<arup-chart
  type="line"
  title="Sample line chart across x axis"
  subtitle="Monthly average temp"
  y-axis-label="temp in celcius"
  x-axis-categories='["Jan", "Feb", "Mar", "Apr", "May", "June", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"]'
  export-file-name="sample basic line chart"
  series='[{ "name": "Tokyo", "data": [7.0, 6.9, 9.5, 14.5, 18.4, 21.5, 25.2, 26.5, 23.3, 18.3, 13.9, 9.6]}, { "name": "London", "data": [3.9, 4.2, 5.7, 8.5, 11.9, 15.2, 17.0, 16.6, 14.2, 10.3, 6.6, 4.8]}]'>
</arup-chart>
```
Refer to demo directory for more examples

## To use within your polymer app:

```
$ bower install rubisc/arup-chart
```

## Assigning attributes

These are the attributes users must assign:
* __title__ (string)
* __subtitle__ (string)
* __series__: to assign data; see demo for examples of format for setting data for line/pie charts
* __x-axis-label__ (string)
* __y-axis-label__ (string)
* __iterate-across-axis__: for line charts; specify whether chart iterates across the x axis or the y axis (defaults to x)

Additional (optional) attributes users may use to customize charts:
* __y-axis-scale-factor__ (number)
* __x-axis-scale-factor__ (number)

If your chart is iterating across the y axis, x and y labels will be reversed. Make sure to take this into account when assigning attribute values.

## More on Scale Factors

You may adjust data values by a scale factor; that axis will automatically be multiplied by the number you provide.
If you wish to divide by one you must provide the reciprocal of that number.

__y-axis-scaleFactor__: use this to adjust values for pie charts or line charts that iterate across the x axis.  

__x-axis-scaleFactor__: use this only for line charts that iterate across the y axis. Remember that if your chart iterates across the y axis then the x and y axes are swapped, so you will have to assign them accordingly.

__Pie Charts__
Typically, because pie charts display a percentage, we don't care to provide a scale factor because it will not affect the chart.
However, the feature is still enabled in case values do have to change; these values will be reflected in the tooltip when a user hovers over the chart.
