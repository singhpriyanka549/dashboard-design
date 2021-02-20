<template >
  <div>
    <b-row>
      <b-col sm="12">
          <h6 class="h6-font">{{ heading }}</h6></b-col>
      <b-col sm="12">
        <select class="drop-down">
          <option selected>By Sessions</option>
        </select>
      </b-col>
      <b-col sm="12" style="margin-top: 24px">
        <div v-for="(data, index) in generaldata" :key="index" style="margin-bottom: 10px">
          <h5 class="h6-font">{{ data.name }}</h5>
          <b-row>
            <b-col sm="10" style="float: left">
              <b-progress class="progress"></b-progress>
            </b-col>
            <b-col sm="2" style="float: left">
              <span class="h6-font">{{ data.perc }}</span>
            </b-col>
          </b-row>
        </div>
      </b-col>
    </b-row>
  </div>
</template>
<script>
export default {
  props: ["heading", "generaldata"],
  data() {
    return {};
  },
};
</script>
<style scoped>
.drop-down {
  width: 60%;
  height: 20px;
  color: #ffffff73;
  background: #000;
  border-color: #000;
  border-bottom: 1px solid #ced4da;
  font-size: 7px;
}
.h6-font {
  font-size: 10px;
}
.progress {
  height: 2px;
  background-color: #ffb6c1;
}
</style>