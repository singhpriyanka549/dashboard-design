<template>
  <b-container class="background-black">
      <b-row style="margin-top = 10px">
          <b-col sm="12"><h6 class="h6-font">Insights</h6></b-col>
          <b-col sm="12" class="bottom-prop" v-for="arr in tempArray" :key="arr">
              <span style="color:red"> <b-icon icon="exclamation-circle-fill" variant="danger"></b-icon>  &nbsp; &nbsp;{{arr.temp}}</span><br>
              <span class="h6-font h6-span">{{arr.data}}</span>
              <hr style="border-top: 1px solid #f1f1f152" />
          </b-col>
      </b-row>
  </b-container>
</template>

<script>
export default {
  data () {
    return {
      tempArray:[
           {temp: "2", data: "Infected Hosts"},
           {temp: "43", data: "Critical Alerts"},
           {temp: "22%", data: "Incrypted Traffic"}
       ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.background-black{
    background-color: black;
    color: white;
    padding: 10px;
}
.h6-font{
font-size: 12px;
}
.h6-span{
    margin-left: 25px;
}
.bottom-prop{
  padding-top: 13px;
  padding-bottom: 14px;
}
</style>
