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
  }
};
</script>

<style scoped>
    
</style>
