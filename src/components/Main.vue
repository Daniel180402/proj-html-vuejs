<template>
    <main>
        <Jumbotron/>
    </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue"

export default {
    name: "mainPage",
    components: {
        Jumbotron,
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";


</style>