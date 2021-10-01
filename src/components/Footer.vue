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

                        <ul v-for="(elm, index) in element.subMenu" :key="index" >

                            <li>
                                <h3>{{elm.list}}</h3>
                            </li>

                            <li v-for="(link , order) in elm.links" href="links.url" :key="order">
                                <a>{{link.linkName}}</a>
                            </li>

                        </ul>

                    </li>

                </ul>

                <div class="logo"></div>


            
            </div>

            <div class="bottom">

                <div class="container">

                    <a href="">SIGN-UP NOW!</a>
                    
                    <ul>
                        <li><h3>FOLLOW US</h3></li>
                        <li v-for="(element, index) in icons" :key="index">
                            <a href="element.url">
                                <img  :src="element.logoSrc " :alt="element.logo">
                            </a>
                        </li>
                    </ul>

                </div>

            </div>

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
                ],
                    subMenu: [
                        {
                        list: "SHOP",
                        links: [
                        { linkName : "Shop DC", url : "#"},
                        { linkName : "Shop DC Collectibles", url : "#"}
                    ]
                },
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
@import "../assets/style/variables";

footer{
    color:lightgray;

    
    .top{
        background-image: url(../assets/img/footer-bg.jpg);
        padding: -6.25rem 0;
       
        .container{
            display: flex;
            justify-content: space-between;

            .main_list{
            display: flex;
            justify-content: flex-start;
            padding: 1.875rem 0;

                li{
                    margin-right: 1.875rem;
                    color: $gray;
                }

                h3{
                    font-size: 1.2em;
                    margin-bottom: .625rem ;
                    color: $white;
                }

                & li:first-child ul:last-child{
                    margin-top:.625rem;
                }

            }

            .logo{
                background-image: url(../assets/img/dc-logo-bg.png);
                background-size: cover;
                background-repeat: no-repeat;
                background-position: center;
                flex-grow: 1;
                margin-left: 12.5rem;
            }
        }

    .bottom{
        background-color: $primaryBlack;
        padding: 1.875rem;

        .container{
            display: flex;
            align-items: center;

            & > a{
                color: $white;
                border: 2px solid $primaryBlue;
                padding: .625rem 1.25rem
            }

            ul{
                display: flex;
                align-items: center;

                & li:first-child{
                    color: $primaryBlue;
                }
                
                li{
                    margin: .625rem;            
                }
            }
        }
    }
       
    


        
    }

    
}


</style>