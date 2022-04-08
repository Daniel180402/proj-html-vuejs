<template>
    <div class="category-carousel-wrapper">
        <div class="container h-100 w-100 d-flex justify-content-center align-items-center">
            <button @click="prev" class="prev p-2 rounded-circle"> Prev </button>
            <div class="slider-wrapper h-100 d-flex align-items-center overflow-hidden">
                <div class="category px-5 py-3 mx-4" v-for="(element, index) in postCategories" :key="index + 'categories'">
                    <p class="text-white fw-bold">{{element}}</p>
                </div>
            </div>
            <button @click="next" class="next p-2 rounded-circle"> Next </button>
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
        .prev, .next{
            height: fit-content;
            width: fit-content;
            background-color: black;
            border: none;
            color: white;
        }
        .slider-wrapper{
            .category{
            width: fit-content;
            background-color: $bg-light-black;
        }
        }
    }
</style>