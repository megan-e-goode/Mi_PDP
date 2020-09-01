<template>
  <div>
    PDP id: {{ id }}
    PDP title: {{pdp.title}}
  </div>
</template>

<script>
export default {
  name: "PdpDetail",

  props: {
    id: {
      type: String,
      required: true
    },
    pdp: {
    type: Object,
    required: true
    }
  },
  
  created () {
    // Here we will fetch a single pdp using this.id 
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
