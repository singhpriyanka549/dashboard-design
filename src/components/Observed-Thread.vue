<template>
  <b-container class="background-black">
      <b-row>
          <b-col sm="12"><h6 class="h6-font">Observed Thread</h6></b-col>
          <b-col sm="12" v-for="arr in tempArray" :key="arr">
              <span class="h6-font">{{arr.temp}}   &nbsp; &nbsp;{{arr.data}}</span>
              <hr style="border-top: 1px solid #f1f1f152;margin-bottom: 15px;" />
          </b-col>
      </b-row>
  </b-container>
</template>

<script>
export default {
  data () {
    return {
      tempArray:[
           {temp: "11400", data: "IPS"},
           {temp: "7456", data: "BotNet"},
           {temp: "3980", data: "Gv/AS"},
           {temp: "5539", data: "SandBox"},
           {temp: "3901", data: "App Risk"},
           {temp: "5", data: "Vulnerabilities"},
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
    padding: 8px 10px 0px 10px;
}
.h6-font{
font-size: 12px;
}

</style>
