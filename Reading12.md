# Chart.js and Canvas

## References

- <cite><https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/></cite>
- <cite><https://www.chartjs.org/docs/latest/></cite>
- <cite><https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage></cite>
- <cite><https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes></cite>
- <cite><https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors></cite>
- <cite><https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text></cite>

## Chart.js API

- Chart.js is a javascript plugin that uses the `<canvas>` element in HTML5 to draw graphs and charts

### Setting Up

- FIRST - download <https://github.com/chartjs/Chart.js> and copy the `Chart.min.js` out of the unzipped folder and into the directory that you'll be working

```html
<!DOCTYPE>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Chart.js Demo</title>
    <script src='chart.min.js'></script>
  </head>
  <body>
  </body>
</html>
```

### Drawing a Line Chart

- First - create the canvas

```html
<canvas id="buyers" width="600" height="400"></canvas>
```

- Then, add a `<script>` to the foot of the body element that will retrieve the context of the canvas

```html
<script>
let buyers = document.getElementById('buyers').getContext('2d');
new Chart(buyers).Line(buyerData);
</script>
```

- Next, add the data needed to create the chart. In this ex. an object is created with the labels for the base of the chart and the dataset
- ***NOTE:*** some options can be passed to the chart via the _Line_ method

```js
var buyerData = {
  labels: ["Jan", "Feb", "Mar", "Apr", "May", "Jun"];
  datasets: [
    {
    fillcolor: "rgba(172, 194, 132, 0.4)",
    strokeColor: "#ACC26D",
    pointColor: "#fff", 
    pointStrokeColor: "#9DB86D",
    data: [203, 156. 99, 251, 305, 247] 
    }
  ]
}
```

### Drawing a Pie Chart and a Bar Chart

```HTML
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Chart.js demo</title>
        <!-- import plugin script -->
        <script src='Chart.min.js'></script>
    </head>
    <body>
        <!-- line chart canvas element -->
        <canvas id="buyers" width="600" height="400"></canvas>
        <!-- pie chart canvas element -->
        <canvas id="countries" width="600" height="400"></canvas>
        <!-- bar chart canvas element -->
        <canvas id="income" width="600" height="400"></canvas>
        <script>
            // line chart data
            var buyerData = {
                labels : ["January","February","March","April","May","June"],
                datasets : [
                {
                    fillColor : "rgba(172,194,132,0.4)",
                    strokeColor : "#ACC26D",
                    pointColor : "#fff",
                    pointStrokeColor : "#9DB86D",
                    data : [203,156,99,251,305,247]
                }
            ]
            }
            // get line chart canvas
            var buyers = document.getElementById('buyers').getContext('2d');
            // draw line chart
            new Chart(buyers).Line(buyerData);
            // pie chart data
            var pieData = [
                {
                    value: 20,
                    color:"#878BB6"
                },
                {
                    value : 40,
                    color : "#4ACAB4"
                },
                {
                    value : 10,
                    color : "#FF8153"
                },
                {
                    value : 30,
                    color : "#FFEA88"
                }
            ];
            // pie chart options
            var pieOptions = {
                 segmentShowStroke : false,
                 animateScale : true
            }
            // get pie chart canvas
            var countries= document.getElementById("countries").getContext("2d");
            // draw pie chart
            new Chart(countries).Pie(pieData, pieOptions);
            // bar chart data
            var barData = {
                labels : ["January","February","March","April","May","June"],
                datasets : [
                    {
                        fillColor : "#48A497",
                        strokeColor : "#48A4D1",
                        data : [456,479,324,569,702,600]
                    },
                    {
                        fillColor : "rgba(73,188,170,0.4)",
                        strokeColor : "rgba(72,174,209,0.4)",
                        data : [364,504,605,400,345,320]
                    }
                ]
            }
            // get bar chart canvas
            var income = document.getElementById("income").getContext("2d");
            // draw bar chart
            new Chart(income).Bar(barData);
        </script>
    </body>
</html>
```

## Chart.js Docs

## Canvas API

### Basic Usage

### Drawing Shapes With Canvas

### Applying Styles And Colors

### Drawing Text