# googleCharts
googleCharts

https://developers.google.com/chart/interactive/docs/gallery

1 Visualization: Area Chart

    <html>
      <head>
        <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
        <script type="text/javascript">
          google.charts.load('current', {'packages':['corechart']});
          google.charts.setOnLoadCallback(drawChart);

          function drawChart() {
            var data = google.visualization.arrayToDataTable([
              ['Year', 'Sales', 'Expenses'],
              ['2013',  1000,      400],
              ['2014',  1170,      460],
              ['2015',  660,       1120],
              ['2016',  1030,      540]
            ]);

            var options = {
              title: 'Company Performance',
              hAxis: {title: 'Year',  titleTextStyle: {color: '#333'}},
              vAxis: {minValue: 0}
            };

            var chart = new google.visualization.AreaChart(document.getElementById('chart_div'));
            chart.draw(data, options);
          }
        </script>
      </head>
      <body>
        <div id="chart_div" style="width: 100%; height: 500px;"></div>
      </body>
    </html>
    

2 Bar Charts

    <html>
      <head>
        <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
        <script type="text/javascript">
          google.charts.load('current', {'packages':['bar']});
          google.charts.setOnLoadCallback(drawChart);

          function drawChart() {
            var data = google.visualization.arrayToDataTable([
              ['Year', 'Sales', 'Expenses', 'Profit'],
              ['2014', 1000, 400, 200],
              ['2015', 1170, 460, 250],
              ['2016', 660, 1120, 300],
              ['2017', 1030, 540, 350]
            ]);

            var options = {
              chart: {
                title: 'Company Performance',
                subtitle: 'Sales, Expenses, and Profit: 2014-2017',
              },
              bars: 'horizontal' // Required for Material Bar Charts.
            };

            var chart = new google.charts.Bar(document.getElementById('barchart_material'));

            chart.draw(data, google.charts.Bar.convertOptions(options));
          }
        </script>
      </head>
      <body>
        <div id="barchart_material" style="width: 900px; height: 500px;"></div>
      </body>
    </html>
    
    
  3 columnchart_material
  
      <html>
      <head>
        <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
        <script type="text/javascript">
          google.charts.load('current', {'packages':['bar']});
          google.charts.setOnLoadCallback(drawChart);

          function drawChart() {
            var data = google.visualization.arrayToDataTable([
              ['Year', 'Sales', 'Expenses', 'Profit'],
              ['2014', 1000, 400, 200],
              ['2015', 1170, 460, 250],
              ['2016', 660, 1120, 300],
              ['2017', 1030, 540, 350]
            ]);

            var options = {
              chart: {
                title: 'Company Performance',
                subtitle: 'Sales, Expenses, and Profit: 2014-2017',
              }
            };

            var chart = new google.charts.Bar(document.getElementById('columnchart_material'));

            chart.draw(data, google.charts.Bar.convertOptions(options));
          }
        </script>
      </head>
      <body>
        <div id="columnchart_material" style="width: 800px; height: 500px;"></div>
      </body>
    </html>

