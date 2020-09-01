<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <Pdps v-bind:pdps="pdps"/>
  </div>
</template>

<script>
import Pdps from '@/components/Pdps'
import axios from 'axios';

export default {
  name: 'Home',
  components: {
    Pdps
  },
  data() {
    return {
      pdps: []
    }
  },
  created() {
    axios.get('pdpData.json')
    .then(res => this.pdps = res.data)
    .catch( err => console.log("Error: " + err));
  }
}
</script>
