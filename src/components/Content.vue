<template>
    <div class="content">
        <Hero src="../img/jumbotron.jpg" alt="hero" height="25rem"/>

        <div class="container">
            <div class="limbo">
                <h2>CURRENT SERIES</h2>
            </div>

            <Cards/>

            <a href="#">LOAD MORE</a>
        </div>

    </div>    
</template>

<script>
import Hero from "./Hero.vue";
import Cards from "./Cards";

export default {
    
    name: 'Content',
    components: {
        Hero,
        Cards
    },
   


}
</script>

<style lang="scss" scoped>
@import "../assets/style/variables";

.content{
    color:$white;
    background-color: $primaryBlack;

    .container{
        display: flex;
        flex-direction: column;
        align-items: flex-start;

        .limbo{
            position: relative;
            top: -2rem;
            padding: .9375rem 1.875rem;
            background-color: $primaryBlue;
        }

        a{
            margin: 1.25rem auto;
            padding: .75rem 3.75rem;
            background-color: $primaryBlue;
            color: inherit;
            font-weight: bold;
        }
    }
}


</style>