<template>
    <div>
        <div class="post-section-wrapper container mb-5">
            <div class="row">
                <div class="col-4">
                    <h5>{{popularPostsTitle}}</h5>
                    <div class="popular-posts py-4 d-flex align-items-center" v-for="(element, index) in popularPosts" :key="index + 'popularPosts'"> 
                        <img :src="element.image" :alt="element.articleName">
                        <div class="popular-posts-text d-flex flex-column justify-content-start ps-3">
                            <p class="mb-0 pb-1">{{element.articleName}}</p>
                            <div>
                                <p class="text-date fw-light"> {{element.articleDateMonth}} {{element.articleDate}}</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-4">
                    <h5>{{recentPostsTitle}}</h5>
                    <div class="popular-posts py-4 d-flex align-items-center" v-for="(element, index) in recentPosts" :key="index + 'recentPosts'"> 
                        <img :src="element.image" :alt="element.articleName">
                        <div class="popular-posts-text d-flex flex-column justify-content-start ps-3">
                            <p class="mb-0 pb-1">{{element.articleName}}</p>
                            <div>
                                <p class="text-date fw-light">{{element.articleDate}}</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-4">
                    <h5>{{featuredPostsTitle}}</h5>
                    <div class="my-card position-relative py-5" v-for="(element, index) in featuredPosts" :key="index">
                        <img :src="element.image" :alt="element.title">
                        <div class="card-text position-absolute text-white p-3 mb-5">
                            <div class="card-category px-2">
                                <span class="card-category-text fw-bold">{{element.articleCategory}}</span>
                            </div>
                            <span class="fs-5 fw-bold">{{element.articleName}}</span>
                        </div>
                    </div>
                    <h5>{{featuredAuthorTitle}}</h5> 
                    <div class="author-card d-flex" v-for="(element, index) in featuredAuthor" :key="index">
                        <img :src="element.image" :alt="element.authorName">
                        <div class="author-info d-flex flex-column justify-content-center ps-3">
                            <h6 class="pb-3 fw-bold fs-5">{{element.authorName}}</h6>
                            <p class="fw-light">{{element.authorInfo}}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:"PostsSection",
    props: ["popularPosts"],
    data: function() {
        return {
            popularPostsTitle: "POPULAR POSTS",
            recentPostsTitle: "RECENT POSTS",
            featuredPostsTitle: "FEATURED POSTS",
            featuredAuthorTitle: "FEATURED AUTHOR",
            recentPosts: [
                {
                    image: require("../assets/img/blog-65.jpg"),
                    articleName: "Main REasons To Stop Textiong And Driving",
                    articleDate: "January 12, 2019"
                },
                {
                    image: require("../assets/img/blog-66 (1).jpg"),
                    articleName: "Tips to Help You Quickly Prepare your Lunch",
                    articleDate: "January 12, 2019"
                },
                {
                    image: require("../assets/img/blog-67.jpg"),
                    articleName: "Why should i buy a Smartwatch",
                    articleDate: "January 12, 2019"
                },
                {
                    image: require("../assets/img/blog-68.jpg"),
                    articleName: "The best Augmented Reality Smartglasses",
                    articleDate: "January 12, 2019"
                },
                {
                    image: require("../assets/img/blog-69.jpg"),
                    articleName: "12 Healthiest Foods to Eat for Breakfast",
                    articleDate: "January 12, 2019"
                },
            ],
            featuredPosts: [
                {
                    image: require("../assets/img/blog-66.jpg"),
                    articleName: "Tips to Help You Quickly Prepare Your Lunch",
                    articleCategory: "RECIPES"
                }
            ],
            featuredAuthor: [
                {
                    image: require("../assets/img/avatar.jpg"),
                    authorName: "John Doe",
                    authorInfo: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Beatae sed dolore doloribus."
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";

    .post-section-wrapper{
        & h5{
            font-size: 1.1rem;
            font-weight: 800;
            padding-bottom: 1.2rem;
        }
        .popular-posts{
            border-bottom: 1px solid lightgray;
            & img{
                width: 5rem;
            }
            .popular-posts-text{
                & > p{
                    font-weight: 700;
                }
            }
        }
        .my-card{
            width: 100%;

            & > img{
                width: 100%;

                &:hover{
                filter: brightness(80%);
                }
            }

            .card-text{
                bottom: 0;
                left: 0;

                .card-category{
                    width: fit-content;
                    background-color: $bg-sign-in;

                    .card-category-text{
                        font-size: .7rem;
                    }
                }
            }
        }
        .author-card{
            & img{
                width: 40%;
            }
        }
    }
</style>