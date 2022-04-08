<template>
    <main>
        <Jumbotron/>
        <PostsSection/>
        <CategoryCarousel :postCategories="postCategories"/>
    </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue"
import PostsSection from "./PostsSection.vue"
import CategoryCarousel from "./CategoryCarousel.vue"

export default {
    name: "mainPage",
    props : ["postCategories"],
    components: {
        Jumbotron,
        PostsSection,
        CategoryCarousel,
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