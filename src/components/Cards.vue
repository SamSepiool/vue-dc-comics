<template>
    <div class="cards">
        <Card :api="element" v-for="(element, index) in cards" :key="index"/>
    </div>
</template>

<script>
import Card from "./Card.vue";
import jsCards from "./dc-comics.json";



export default {
    name:'Cards',
    components:{
        Card
    },
     data(){
        return {
            cards: jsCards
        }
    }
    
    


}
</script>

<style lang='scss'>

.cards{
    max-width: 81.25rem;
    margin: auto;
    display: flex;
    flex-wrap: wrap;
    overflow: hidden;
}

</style>