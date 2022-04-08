<template>
    <div>
        <div class="wrapper mb-5">
            <div class="jumbotron-wrapper container py-5 flex-wrap d-flex">
                <div class="my-card position-relative" v-for="(element, index) in jumboContent" :key="index">
                    <img :src="element.img" :alt="element.title">
                    <div class="card-text position-absolute text-white p-3">
                        <div class="card-category px-2">
                            <span class="card-category-text fw-bold">{{element.category}}</span>
                        </div>
                        <span class="fs-5 fw-bold">{{element.title}}</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:"MainJumbotron",
    data: function() {
    return {
        jumboContent: [
            {
                img: require("../assets/img/blog-46.jpg"),
                category: "PHOTOGRAPHY",
                title: "How to Take Better Concert Pictures in 30 Seconds"
            },
            {
                img: require("../assets/img/blog-47.jpg"),
                category: "GADGET",
                title: "Gadgets That Make Your Smartphone Even Smarter"
            },
            {
                img: require("../assets/img/blog-48.jpg"),
                category: "TRAVEL",
                title: "20 Top-Rated Tourist Attractions in Manhattan"
            },
            {
                img: require("../assets/img/blog-49.jpg"),
                category: "LIFESTYLE",
                title: "The Best Way to Ride a Motorcycle"
            },
            {
                img: require("../assets/img/blog-50.jpg"),
                category: "TRAVEL",
                title: "5 Fun Things to Do at the Beach"
            },
            {
                img: require("../assets/img/blog-51.jpg"),
                category: "RECIPES",
                title: "Amazingly Fresh Fruits And Herbs Drinks For Summer"
            },
        ]
    }
}
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";

.wrapper{
    height: 100%;
    background-color: $bg-light-grey;

    .jumbotron-wrapper{
        width: 100%;
        gap: 30px;

        .my-card{
            width: calc((100% / 3) - 20px);

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
    }
}
</style>