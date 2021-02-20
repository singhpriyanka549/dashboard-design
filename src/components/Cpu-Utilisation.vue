<template>
  <b-container class="background-black">
    <b-row>
      <b-col sm="6"><h6 class="h6-font">CPU Utilisation</h6></b-col>
      <b-col sm="6" style="text-align: right">
        <select class=" drop-down">
          <option selected>Day</option>
        </select>
        
      </b-col>
      <b-col sm="12">
        <chart></chart>
      </b-col>
    </b-row>
    <hr style="border-top: 1px solid #f1f1f152" />
    <b-row>
      <b-col sm="8"><h6 class="h6-font">Sessions</h6></b-col>
      <b-col sm="4">
        <span>213</span><span class="h6-font">/minute</span>
      </b-col>
      <b-col sm="12">
        <line-chart></line-chart>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import chart from "./chart";
import lineChart from "./lineChart";
export default {
  components: { chart, lineChart },
  data() {
    return {
      selected: "Day",
      options: [
        { value: "Day", text: "Day" },
        { value: "a", text: "Week" },
        { value: "b", text: "Month" },
      ],
    };
  },
  mounted() {
    // Overwriting base render method with actual data.
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.background-black {
  background-color: black;
  color: white;
  padding: 10px;
}
.h6-font {
  font-size: 10px;
}
.drop-down {
  width: 60%;
  height: 20px;
  color: #ffffff73;
  background: #000;
  border-color: #000;
  border-bottom: 1px solid #ced4da;
  font-size: 11px;
}
</style>
