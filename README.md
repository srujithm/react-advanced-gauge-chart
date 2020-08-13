# react-advanced-gauge-chart
React component for displaying a gauge chart, using D3.js

# Usage
Install it by running `npm install react-advanced-gauge-chart`. Then to use it:

```jsx
import GaugeChart from 'react-advanced-gauge-chart'

<GaugeChart id="gauge-chart1" />
```

#### Note: This repo has been cloned and modified from https://github.com/Martin36/react-gauge-chart, please refer and use Martin's original package if you do not need the additional changes.

#### Important: Font Awesome Icon package should be imported (from any of your preferred CDN) in index.html.

## Examples

Check the demo below for complete list of live examples of the charts

#### To create a default chart

```jsx
<GaugeChart id="gauge-chart1" />
```

#### Chart with difference highlighted 

```jsx
<GaugeChart id="gauge-chart2"
  percent={0.86}
  previousValue={0.75}
/>
```

# Demo
https://srujithm.github.io/react-advanced-gauge-chart/

# API

## <GaugeChart />

### Warning: Do not use the same `id` for multiple charts, as it will put multiple charts in the same container

Props from https://github.com/Martin36/react-gauge-chart:

| Name            | PropType                    | Description                                                    | Default value          |
|-----------------|-----------------------------|----------------------------------------------------------------|------------------------|
| id              | PropTypes.string.isRequired | Used for the identification of the div surrounding the chart   |                        |
| className       | PropTypes.string            | Add `className` to the div container                           |                        |
| style           | PropTypes.object            | Add `style` to the div container                               | { width: '100%' }      |
| marginInPercent | PropTypes.number            | Margin for the chart inside the containing SVG element         | 0.05                   |
| cornerRadius    | PropTypes.number            | Corner radius for the elements in the chart                    | 6                      |
| nrOfLevels      | PropTypes.number            | The number of elements displayed in the arc                    | 3                      |
| percent         | PropTypes.number            | The number where the pointer should point to (between 0 and 1) | 0.4                    |
| arcPadding      | PropTypes.number            | The distance between the elements in the arc                   | 0.05                   |
| arcWidth        | PropTypes.number            | The thickness of the arc                                       | 0.2                    |
| colors          | PropTypes.array             | An array of colors in HEX format displayed in the arc          | ["#00FF00", "#FF0000"] |
| textColor       | PropTypes.string            | The color of the text                                          | "#FFFFFF"              |
| needleColor     | PropTypes.string            | The color of the needle triangle                               | "#464A4F"              |
| needleBaseColor | PropTypes.string            | The color of the circle at the base of the needle              | "#464A4F"              |
| hideText        | PropTypes.bool              | Whether or not to hide the percentage display                  | false                  |
| arcsLength      | PropTypes.array             | An array specifying the lenght of the each individual arc. If this prop is then the nrOfLevels prop will have no effect      | none                   |
| animate         | PropTypes.bool              | Whether or not to animate the needle when loaded               | true                   |
| animDelay       | PropTypes.number            | Delay in ms before start the needle animation                  | 500                    |
| formatTextValue | PropTypes.func              | Format you own text value (example: value => value+'%')        | null                   |

Newly introduced props for the chart:

| Name            | PropType                    | Description                                                    | Default value          |
|-----------------|-----------------------------|----------------------------------------------------------------|------------------------|
| previousValue   | PropTypes.number | The number to compare current percentage with (between 0 and 1)   |                        |
