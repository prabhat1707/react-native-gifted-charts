# react-native-gifted-charts [![Rate on Openbase](https://badges.openbase.com/js/rating/react-native-gifted-charts.svg)](https://openbase.com/js/react-native-gifted-charts?utm_source=embedded&utm_medium=badge&utm_campaign=rate-badge)

The most complete library for Bar, Line, Area, Pie, Donut and Stacked Bar charts in React Native. Allows 2D, 3D, gradient, animations and live data updates.

### Yet another chart library? Why?

**_To bring Life to your data_**

1. Plenty of features with minimal code
2. Apply animations to your charts on load and on value change, just by adding a prop
3. Smooth animations implemented using LayoutAnimation
4. Clickable and scrollable
5. Three-D and gradient effects
6. Fully customizable (see the [props](docs/docs.md))
7. Detailed [documentation](https://gifted-charts.web.app/) with examples
8. Support for **_combined_** Bar and Line charts

---

![alt text](/demos/altBars.svg)
![alt text](/demos/barPairs.svg)
<img src='/demos/animatedDataLine.gif' alt='' width=300/>
<img src='/demos/pielabbelled.svg' alt='' height=280 width=270/>
<img src='/demos/movingBars.gif' alt='' width=300/>
<img src='/demos/stacks.png' alt='' height=360 width=320/>
![alt text](/demos/lineArea.png)
<img src='/demos/cappedCombined.png' alt='' height=280 width=280/>
<img src='/demos/line.gif' alt='' height=300 width=290/>

---

## Installation

```sh
npm install react-native-gifted-charts react-native-linear-gradient react-native-svg
```

For Pie chart and Donut chart, these additional packages should be installed-

```sh
npm i react-native-canvas react-native-webview
```

For iOS-

```sh
cd ios && pod install
```

# Docs

[Documentation and gallery](https://gifted-charts.web.app/)

## Usage

The simplest usage of various types of charts can be done as below-

```js
import { BarChart, LineChart, PieChart } from "react-native-gifted-charts";

// ...
const data=[ {value:50}, {value:80}, {value:90}, {value:70} ]

<BarChart data = {data} />
<LineChart data = {data} />
<PieChart data = {data} />

// For Horizontal Bar chart, just add the prop horizontal to the <BarChart/> component

<BarChart data = {data} horizontal />

// For Area chart, just add the prop areaChart to the <LineChart/> component

<LineChart data = {data} areaChart />

// For Donut chart, just add the prop donut to the <PieChart/> component

<PieChart data = {data} donut />
```

## Props tables

**[1. BarChart, Horizontal BarChart and Stacked Bar Chart props](docs/BarChart/BarChartProps.md)** \
**[2. LineChart and AreaChart props](docs/LineChart/LineChartProps.md)** \
**[3. PieChart and DonutChart props](docs/PieChart/PieChartProps.md)**

## Contributing

_Dear developers_! Your small contribution can make someone's day 😊

One of the ways you can contribute is to address an [open issue](https://github.com/Abhinandan-Kushwaha/react-native-gifted-charts/issues).

Sometimes people report issues which don't exist, or request for features which are already present. Such issues can be addressed without pushing any code to the repo. Just show them in the comments how to do it.

See the [contributing guide](CONTRIBUTING.md) to learn how to contribute to the repository and the development workflow.

## Common issues

| Issue                                                                                                                        | Solution                                                                                                                                                                    |
| ---------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [BarChart - Value and section line don't match](https://github.com/Abhinandan-Kushwaha/react-native-gifted-charts/issues/35) | [Comment by the owner](https://github.com/Abhinandan-Kushwaha/react-native-gifted-charts/issues/35#issuecomment-972673281)                                                  |
| **Invariant Violation: requireNativeComponent: "RNCWebView" was not found in the UIManager.**                                | install `react-native-webview`                                                                                                                                              |
| Setting `height`, `maxValue`, `stepValue`, `stepHeight`, or `noOfSections` breaks the chart                                  | Please make sure that<br/> `maxValue = noOfSections * stepValue;` <br/>is followed. [See this](https://github.com/Abhinandan-Kushwaha/react-native-gifted-charts/issues/71) |

## To-dos

[To do list](./src/todos.md)

## License

MIT
