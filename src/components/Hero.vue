<template>

    <div class="hero">
        <img :src="src" :alt="alt" :style="`height:${height}`">
    </div>

    
</template>

<script>
export default {
    
    name: 'Hero',
    props:[
        'src', 'alt', 'height'
    ],
};
</script>

<style lang="scss" scoped>
@import "../assets/style/variables";

.hero{
    position: relative;
    width: 100%;
    display: flex;

    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top center;
    }

}

</style>