<template>

    <div>
        <div class="container">
            <ul>
                <li v-for="(element, index) in icons" :key="index">
                    <img :src="element.imgSrc" :alt="element.item">
                    <a href="">{{element.item}}</a>
                </li>
            </ul>
        </div>
    </div>
    

    
</template>

<script>
export default {

    name: 'Services',
        data() {

        return {

            icons : [
                {
                    item: "DIGITAL COMICS",
                    imgSrc : '../img/buy-comics-digital-comics.png'
                },
                {
                    item: "DC MERCHANDISE",
                    imgSrc : '../img/buy-comics-merchandise.png'
                },
                {
                    item: "SUBSCRIPTION",
                    imgSrc : '../img/buy-comics-subscriptions.png'
                },
                {
                    item: "COMIC SHOP LOCATION",
                    imgSrc : '../img/buy-comics-shop-locator.png'
                },
                {
                    item: "DC POWER VISA",
                    imgSrc : '../img/buy-dc-power-visa.svg'
                }
            ]
        }
    }

}
</script>

<style lang="scss" scoped>
@import "../assets/style/variables";

div{
    background-color: $primaryBlue;
    font-size: 15px;
    padding: 1.875rem;

    ul{
        display: flex;
        justify-content: space-evenly;

        li{
            display: flex;
            align-items: center;
        }
        img{
            height: 3.125rem;
            margin-right: .75rem;
        }
        a{
            color: $white;
        }


    }

}

</style>