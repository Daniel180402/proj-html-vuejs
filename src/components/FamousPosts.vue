<template>
    <div>
        <div class="famous-post-wrapper container mb-5">
            <div class="row">
                <div class="col-9">
                    <div id="page-1">
                        <div class="my-card" v-for="(element, index) in famousPosts1" :key="index + 'posts'">
                            <img :src="element.postImage" class="card-img-top" alt="...">
                            <div class="card-body d-flex">
                                <div class="card-date d-flex flex-column align-items-center pe-3">
                                    <div class="post-date d-flex justify-content-center align-items-center">
                                        {{element.postDay}}
                                    </div>
                                    <div class="post-month d-flex justify-content-center">
                                        {{element.postMonth}}
                                    </div>
                                </div>
                                <div class="card-text pb-2 mb-5">
                                    <h5 class="card-title fw-bold pb-3">{{element.postTitle}}</h5>
                                    <p>{{element.postText}}</p>
                                    <div class="d-flex py-3">
                                        By {{element.postAuthor}} |📁 {{element.postCategory}} | {{element.postComments}} :Comments
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div id="page-2">
                        <div class="my-card" v-for="(element, index) in famousPosts2" :key="index + 'posts'">
                            <img :src="element.postImage" class="card-img-top" alt="...">
                            <div class="card-body d-flex">
                                <div class="card-date d-flex flex-column align-items-center pe-3">
                                    <div class="post-date d-flex justify-content-center align-items-center">
                                        {{element.postDay}}
                                    </div>
                                    <div class="post-month d-flex justify-content-center">
                                        {{element.postMonth}}
                                    </div>
                                </div>
                                <div class="card-text pb-2 mb-5">
                                    <h5 class="card-title fw-bold pb-3">{{element.postTitle}}</h5>
                                    <p>{{element.postText}}</p>
                                    <div class="d-flex py-3">
                                        By {{element.postAuthor}} |📁 {{element.postCategory}} | {{element.postComments}} :Comments
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div id="page-3">
                        <div class="my-card" v-for="(element, index) in famousPosts3" :key="index + 'posts'">
                            <img :src="element.postImage" class="card-img-top" alt="...">
                            <div class="card-body d-flex">
                                <div class="card-date d-flex flex-column align-items-center pe-3">
                                    <div class="post-date d-flex justify-content-center align-items-center">
                                        {{element.postDay}}
                                    </div>
                                    <div class="post-month d-flex justify-content-center">
                                        {{element.postMonth}}
                                    </div>
                                </div>
                                <div class="card-text pb-2 mb-5">
                                    <h5 class="card-title fw-bold pb-3">{{element.postTitle}}</h5>
                                    <p>{{element.postText}}</p>
                                    <div class="d-flex py-3">
                                        By {{element.postAuthor}} |📁 {{element.postCategory}} | {{element.postComments}} :Comments
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="pages d-flex justify-content-end">
                        <div class="page page-selector-1" @click="page1">
                            <p>1</p>
                        </div>
                        <div class="page page-selector-2" @click="page2">
                            <p>2</p>
                        </div>
                        <div class="page page-selector-3" @click="page3">
                            <p>3</p>
                        </div>
                    </div>
                </div>
                <div class="col-3">
                    <div class="aside-social-wrapper">
                        <div class="twitter-wrapper">
                            <h5 class="pb-3">{{twitterTitle}}</h5>
                            <div class="tweet pb-3" v-for="(element, index) in tweet" :key="index + 'tweet'">
                                <p class="tweet-text">{{element.tweet}}</p>
                                <p class="tweet-date">{{element.tweetDate}}</p>
                            </div>
                        </div>
                        <div class="instagram-wrapper mb-5 pb-5">
                            <h5 class="pb-3">{{instagramTitle}}</h5>
                            <div class="card-wrapper pb-3 flex-wrap d-flex">
                                <div class="my-card" v-for="(element, index) in instagram" :key="index">
                                    <img :src="element.img" alt="instagram photo">
                                </div>
                            </div>
                            <h5 class="pb-3">TAGS</h5>
                            <div class="cat-wrapper pb-3 d-flex">
                                <div class="my-card-cat px-2 py-1 bg-dark mx-1 rounded-pill text-white" v-for="(element, index) in instagram" :key="index">
                                    <p>{{element.cat}}</p>
                                </div>
                            </div>
                        </div>
                        <div class="facebook-wrapper">
                            <h5 class="pb-3">{{facebookTitle}}</h5>
                            <div class="facebook-contact ps-3 d-flex align-items-center">
                                <a href="#">Okler Themes</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:"FamousPosts",
    data: function(){
        return {
            twitterTitle: "LATEST FROM TWITTER",
            instagramTitle: "PHOTOS FROM INSTAGRAM",
            facebookTitle: "FIND US ON FACEBOOK",
            actualPage: 1,
            tweet:[
                {
                    tweet: "if you have any suggestions for the next updates, let us know.",
                    tweetDate: "01:05 PM Sep 18th"
                },
                {
                    tweet: "if you have any suggestions for the next updates, let us know.",
                    tweetDate: "01:05 PM Sep 18th"
                }
            ],
            instagram:[
                {
                    img: require("../assets/img/29739607_2020680068220520_4509928046932787200_n.jpg"),
                    cat: "DESIGN"
                },
                {
                    img: require("../assets/img/30087804_253872848488989_8792603541668626432_n.jpg"),
                    cat: "BRANDS"
                },
                {
                    img: require("../assets/img/29415620_196477127626244_3250318472361541632_n.jpg"),
                    cat: "VIDEO"
                },
                {
                    img: require("../assets/img/30078414_1274410412703843_8290935809419247616_n.jpg"),
                    cat: "BUSINESS"
                },
                {
                    img: require("../assets/img/30077195_2066750973610181_3733150062893596672_n.jpg"),
                    cat: "TRAVEL"
                },
                {
                    img: require("../assets/img/29415304_166583630713703_1032667922171953152_n.jpg"),
                    cat: "FASHION"
                }
            ],
            famousPosts1: [
                {
                    postImage: require("../assets/img/blog-54.jpg"),
                    postTitle: "1How to Make Friends as a Grown-up",
                    postText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium exercitationem impedit consectetur veritatis corporis facere ad obcaecati eius! Magni necessitatibus suscipit in, laudantium placeat sequi deserunt unde quam minus ea.",
                    postDay: "12",
                    postMonth: "JAN",
                    postAuthor: "John Doe",
                    postCategory: "Lifestyle, Travel",
                    postComments: "12"
                },
                {
                    postImage: require("../assets/img/blog-55 (1).jpg"),
                    postTitle: "Simple Ways to Have a Pretty Face",
                    postText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium exercitationem impedit consectetur veritatis corporis facere ad obcaecati eius! Magni necessitatibus suscipit in, laudantium placeat sequi deserunt unde quam minus ea.",
                    postDay: "12",
                    postMonth: "JAN",
                    postAuthor: "John Doe",
                    postCategory: "Photography, Travel",
                    postComments: "12"
                },
                {
                    postImage: require("../assets/img/blog-56 (1).jpg"),
                    postTitle: "Ranking the greatest players in basketball",
                    postText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium exercitationem impedit consectetur veritatis corporis facere ad obcaecati eius! Magni necessitatibus suscipit in, laudantium placeat sequi deserunt unde quam minus ea.",
                    postDay: "12",
                    postMonth: "JAN",
                    postAuthor: "John Doe",
                    postCategory: "Sports, Business",
                    postComments: "12"
                },
                {
                    postImage: require("../assets/img/blog-58 (1).jpg"),
                    postTitle: "Top Camper Trailer Towing Tips",
                    postText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium exercitationem impedit consectetur veritatis corporis facere ad obcaecati eius! Magni necessitatibus suscipit in, laudantium placeat sequi deserunt unde quam minus ea.",
                    postDay: "12",
                    postMonth: "JAN",
                    postAuthor: "John Doe",
                    postCategory: "Travel, Lifestyle",
                    postComments: "12"
                },
                {
                    postImage: require("../assets/img/blog-67 (1).jpg"),
                    postTitle: "Why should i buy a Smartwatch",
                    postText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium exercitationem impedit consectetur veritatis corporis facere ad obcaecati eius! Magni necessitatibus suscipit in, laudantium placeat sequi deserunt unde quam minus ea.",
                    postDay: "12",
                    postMonth: "JAN",
                    postAuthor: "John Doe",
                    postCategory: "Technology",
                    postComments: "12"
                },
            ],
            famousPosts2: [
                {
                    postImage: require("../assets/img/blog-66.jpg"),
                    postTitle: "Tips to Help You quickly Prepare your Lunch",
                    postText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium exercitationem impedit consectetur veritatis corporis facere ad obcaecati eius! Magni necessitatibus suscipit in, laudantium placeat sequi deserunt unde quam minus ea.",
                    postDay: "12",
                    postMonth: "JAN",
                    postAuthor: "John Doe",
                    postCategory: "Lifestyle, Travel",
                    postComments: "12"
                },
                {
                    postImage: require("../assets/img/blog-65 (1).jpg"),
                    postTitle: "Main Reasons To Stop Texting And Driving",
                    postText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium exercitationem impedit consectetur veritatis corporis facere ad obcaecati eius! Magni necessitatibus suscipit in, laudantium placeat sequi deserunt unde quam minus ea.",
                    postDay: "12",
                    postMonth: "JAN",
                    postAuthor: "John Doe",
                    postCategory: "Photography, Travel",
                    postComments: "12"
                },
                {
                    postImage: require("../assets/img/blog-56 (1).jpg"),
                    postTitle: "Ranking the greatest players in basketball",
                    postText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium exercitationem impedit consectetur veritatis corporis facere ad obcaecati eius! Magni necessitatibus suscipit in, laudantium placeat sequi deserunt unde quam minus ea.",
                    postDay: "12",
                    postMonth: "JAN",
                    postAuthor: "John Doe",
                    postCategory: "Sports, Business",
                    postComments: "12"
                },
                {
                    postImage: require("../assets/img/blog-58 (1).jpg"),
                    postTitle: "Top Camper Trailer Towing Tips",
                    postText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium exercitationem impedit consectetur veritatis corporis facere ad obcaecati eius! Magni necessitatibus suscipit in, laudantium placeat sequi deserunt unde quam minus ea.",
                    postDay: "12",
                    postMonth: "JAN",
                    postAuthor: "John Doe",
                    postCategory: "Travel, Lifestyle",
                    postComments: "12"
                },
                {
                    postImage: require("../assets/img/blog-67 (1).jpg"),
                    postTitle: "Why should i buy a Smartwatch",
                    postText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium exercitationem impedit consectetur veritatis corporis facere ad obcaecati eius! Magni necessitatibus suscipit in, laudantium placeat sequi deserunt unde quam minus ea.",
                    postDay: "12",
                    postMonth: "JAN",
                    postAuthor: "John Doe",
                    postCategory: "Technology",
                    postComments: "12"
                },
            ],
            famousPosts3: [
                {
                    postImage: require("../assets/img/blog-54.jpg"),
                    postTitle: "3How to Make Friends as a Grown-up",
                    postText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium exercitationem impedit consectetur veritatis corporis facere ad obcaecati eius! Magni necessitatibus suscipit in, laudantium placeat sequi deserunt unde quam minus ea.",
                    postDay: "12",
                    postMonth: "JAN",
                    postAuthor: "John Doe",
                    postCategory: "Lifestyle, Travel",
                    postComments: "12"
                },
                {
                    postImage: require("../assets/img/blog-55 (1).jpg"),
                    postTitle: "Simple Ways to Have a Pretty Face",
                    postText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium exercitationem impedit consectetur veritatis corporis facere ad obcaecati eius! Magni necessitatibus suscipit in, laudantium placeat sequi deserunt unde quam minus ea.",
                    postDay: "12",
                    postMonth: "JAN",
                    postAuthor: "John Doe",
                    postCategory: "Photography, Travel",
                    postComments: "12"
                },
                {
                    postImage: require("../assets/img/blog-56 (1).jpg"),
                    postTitle: "Ranking the greatest players in basketball",
                    postText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium exercitationem impedit consectetur veritatis corporis facere ad obcaecati eius! Magni necessitatibus suscipit in, laudantium placeat sequi deserunt unde quam minus ea.",
                    postDay: "12",
                    postMonth: "JAN",
                    postAuthor: "John Doe",
                    postCategory: "Sports, Business",
                    postComments: "12"
                },
                {
                    postImage: require("../assets/img/blog-58 (1).jpg"),
                    postTitle: "Top Camper Trailer Towing Tips",
                    postText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium exercitationem impedit consectetur veritatis corporis facere ad obcaecati eius! Magni necessitatibus suscipit in, laudantium placeat sequi deserunt unde quam minus ea.",
                    postDay: "12",
                    postMonth: "JAN",
                    postAuthor: "John Doe",
                    postCategory: "Travel, Lifestyle",
                    postComments: "12"
                },
                {
                    postImage: require("../assets/img/blog-67 (1).jpg"),
                    postTitle: "Why should i buy a Smartwatch",
                    postText: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium exercitationem impedit consectetur veritatis corporis facere ad obcaecati eius! Magni necessitatibus suscipit in, laudantium placeat sequi deserunt unde quam minus ea.",
                    postDay: "12",
                    postMonth: "JAN",
                    postAuthor: "John Doe",
                    postCategory: "Technology",
                    postComments: "12"
                },
            ]
        }
    },
    methods: {
        page1(){
            this.actualPage = 1;
            if(this.actualPage == 1){
                document.getElementById("page-2").style.display = "none";
                document.getElementById("page-3").style.display = "none";
                document.getElementById("page-1").style.display = "block";
                document.querySelector(".page-selector-1").style.background = "#0088cc";
                document.querySelector(".page-selector-2").style.removeProperty("background-color");
                document.querySelector(".page-selector-3").style.removeProperty("background-color");
            }
        },
        page2(){
            this.actualPage = 2;
            if(this.actualPage == 2){
                document.getElementById("page-1").style.display = "none";
                document.getElementById("page-3").style.display = "none";
                document.getElementById("page-2").style.display = "block";
                document.querySelector(".page-selector-2").style.background = "#0088cc";
                document.querySelector(".page-selector-1").style.removeProperty("background-color");
                document.querySelector(".page-selector-3").style.removeProperty("background-color");
            }
        },
        page3(){
            this.actualPage = 3;
            if(this.actualPage == 3){
                document.getElementById("page-2").style.display = "none";
                document.getElementById("page-1").style.display = "none";
                document.getElementById("page-3").style.display = "block";
                document.querySelector(".page-selector-3").style.background = "#0088cc";
                document.querySelector(".page-selector-1").style.removeProperty("background-color");
                document.querySelector(".page-selector-2").style.removeProperty("background-color");
            }
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";

    .famous-post-wrapper{
        height: 100%;
        #page-2, #page-3{
            display: none;
        }
        .my-card{
            .card-body{
                .card-date{
                    .post-date{
                        background-color: $bg-light-grey;
                        width: 40px;
                        height: 50px;
                        font-weight: 800;
                    }
                    .post-month{
                        background-color: black;
                        width: 40px;
                        color: white;
                        font-weight: 600;
                        font-size: .8rem;
                    }
                }
                .card-text{
                    border-bottom: 1px solid rgb(241, 241, 241);
                }
            }
        }
        .aside-social-wrapper{
            .twitter-wrapper{
                & > h5{
                font-size: 1.1rem;
                font-weight: 700;
                }
                .tweet-text{
                color: rgb(124, 124, 124);
                }
                .tweet-date{
                    color: $bg-sign-in;
                    font-weight: 500;
                }
            }
            .instagram-wrapper{
                width: 100%;
                
                & > h5{
                    font-size: 1.1rem;
                    font-weight: 700;
                }

                .my-card{
                    width: calc(100% / 3);

                    & > img{
                        width: 100%;

                        &:hover{
                        filter: brightness(80%);
                        }
                    }
                }
                .cat-wrapper{
                    .my-card-cat{
                        width: fit-content;

                        & > p{
                            font-size: .8rem;
                        }
                    }
                }
            }
            .facebook-wrapper{
                & > h5{
                    font-size: 1.1rem;
                    font-weight: 700;
                }
                .facebook-contact{
                    height: 50px;
                    border-left: 6px solid lightgray;

                    & > a{
                        text-decoration: none;
                        font-weight: 500;
                        color: $bg-sign-in;
                    }
                }
            }
        }
        .pages{
            .page{
                & > p{
                    padding: .8rem 1.3rem;
                    color: $bg-dark-blue;
                    border: 1px solid lightgrey;
                    color:  black;
                    font-weight: 700;
                }
                .page-active{
                    background-color: $bg-sign-in;
                }
            }
        }
    }
</style>