<template>
    <header>
        <div class="sign-in-wrapper">
            <div class="sign-in container d-flex align-items-center">
                <p class="text-white"> Everything about lifestyle, Travel and Gadgets!</p>
                <!-- <p v-for="element in signIn" :key="element"> {{element}} </p> -->
                <p class="px-4 text-white" v-for="(element, index) in signIn" :key="index"> {{signIn[index]}} </p>
            </div>
        </div>
        <div class="logo-wrapper container d-flex align-items-center">
            <img class="my-logo" src="../assets/img/logo-default-slim.png" alt="logo">
        </div>
        <div class="navbar-wrapper d-flex align-items-center">
            <div class="container d-flex align-items-center justify-content-between">
                <nav class="my-navbar d-flex">
                    <li class="list-unstyled pe-5 fw-bold active-tab">HOME</li>
                    <li class="list-unstyled pe-5 fw-bold" v-for="(element, index) in navbarTabs" :key="index"> {{navbarTabs[index]}} </li>
                </nav>
                <div class="input-group w-25">
                    <div class="input-group-prepend">
                        <button class="btn btn-outline-primary" type="button">Search</button>
                    </div>
                    <input type="text" class="form-control" placeholder="" aria-label="" aria-describedby="basic-addon1">
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: "pageHeader",
    data: function() {
        return {
            signIn: [
                "SIGN IN",
                "ABOUT US",
                "CONTACT US",
                "BUY NOW",
            ],
            navbarTabs: [
                "ELEMENTS",
                "FEATURES",
                "PAGES",
                "PORTFOLIO",
                "BLOG",
                "SHOP",
            ]    
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";

header{
    
    .sign-in-wrapper{
        height: 5vh;
        background-color: $bg-sign-in;

        .sign-in{
            height: 100%;

            & > p{
                font-size: .8rem;
            }
        }
    }
    .logo-wrapper{
        height: 10vh;

        .my-logo{
            width: 8rem;
        }
    }
    .navbar-wrapper{
        height: 6vh;
        border-top: 1px solid lightgray;
        border-bottom: 1px solid lightgray;

        .active-tab{
            color: $bg-sign-in;
        }
    }
}
</style>