<template>
    <main>
        <Jumbotron/>
        <PostsSection/>
    </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue"
import PostsSection from "./PostsSection.vue"

export default {
    name: "mainPage",
    components: {
        Jumbotron,
        PostsSection,
    },
    data: function() {
        return {

        }
    }

}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";


</style>