<template>
  <div>
    <div class = 'chart'>
      <!-- import font awesome for legend icons -->
      <link href = 'https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css' rel = 'stylesheet' integrity = 'sha384-wvfXpqpZZVQGK6TAh5PVlGOfQNHSoD2xbE+QkPxCAFlNEevoEH3Sl0sibVcOQVnN' crossorigin = 'anonymous'>
      <chart-axis :data = 'chartData'></chart-axis>
    </div>

    <pre class="language-html"><code>
&lt;template&gt;
  &lt;div class='chart'&gt;
    &lt;!-- import font awesome for legend icons --&gt;
    &lt;link href='https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css' rel='stylesheet'&gt;
    &lt;chart-axis :data='chartData'&gt;&lt;/chart-axis&gt;
  &lt;/div&gt;
&lt;/template&gt;

&lt;script&gt;
  import { svgArea, svgLine, svgScatter } from 'd2b'
  import { ChartAxis } from 'vue-d2b'

  export default {
    data () {
      return {
        chartData: {
          sets: [
            {
              generators: [svgArea(), svgLine(), svgScatter()],
              graphs: [
                {
                  label: 'area 1',
                  values: [
                    {x: 1, y: 25},
                    {x: 2, y: 38},
                    {x: 3, y: 24},
                    {x: 4, y: 60},
                    {x: 5, y: 22}
                  ]
                },
                {
                  label: 'area 2',
                  values: [
                    {x: 1, y: 15},
                    {x: 2, y: 8},
                    {x: 3, y: 54},
                    {x: 4, y: 22},
                    {x: 5, y: 20}
                  ]
                }
              ]
            }
          ]
        }
      }
    },

    components: {
      ChartAxis
    }
  }
&lt;/script&gt;

&lt;style scoped&gt;
  .chart{
    width: 100%;
    height: 500px;
  }
&lt;/style&gt;</code></pre>
  </div>
</template>

<script>
  import { svgArea, svgLine, svgScatter } from 'd2b'
  import { ChartAxis } from '../src/'

  export default {
    data () {
      return {
        chartData: {
          sets: [
            {
              generators: [svgArea(), svgLine(), svgScatter()],
              graphs: [
                {
                  label: 'area 1',
                  values: [
                    {x: 1, y: 25},
                    {x: 2, y: 38},
                    {x: 3, y: 24},
                    {x: 4, y: 60},
                    {x: 5, y: 22}
                  ]
                },
                {
                  label: 'area 2',
                  values: [
                    {x: 1, y: 15},
                    {x: 2, y: 8},
                    {x: 3, y: 54},
                    {x: 4, y: 22},
                    {x: 5, y: 20}
                  ]
                }
              ]
            }
          ]
        }
      }
    },

    components: {
      ChartAxis
    }
  }
</script>

<style scoped>
  .chart{
    height: 100vh;
    max-height: 500px;
    margin-top: 40px;
  }
</style>
