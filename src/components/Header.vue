<template>
<b-container fluid class="header">
  <b-row>
    <b-col sm="10">
      <b-icon icon="dash-circle-fill" aria-hidden="true" variant="warning"></b-icon>
      <span class="dashboard">DASHBOARD</span>
    </b-col>
      <b-col sm="2" class="right-header">
        <b-icon icon="search" aria-hidden="true" class="white-icon"></b-icon>
        <b-icon icon="alarm" aria-hidden="true" class="white-icon"></b-icon>
        <b-icon icon="award-fill" aria-hidden="true" class="white-icon"></b-icon>
        <avatar username="A Doe" class="avatar"></avatar>
      </b-col>
  </b-row>
</b-container>
</template>

<script>
import Avatar from 'vue-avatar'
export default {
  data () {
    return {
      
    }
  },
   components: {
    Avatar
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >
.header{
  height: 26px;
  background-color: black;
}
.dashboard{
color: white;
}
.white-icon{
color: white;
}
.avatar{
  display: flex;
    width: 22px !important; 
    height: 22px !important;
    border-radius: 50%;
    font: 11px / 26px Helvetica, Arial, sans-serif !important;
    align-items: center;
    justify-content: center;
    text-align: center;
    user-select: none;
    background-color: #ffffff !important;
    color: rgb(0 0 0) !important;
}
.right-header{
  display: inline-flex;
  text-align: right;
}
.right-header svg , .right-header div{
  margin-left: 10px;
  margin-top: 3px;
}
</style>
