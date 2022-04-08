<template>
    <footer>
        <div class="footer-top-wrapper">
            <div class="footer-top container d-flex align-items-center">
                <div class="row pt-5">
                    <div class="col-3">
                        <h5>{{aboutBlogTitle}}</h5>
                        <div class="about-blog" v-for="(element, index) in aboutBlog" :key="index + 'blog'">
                            <p class="pb-3">{{element.infos}} </p>
                        </div>
                    </div>
                    <div class="col-3">
                        <h5>{{recentPostTitle}}</h5>
                        <div class="recent-post pb-4 d-flex align-items-center" v-for="(element, index) in recentPosts" :key="index + 'posts'"> 
                            <img class="rounded-circle" :src="element.image" :alt="element.title">
                            <div class="post-text d-flex flex-column justify-content-start ps-2">
                                <p class="text-white fw-bold">{{element.title}}</p>
                                <div>
                                    <p class="text-date">{{element.postDate}}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-3">
                        <h5>{{recentCommentTitle}}</h5> 
                        <div class="recent-comments-wrapper d-flex flex-column" v-for="(element, index) in recentComments" :key="index + 'comments'">
                            <div class="recent-comment pb-4">
                                <p class="pb-2"><span>> </span><span class="text-white fw-bold">{{element.username}} </span>commented on <span>{{element.postTitle}}</span></p>
                                <p class="text-date">{{element.commentDate}}</p>
                            </div>
                        </div>
                        
                    </div>
                    <div class="col-3">
                        <h5>{{categoriesTitle}}</h5>
                        <div class="categories-wrapper d-flex flex-wrap">
                            <div class="category p-1 px-2 rounded-3 m-1" v-for="element in categories" :key="element + 'comments'">
                                <p class="text-white fw-bold">{{element}}</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="footer-bottom-wrapper">
            <div class="footer-bottom d-flex justify-content-between container">
                <div class="logo-copyright d-flex align-items-center">
                    <img class="logo-footer" src="../assets/img/logo-footer.png" alt="">
                    <span class="ps-5">&copy; Copyright 2020. All Rights Reserved.</span>
                </div>
                <div class="footer-options d-flex align-items-center">
                    <span>> FAQ's</span>
                    <span>> Sitemap</span>
                    <span>> Contact Us</span>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
name: "pageFooter",
data: function() {
    return {
        aboutBlogTitle: "ABOUT THE BLOG",
        recentPostTitle: "RECENT POSTS",
        recentCommentTitle: "RECENT COMMENTS",
        categoriesTitle: "CATEGORIES",
        aboutBlog :[
            {
                infos: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sint impedit veritatis quod adipisci saepe? Ut, neque optio in voluptatem perspiciatis ."
            },
            {
                infos: "Lorem ipsum dolor, sit amet consectetur adipisicing elit."
            }
        ],
        recentPosts :[
            {
                image: require("../assets/img/our-office-4-square.jpg"),
                title: "Lorem ipsum dolor sit amet consectetur, adipisicing.",
                postDate: "12.53 AM Dec 19th"
            },
            {
                image: require("../assets/img/our-office-5-square.jpg"),
                title: "Lorem ipsum dolor sit amet consectetur.",
                postDate: "12.53 AM Dec 20th"
            }
        ],
        recentComments :[
            {
                username: "John Doe",
                postTitle: "Lorem ipsum dolor sit amet consectetur, adipisicing.",
                commentDate: "12.53 AM Dec 19th"
            },
            {
                username: "Joe Biden",
                postTitle: "Lorem ipsum dolor sit amet consectetur, adipisicing.",
                commentDate: "11.13 AM Nov 15th"
            }
        ],
        categories :[
            "GADGETS",
            "PHOTOGRAPHY",
            "LIFESTYLE",
            "FASHION",
            "RECIPES",
            "TRAVEL",
            "BUSINESS",
            "ARCHITECTURE",
            "REVIEWS",
            "SPORTS",
            "VIDEOS",
            "TECHNOLOGY",
            "DESIGN"
        ] 
    }
}
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";

footer{
    .footer-top-wrapper{
        background-color: $bg-footer-grey;
        height: 45vh;
        .footer-top{   
            height: 100%;

            & h5{
                color: white;
                font-size: 1rem;
                padding-bottom: 1.5rem;
            }
            
            & p {
                color: $text-dark-grey;
            }
            .recent-post{
                & img{
                    height: 5rem;
                }
                .post-text{
                    .text-date{
                        color: $text-dark-grey;
                    }
                }
            }
            .recent-comments-wrapper{
                & span{
                    color: $bg-sign-in;
                }
                & p{
                    color: white;
                }
                .recent-comment{
                    .text-date{
                        color: $text-dark-grey;
                    }
                }
            }
            .categories-wrapper{
                .category{
                    width: fit-content;
                    background-color: black;

                    & > p{
                        font-size: .8rem;
                    }
                }
            }
        }
    }
    .footer-bottom-wrapper{
        background-color: $bg-footer-dark-grey;
        height: 12vh;
        .footer-bottom{
            height: 100%;
            .logo-copyright{

                & > span{
                    color: $text-dark-grey;
                }
                .logo-footer{
                    width: 7rem;
                    filter: grayscale(90%);
                }
            }
            .footer-options{
                
                & > span{
                    padding-right: 1.2rem;
                    color: $text-dark-grey;
                }
            }
            .chat-box{
                bottom: 0;
                right: 0;
            }
        }
    }
}
</style>