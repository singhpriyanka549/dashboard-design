<template >
  <b-container class="background-black">
    <b-row>
      <b-col sm="11">
        <topComponentChild
          :heading="head1"
          :generaldata="generalData1"
        ></topComponentChild>
      </b-col>
      <b-col sm="11">
        <topComponentChild
          :heading="head2"
          :generaldata="generalData2"
        ></topComponentChild>
      </b-col>
    </b-row>
  </b-container>
</template>
<script>
import topComponentChild from "./top-component-child";

export default {
  components: {
    topComponentChild,
  },
  data() {
    return {
      selected: "Day",
      options: [
        { value: "Day", text: "Day" },
        { value: "a", text: "Week" },
      ],
      head1: "Policies",
      head2: "NAT Rules",
      generalData1: [
        { name: "General Https", perc: "435%" },
        { name: "General Https", perc: "412%" },
      ],
      generalData2: [
        { name: "General Https", perc: "45k" },
        { name: "General Https", perc: "45k" },
      ],
    };
  },
};
</script>
<style scoped>
.background-black {
  background-color: black;
  color: white;
  padding: 10px;
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
</style>