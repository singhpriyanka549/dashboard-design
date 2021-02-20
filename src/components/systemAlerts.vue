<template>
  <b-container class="background-black">
      <b-row>
          <b-col sm="6"><h6 class="h6-font">System Alerts (Last 5)</h6></b-col>
          <b-col sm="6" style="text-align: right">
        <select class=" drop-down">
          <option selected>All Alerts</option>
        </select>
        
      </b-col><br>
          <b-col sm="12" style="display:inline-flex;padding-bottom:20px" v-for="arr in tempArray" :key="arr">
            <b-col sm="8">
                <span class="span-font" >{{arr.time}}  &nbsp;{{arr.date}}</span><br>
                <h6 class="h6-font" style="margin-top:5px">{{arr.data}}</h6>
            </b-col>
            <b-col sm="4">
                <a class="span-font" style="color: #FFA07A">View Details</a>
            </b-col>
          </b-col>
      </b-row>
  </b-container>
</template>

<script>
export default {
  data () {
    return {
      selected: "Day",
      options: [
          { value: "Day", text: 'Day' },
          { value: 'a', text: 'Week' },
          { value: 'b', text: 'Month' }
        ],
       tempArray:[
           {time: "20:11:35", date:"05 May 2020", data: "New Threat Found"},
           {time: "10:02:13", date:"05 May 2020", data: "Infrastructure Amazon Cloundfront"},
           {time: "15:31:14", date:"05 May 2020", data: "Procex.exe has been Run"},
           {time: "13:16:19", date:"05 May 2020", data: "Configure Audit"}
       ]
    }
  },
  mounted () {
    // Overwriting base render method with actual data.
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.background-black{
    background-color: black;
    color: white;
    padding: 15px;
}
.span-font{
font-size: 10px;
}
.h6-font{
   font-size: 12px; 
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
