<script>
import { Line } from 'vue-chartjs'
 
export default {
  extends: Line,
  mounted () {
    this.renderChart({
      labels: ['', '', '', '', '', '', '','','','','',''],
      datasets: [
        {
          label: 'Data One',
          backgroundColor: '#f87979',
          data: [40, 39, 38, 40, 39, 60, 40,40,40,40,40,40]
        }
      ]
    }, {responsive: true, maintainAspectRatio: true})
  }
}
</script>