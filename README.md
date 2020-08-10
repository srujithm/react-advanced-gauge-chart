# react-advanced-gauge-chart
React component for displaying a gauge chart, using D3.js

# Usage
Install it by running `npm install react-advanced-gauge-chart`. Then to use it:

```jsx
import GaugeChart from 'react-gauge-chart'

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

#### Note: Please refer to https://github.com/Martin36/react-gauge-chart to get complete list of props. Only new props are being highlighted here.

The props for the chart:

| Name            | PropType                    | Description                                                    | Default value          |
|-----------------|-----------------------------|----------------------------------------------------------------|------------------------|
| previousValue   | PropTypes.number | The number to compare current percentage with (between 0 and 1)   |                        |
