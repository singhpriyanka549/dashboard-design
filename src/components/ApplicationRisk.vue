<template>
  <b-container class="background-black">
    <b-row>
      <b-col sm="12"><h6 class="h6-font">Application Risk Level</h6></b-col>
      <b-col sm="12">
        <chart></chart>
        <br>
        <ul class="ul-line">
            <li class="h6-font-ul">45% &nbsp;&nbsp;<span class="h6-font-ul">General HTTPS</span></li>
            <li class="h6-font-ul">16% &nbsp;&nbsp;<span class="h6-font-ul">General UDP</span></li>
            <li class="h6-font-ul">13% &nbsp;&nbsp;<span class="h6-font-ul">General DNS</span></li>
            <li class="h6-font-ul">11% &nbsp;&nbsp;<span class="h6-font-ul">General DNS</span></li>
            <li class="h6-font-ul">5% &nbsp;&nbsp;<span class="h6-font-ul">Other</span></li>
        </ul>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import chart from "./pie-chart";
export default {
  components: { chart },
  data() {
    return {
      selected: "Day",
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
.h6-font-ul {
  font-size: 14px;
  margin-bottom: 13px;
}
.drop-down {
  display: inline-block;
  width: 100%;
  height: 20px;
  padding: 0.375rem 1.75rem 0.375rem 0.75rem;
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.5;
  color: #fff;
  vertical-align: middle;
  background: #000;
  border-color: #000;
  border-bottom: 1px solid #ced4da;
  border-radius: 0.25rem;
  appearance: none;
}
.ul-line{
    padding-inline-start: 10px;
}
</style>
