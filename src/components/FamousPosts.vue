<template>
    <div>
        <div class="famous-post-wrapper container mb-5">
            <div class="row">
                <div class="col-9">

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
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";

    .famous-post-wrapper{
        height: 100%;

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
    }
</style>