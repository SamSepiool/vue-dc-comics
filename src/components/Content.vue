<template>

    <div class="content">
        <Hero src="../img/jumbotron.jpg" alt="hero" height="25rem"/>

        <div class="container">
            <div class="limbo">
                <h2>CURRENT SERIES</h2>
            </div>
            
        </div>
    </div>

    
</template>

<script>
import Hero from "./Hero.vue";
// import jsCards from "./dc-comics.json"

export default {
    
    name: 'Content',
    components: {
        Hero,
    },
    // data(){
    //     return {
    //         cards: jsCards
    //     }
    // }


}
</script>

<style lang="scss" scoped>
@import "../assets/style/variables";

.content{
    color:$white;

    .container{
        
        .limbo{
            display: inline-block;
            position: relative;
            top: -2rem;
            padding: .9375rem 1.875rem;
            background-color: $primaryBlue;
        }
    }
}


</style>