<template>

    <div class="content">
        <Hero src="../img/jumbotron.jpg" alt="hero" height="25rem"/>

        <div class="container">
            
        </div>
    </div>

    
</template>

<script>
import Hero from "./Hero.vue";

export default {
    
    name: 'Content',
    components: {
        Hero,
    }

}
</script>

<style lang="scss" scoped>
@import "../assets/style/variables";


</style>