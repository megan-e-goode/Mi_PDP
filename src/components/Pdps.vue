<template>
    <div>
        <div v-bind:key="pdp.id" v-for="pdp in pdps">
            <PdpItem v-bind:pdp="pdp" />
        </div>
    </div>
</template>

<script>
import PdpItem from './PdpItem.vue';

export default {
    name: "Pdps",
    components: {
        PdpItem
    },
    props: ["pdps"]
}
</script>