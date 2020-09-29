<template>
    <div>
        <b-navbar variant="dark" type="dark" class="line-height-50">
            <b-navbar-brand href="#" class="line-height-50">
            <b-avatar variant="light" src="/img/profileBitmoji.c6a8131b.png" alt="Profile photo"></b-avatar>
            Mi PDP
            </b-navbar-brand>
            <router-link to="/">Home</router-link> |
            <router-link to="/about">About</router-link>
        </b-navbar>
    </div>
</template>

<script>
export default {
    name: "Navbar"
}
</script>

<style scoped>
</style>