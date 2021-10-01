<template>

    <header>
        <div class="container">

            <div class="logo">
                <a href="#"><img src="../assets/img/dc-logo.png" alt=""></a>
            </div>
            <nav>
                <ul>
                    <li v-for="(element, index) in menu" :key="index"><a :class="{ active : element.current }" :href="element.url">{{element.item}}</a></li>
                </ul>
            </nav>

        </div>

    </header>
    
</template>

<script>
export default {
    name: 'Header',
    data(){
        return {
            menu:[
                {
                    item: 'CHARACTERS',
                    url: '#',
                    current: false
                },
                 {
                    item: 'COMICS',
                    url: '#',
                    current: true
                },
                 {
                    item: 'MOVIES',
                    url: '#',
                    current: false
                },
                 {
                    item: 'TV',
                    url: '#',
                    current: false
                },
                 {
                    item: 'GAMES',
                    url: '#',
                    current: false
                },
                   {
                    item: 'COLLECTIBLES',
                    url: '#',
                    current: false
                },
                 {
                    item: 'VIDEOS',
                    url: '#',
                    current: false
                },
                 {
                    item: 'FANS',
                    url: '#',
                    current: false
                },
                 {
                    item: 'NEWS',
                    url: '#',
                    current: false
                },
                 {
                    item: 'SHOP',
                    url: '#',
                    current: false
                },                
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/variables";
header {
    background-color: $white;
    font-weight: bold;
    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;

        ul{
            display: flex;
            li{
                display: flex;
                align-items: center;
                margin: 0 .625rem;
            }
            
            a{
                display: inline-block;
                padding: 3.4375rem 0;
                color: $primaryBlack;

                &:active{
                    color: $primaryBlue;
                    box-shadow: 0px -5px 0px inset $primaryBlue; 
                }
            }
        }
    }
   
}
</style>