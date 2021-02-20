<script>
import { Doughnut } from 'vue-chartjs'
 
export default {
  extends: Doughnut,
  mounted () {
    this.renderChart({
      datasets: [
        {
          backgroundColor: [
            '#00ffff',
            '#00ffbf',
            '#bf00ff',
            '#00ff80',
            '#000000'
          ],
          data: [45, 16, 13, 11, 5]
        }
      ]
    }, {responsive: true, maintainAspectRatio: false})
  }
}
</script>