<template>
    <main>
        <Jumbotron/>
        <PostsSection :popularPosts="popularPosts"/>
        <CategoryCarousel :postCategories="postCategories"/>
        <FamousPosts/>
    </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue"
import PostsSection from "./PostsSection.vue"
import CategoryCarousel from "./CategoryCarousel.vue"
import FamousPosts from "./FamousPosts.vue"

export default {
    name: "mainPage",
    props : ["postCategories"],
    components: {
        Jumbotron,
        PostsSection,
        CategoryCarousel,
        FamousPosts,
    },
    data: function() {
        return {
            popularPosts: [
                {
                    image: require("../assets/img/blog-55.jpg"),
                    articleName: "Simple Ways to Have a Pretty Face",
                    articleDate: "12, 2019",
                    articleDateMonth: "January"
                },
                {
                    image: require("../assets/img/blog-56.jpg"),
                    articleName: "Ranking the Greatest Players in Basketball",
                    articleDate: "12, 2019",
                    articleDateMonth: "January"
                },
                {
                    image: require("../assets/img/blog-57.jpg"),
                    articleName: "4 Ways to Look Cool in Glasses",
                    articleDate: "12, 2019",
                    articleDateMonth: "January"
                },
                {
                    image: require("../assets/img/blog-58.jpg"),
                    articleName: "Top Camper Trailer Towing Tips",
                    articleDate: "12, 2019",
                    articleDateMonth: "January"
                },
                {
                    image: require("../assets/img/blog-59.jpg"),
                    articleName: "5 Lovely Walks in New York",
                    articleDate: "12, 2019",
                    articleDateMonth: "January"
                },
            ]
        }
    }

}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";


</style>