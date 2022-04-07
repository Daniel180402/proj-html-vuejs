<template>
    <footer>
        <div class="footer-top">

        </div>
        <div class="footer-bottom">

        </div>
    </footer>
</template>

<script>
export default {
name: "pageFooter",
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";

footer{
    
    .footer-top{
        background-color: $bg-footer-grey;
        height: 45vh;
    }
    .footer-bottom{
        background-color: $bg-footer-dark-grey;
        height: 12vh;
    }
}
</style>