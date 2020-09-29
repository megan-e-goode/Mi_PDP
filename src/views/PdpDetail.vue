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
  methods: {
    SetProgressValues(goals) {
      goals.forEach(goal => {
        var progressDescription = (function(progressIndicator) {
          switch (progressIndicator) {
              case 1: 
                return "Not Started";
              case 2: 
                return "Planning";
              case 3: 
                return "In Progress";
              case 4: 
                return "Complete";
              default:
                return "N/A";
            }
        })(goal.progress);

        goal.progress = progressDescription;
      });
    }
  },
  created () {
    this.SetProgressValues(this.pdp.goals);
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