<template>
    <div class="category-carousel-wrapper">
        <div class="container h-100 w-100 d-flex justify-content-center align-items-center">
            <!-- <button @click="scrollLeft" class="prev p-2 rounded-circle"> Prev </button> -->
            <div class="slider-wrapper h-100 d-flex align-items-center overflow-auto pt-2">
                <div class="category px-5 py-3 mx-4 d-flex justify-content-center" v-for="(element, index) in postCategories" :key="index + 'categories'">
                    <p class="text-white fw-bold">{{element}}</p>
                </div>
            </div>
            <!-- <button @click="next" class="next p-2 rounded-circle"> Next </button> -->
        </div>
    </div>  
</template>

<script>
export default {
    name:"CategoryCarousel",
    props: ["postCategories"],
    data: function(){
        return {
        }
    },
    methods: {
        
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";

    .category-carousel-wrapper{
        height: 20vh;
        background-color: $bg-dark-blue;

        .slider-wrapper{
            width: 100%;

            .category{
                width: calc(100% / 7);
                background-color: $bg-light-black;

                &:hover{
                    background-color: $text-dark-grey;
                }
            }
        }
    }
</style>