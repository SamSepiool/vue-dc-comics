<template>

    <footer>
        <div class="top">

            <div class="container">

                <ul class="main_list">
                    <li v-for="(element, index) in lists" :key="index" >
                        <h3>{{element.list}}</h3>
                        <ul>
                            <li v-for="(link , order) in element.links" href="links.url" :key="order">
                                <a>{{link.linkName}}</a>
                            </li>
                        </ul>
                    </li>
                </ul>
            
            </div>

        </div>

        <div class="bottom">

        </div>
    </footer>

    

    
</template>

<script>
export default {

    name: 'Footer',
     data() {
        return {
            lists:[
                {
                    list: "COMICS",
                    links: [
                        { linkName : "Characters", url : "#"},
                        { linkName: "Comics", url : "#" },
                        { linkName: "Movies", url : "#" },
                        { linkName: "TV", url : "#" },
                        { linkName: "Games", url : "#" },
                        { linkName: "Videos", url : "#" },
                        { linkName: "News", url : "#" }
                    ]
                },
                     {
                    list: "DC",
                    links: [
                        { linkName : "Terms Of Use", url : "#"},
                        { linkName : "Privacy Policy (New)", url : "#"},
                        { linkName : "Ad Choices", url : "#"},
                        { linkName : "Advertising", url : "#"},
                        { linkName : "Jobs", url : "#"},
                        { linkName : "Subscriptions", url : "#"},
                        { linkName : "Talent Workshops", url : "#"},
                        { linkName : "CPSC Certificates", url : "#"},
                        { linkName : "Ratings", url : "#"},
                        { linkName : "Shop Help", url : "#"},
                        { linkName : "Contact us", url : "#"}
                    ]
                },
                {
                    list: "SITES",
                    links: [
                        { linkName : "DC", url : "#"},
                        { linkName : "MAD Magazine", url : "#"},
                        { linkName : "DC Kids", url : "#"},
                        { linkName : "DC Universe", url : "#"},
                        { linkName : "DC Power Visa", url : "#"}
                    ]
                },
                {
                    list: "SHOP",
                    links: [
                        { linkName : "Shop DC", url : "#"},
                        { linkName : "Shop DC Collectibles", url : "#"}
                    ]
                },
              
                
            ],
            icons: [
                {logo: "Facebook", logoSrc : '../img/footer-facebook.png', url : "#"},
                {logo: "Twitter", logoSrc : '../img/footer-twitter.png', url : "#"},
                {logo: "YouTube", logoSrc : '../img/footer-youtube.png', url : "#"},
                {logo: "Pinterest", logoSrc : '../img/footer-pinterest.png', url : "#"},
                {logo: "Periscope", logoSrc : '../img/footer-periscope.png', url : "#"}
                
            ]
        }
    }
  

}
</script>

<style lang="scss" scoped>
@import "@/assets/style/variables";

footer{
    color:lightgray;
    
   

    .top{
        background-image: url(../assets/img/footer-bg.jpg);



        .main_list{
            display: flex;
            flex-wrap: wrap;
            padding: 1.875rem 0;

            li{
                margin-right: 1.875rem;
            }
            h3{
                font-size: 1.2em;
                margin-bottom: .625rem ;
                color: $white;
            }

            & > li:last-child{
                flex-basis: 100%;
                border: 1px solid red;
                
            }
        }

        
    }

    .bottom{
        background-color: $primaryBlack;
    }
}


</style>