<script>
import { Bar } from 'vue-chartjs'
 
export default {
  extends: Bar,
  mounted () {
    // Overwriting base render method with actual data.
    this.renderChart({
      labels: ['', '', '', '', '', '', '', '', '', '', '', '','','','','','','','',''],
      datasets: [
        {
          label: 'GitHub Commits',
          backgroundColor: '#00b9ff',
          data: [40, 20, 12, 39, 20, 40, 39, 60, 40, 20, 12, 11,40, 20, 12, 39, 20, 40, 39, 60]
        }
      ]
    })
  }
}
</script>
<style>
.chartjs-render-monitor{
    height:135px !important
}
</style>