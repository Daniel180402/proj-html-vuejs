<template>
    <main>
        <div class="wrapper">
            <div class="jumbotron-wrapper container py-5 flex-wrap d-flex">
                <div class="my-card position-relative" v-for="(element, index) in jumboContent" :key="index">
                    <img :src="`../assets/img/${element.image}`" :alt="element.title">
                    <div class="card-text position-absolute text-white p-3">
                        <div class="card-category px-2">
                            <span class="card-category-text fw-bold">{{element.category}}</span>
                        </div>
                        <span class="fs-5 fw-bold">{{element.title}}</span>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<script>
export default {
name: "mainPage",
data: function() {
    return {
        jumboContent: [
            {
                image: "@/assets/img/blog-46.jpg",
                category: "PHOTOGRAPHY",
                title: "How to Take Better Concert Pictures in 30 Seconds"
            },
            {
                image: "@/assets/img/blog-47.jpg",
                category: "GADGET",
                title: "Gadgets That Make Your Smartphone Even Smarter"
            },
            {
                image: "",
                category: "TRAVEL",
                title: "20 Top-Rated Tourist Attractions in Manhattan"
            },
            {
                image: "",
                category: "LIFESTYLE",
                title: "The Best Way to Ride a Motorcycle"
            },
            {
                image: "",
                category: "TRAVEL",
                title: "5 Fun Things to Do at the Beach"
            },
            {
                image: "",
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

            &:hover{
                filter: brightness(80%);
            }

            & > img{
                width: 100%;
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