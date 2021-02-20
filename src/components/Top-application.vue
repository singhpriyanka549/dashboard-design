<template >
    <b-container class="background-black">
        <b-row>
       <b-col sm="4">
           <topComponentChild :heading="head1" :generaldata="generalData1"></topComponentChild>
       </b-col>
       <b-col sm="4">
           <topComponentChild :heading="head2" :generaldata="generalData2"></topComponentChild>
       </b-col>
       <b-col sm="4">
           <topComponentChild :heading="head3" :generaldata="generalData3"></topComponentChild>
       </b-col>
        </b-row>
    </b-container>
</template>
<script>
import topComponentChild from './top-component-child';
export default {
    components:{
        topComponentChild
    },
    data(){
        return{
            head1: "Top Application",
            head2: "Top Addresses",
            head3: "Top Users",
            generalData1:[
                {name: 'General Https', perc: '435%'},
                {name: 'General Https', perc: '412%'},
                {name: 'General Https', perc: '353%'},
                {name: 'General Https', perc: '341%'},
                {name: 'General Https', perc: '204%'}
            ],
              generalData2:[
                {name: '75.75.812.09', perc: '45k'},
                {name: '98.234.167.228', perc: '45k'},
                {name: '87.13.187.01', perc: '45k'},
                {name: '198.268.2.346', perc: '45k'},
                {name: '1.0.345.6', perc: '45k'}
            ],
              generalData3:[
                {name: 'Admin', perc: '45GB'},
                {name: 'Admin2', perc: '41GB'},
                {name: 'Unknown', perc: '24GB'},
                {name: 'Supervisor', perc: '18GB'},
                {name: 'Unknown', perc: '45k'}
            ]
        }
    }
}
</script>
<style scoped>
.background-black {
  background-color: black;
  color: white;
  padding: 10px;
}

</style>