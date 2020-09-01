<template>
  <div class="table-page-padding">
      <h1>{{pdp.title}}</h1>
    <b-table
      :bordered=true
      :outlined=true
      :hover=true
      :items="pdp.goals"
      :fields="headings"
      thead-class="thead-dark"
    ></b-table>
  </div>
</template>

<script>
export default {
  name: "PdpDetail",
  props: {
    pdp: {
    type: Object,
    required: true
    }
  },  
  created () {
  },
  data() {
      return {
        headings: ['title', 'description', 'keyActivities', 'deadline', 'progress']
      }
    }
};
</script>

<style scoped>
    .table-page-padding {
        padding: 20px 100px;
    }
</style>