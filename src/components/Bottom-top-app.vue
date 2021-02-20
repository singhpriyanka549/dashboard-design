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
            head1: "Top Viruses",
            head2: "Top Intrusions",
            head3: "Top Botnets",
            generalData1:[
                {name: 'Trojun Horse', perc: '43'},
                {name: 'Power Worm', perc: '41'},
                {name: 'Mydroom', perc: '45'},
                {name: 'StormWarm', perc: '34'},
                {name: 'Brain', perc: '20'}
            ],
              generalData2:[
                {name: 'EchoReply', perc: '9.14k'},
                {name: 'SSLv2.0...Hello2', perc: '130'},
                {name: 'OpenVPN...closure', perc: '6'},
                {name: 'DNSquery...com', perc: '1'},
                {name: '1.0.345.6', perc: '1'}
            ],
              generalData3:[
                {name: '98.124.167.228', perc: '45GB'},
                {name: '198.268.2.345', perc: '24GB'},
                {name: '75.57.812.09', perc: '21GB'},
                {name: '1.0.0678', perc: '12GB'},
                {name: '87.13.187.01', perc: '9GB'}
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