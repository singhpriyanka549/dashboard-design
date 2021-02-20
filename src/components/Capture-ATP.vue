<template>
  <b-container class="background-black">
    <b-row>
      <b-col sm="6"><h6 class="h6-font">Capture ATP</h6></b-col>
      <b-col sm="6">
        <select class=" drop-down">
          <option selected>Week</option>
        </select>
      </b-col>
      <b-col sm="12" class="bottom-capture"  v-for="arr in tempArray" :key="arr">
       <span class="h6-font"><b-icon icon="exclamation-circle"></b-icon> &nbsp; &nbsp;{{arr.temp}}</span>
       <span class="h6-font">{{arr.data}}</span>
      </b-col>
    </b-row>
    <hr style="border-top: 1px solid #f1f1f152" />
    <b-row>
      <b-col sm="6"><h6 class="h6-font">Verdict (Files)</h6></b-col>
      <b-col sm="12">
        <chart></chart>
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
      tempArray:[
           {temp: "2%", data: "Malicious File"},
           {temp: "856", data: "Total File Submitted"},
           {temp: "46", data: "Total file Corupted"},
           {temp: "63", data: "Dynamic Analytics"},
           {temp: "2.3 sec", data: "Avg processing time"}
       ]
    };
  }
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
  font-size: 6px;
}
.bottom-capture{
    margin-bottom: 3px;
}
</style>
