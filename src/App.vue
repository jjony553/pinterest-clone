<template>
<Header />
<router-view></router-view>
</template>

<script>
import Header from './components/Header.vue'

export default {
    setup() {
    },
    components: { Header }
}
</script>

<style>

</style>
