<template>
    <div class="card">
        <div class="thumb">
            <img :src="api.thumb" :alt="api.series">
        </div>
        
        <p>{{api.series}}</p>
    </div>
</template>

<script>
export default {
    name:'Card',
    props:{
        api: Object
    },

}
</script>

<style lang='scss'>

.card{
    width: calc(100% / 6 - 1.875rem);
    min-height: 12.5rem;
    margin: 0 .9375rem 3.125rem .9375rem; 

    .thumb{
        width: 100%;
        max-height: 11.25rem; 
        overflow: hidden;
        object-fit:cover;

        img{
        width: 100%;
        }
    }
    
    p{
        font-size: .875rem;
        margin-top: 1.25rem;
        text-transform: uppercase;

    } 
}
</style>