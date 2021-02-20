<template>
  <div>
      <b-container fluid style="background-color:#000000c9">
          <b-row>
              <header-component/>
          </b-row>
          <b-row class="top-row">
              <b-col sm="3">
                  <cpu-utilisation/>
              </b-col>
              <b-col sm="2">
                  <application-risk/>
              </b-col>
              <b-col sm="4">
                  <top-application/>
              </b-col>
              <b-col sm="3">
                  <system-alerts/>
              </b-col>
          </b-row>
          <b-row class="bottom-row">
            <b-col sm="2">
                  <bottom-application/>
              </b-col>
              <b-col sm="2">
                  <insights/>
              </b-col>
              <b-col sm="2">
                  <observed-thread/>
              </b-col>
              <b-col sm="2">
                  <CaptureATP/>
              </b-col>
              <b-col sm="4">
                  <bottom-top-app/>
              </b-col>
          </b-row>
      </b-container>
     
     
  </div>
</template>

<script>
import ApplicationRisk from './ApplicationRisk.vue'
import BottomApplication from './Bottom-application.vue'
import BottomTopApp from './Bottom-top-app.vue'
import CaptureATP from './Capture-ATP.vue'
import CpuUtilisation from './Cpu-Utilisation.vue'
import HeaderComponent from "./Header"
import Insights from './Insights.vue'
import ObservedThread from './Observed-Thread.vue'
import SystemAlerts from './systemAlerts.vue'
import TopApplication from './Top-application.vue'
import topComponentChild from './top-component-child';
export default {
  components: { CpuUtilisation, HeaderComponent, ApplicationRisk, TopApplication, SystemAlerts,topComponentChild, BottomApplication, ObservedThread, BottomTopApp, Insights, CaptureATP  },
      data () {
    return {
     
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.top-row{
    margin-top: 10px;
}
.bottom-row{
    margin-top: 20px;
}
</style>
