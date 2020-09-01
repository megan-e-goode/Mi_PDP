<template>
    <div>
        <b-button size="lg" 
            variant="outline-dark" 
            class="pdp-tile" 
            @click="$router.push({name: 'PdpDetail', params: { id: pdp.id, pdp: pdp }})">
            {{pdp.title}}
        </b-button>
    </div>
</template>

<script>
export default {
    name: "PdpItem",
    props: ["pdp"]
}
</script>

<style scoped>
    .pdp-tile {
        margin: 5px;
    }
</style>