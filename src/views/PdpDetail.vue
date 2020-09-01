<template>
  <div>
    PDP id: {{ pdp.id }}
    PDP title: {{pdp.title}}
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
    // Here we will fetch a single pdp using this.id 
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
