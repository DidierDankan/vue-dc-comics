<template>
    <footer >
        
        <div class="footer-head">
            <div class="container">
                <ul>
                    <li v-for="(item, index) in linksShop" :key="index">
                        <img :src="item.link" :alt="item.text">
                        <a href="/"> {{ item.text }}</a>
                    </li>
                </ul>
            </div>
        </div>
        <div class="container div-layer">
            <div class="footer-main">
                <div class="main-left">
                    <div> 
                        <ul>
                            <li>
                                DC Comics
                            </li>
                            <li v-for="(link, index) in linksFooter" :key="index">
                                <a :href="link.url">
                                    {{ link.text }}
                                </a>
                            </li>       
                        </ul>
                        <!-- second footer links -->
                        <ul>
                            <li>
                                Shop
                            </li>
                            <li v-for="(link, index) in linksFooter2" :key="index">
                                <a :href="link.url">
                                    {{link.text}}
                                </a>
                            </li>
                        </ul>
                    </div>
                    <!-- third footer links -->
                    <div> 
                        <ul>
                            <li>
                                DC 
                            </li>
                            <li v-for="(link, index) in linksFooter3" :key="index">
                                <a :href="link.url">
                                    {{ link.text }}
                                </a>
                            </li>       
                        </ul>
                    </div>
                    <!-- forth footer links -->
                    <div> 
                        <ul>
                            <li>
                                Sites 
                            </li>
                            <li v-for="(link, index) in linksFooter4" :key="index">
                                <a :href="link.url">
                                    {{ link.text }}
                                </a>
                            </li>       
                        </ul>
                    </div>
                </div>
                <div class="main-right">
                    <img src="@/assets/img/dc-logo-bg.png" alt="dc logo footer">
                </div>
            </div>           
        </div>
        <!-- footer del footer -->
        <div class="footer-foot">
            <div class="container ">
                <button class="signUp-btn">
                    sign up now!
                </button>
                <div class="footer-socials">
                    <ul>
                        <li class="follow-social">
                            follow us
                        </li>
                        <li v-for="(social, index) in socialLinks" :key="index">
                            <a :href="social.links">
                                <img :src="social.url" :alt="social.links">
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
    name:'footerDC',
    data(){
        return {
            linksShop: [
                {
                    link:require('@/assets/img/buy-comics-digital-comics.png'),
                    text:'digital comics',
                },
                {
                    link:require('@/assets/img/buy-comics-merchandise.png'),
                    text:'dc merchandise',
                },
                {
                    link:require('@/assets/img/buy-comics-subscriptions.png'),
                    text:'subscription',
                },
                {
                    link:require('@/assets/img/buy-comics-shop-locator.png'),
                    text:'comic shop locator',
                },
                {
                    link:require('@/assets/img/buy-dc-power-visa.svg'),
                    text:'dc power visa',
                },
            ],
            linksFooter:[    
                {text:'characters', url: '/characters'},
                {text:'comics', url: '/comics'},
                {text:'movies', url: '/movies'},
                {text:'tv', url: '/tv'},
                {text:'games', url: '/games'},
                {text:'collectibles', url: '/collectibles'},
                {text:'videos', url: '/videos'},
                {text:'fans', url: '/fans'},
                {text:'news', url: '/news'},
            ],
            linksFooter2: [
                {text:'shop DC', url:'/shopDC'},
                {text:'shop DC Collectibles', url:'/shopDCCollectibles'},
            ],
            linksFooter3: [
                {text:'terms Of Use', url: '/termsOfUse'},
                {text:'privacy Policy (New)', url: '/privacyPolicy'},
                {text:'ad Choices', url: '/AdChoices'},
                {text:'advertising', url: '/Advertising'},
                {text:'jobs', url: '/Jobs'},
                {text:'subscriptions', url: '/subscriptions'},
                {text:'talent Workshops', url: '/TalentWorkshops'},
                {text:'cPSC Certificates', url: '/CPSCCertificates'},
                {text:'ratings', url: '/Ratings'},
                {text:'shop Help', url: '/shopHelp'},
                {text:'contact Us', url: '/contactUs'},
            ],
            linksFooter4: [
                {text:'dC', url: '/DC'},
                {text:'mAD Magazine', url: '/MADMagazine'},
                {text:'dC Kids', url: '/DCKids'},
                {text:'dC Universe', url: '/DCUniverse'},
                {text:'dC Power Visa', url: '/DCPowerVisa'},
                
            ],
            socialLinks: [
                {links:'/facebook', url:require('../assets/img/footer-facebook.png')},
                {links:'/periscope', url:require('../assets/img/footer-periscope.png')},
                {links:'/pinterest', url:require('../assets/img/footer-pinterest.png')},
                {links:'/twitter', url:require('../assets/img/footer-twitter.png')},
                {links:'/youtube', url:require('../assets/img/footer-youtube.png')},
            ],
           
        }
    }
}
</script>

<style scoped lang="scss">
    footer {       
        background-image: url(../assets/img/footer-bg.jpg);
    }

    .div-layer {
        display: flex;
        flex-direction: column;
        position: relative;
        width: 1000px;
        height: 100%;
        margin: 0 auto;
        z-index: 1;
    }
/* footer head */
    .footer-head {
        .container {
            display: flex;
            align-items: center;
            height: 100%;
        }
        background: #0282F9;
        height: 140px;
        ul {
            display: flex;
            align-items: center;
            justify-content: space-around;
            width: 100%;
            list-style: none;
            li {
                display: flex;
                align-items: center;
                justify-content: space-around;
                
                a{
                    margin-left:10px;
                    font-size: .75rem;
                    text-transform: uppercase;
                    text-decoration: none;
                    color: #fff;
                }
            }
        }       
    }

    .footer-head .container ul li img {
        height:40px
    }

    .footer-head .container ul li:last-child img{
        height: 30px;
    }

    .footer-main {
        display: flex;
        justify-content: space-between;
    }

/* footer main left */
    .footer-main .main-left {
        display: flex;
        justify-content: space-around;
        padding: 15px 0;
    }

    .footer-main .main-left > div {
        margin-right: 35px;
    }

    .footer-main .main-left > div:last-child{
        margin-right: 0;
    }

    .footer-main .main-left ul {
        margin-bottom: 10px;
        list-style: none;
    }

    .footer-main .main-left ul li:first-child {
        margin-bottom: 5px;
        color: #fff;
        font-weight: 600;
        text-transform: uppercase;
    }

    .footer-main .main-left ul li a {
        font-size: .8rem;
        color: #69646D;
        line-height: 1.5;
        text-transform: capitalize;
        text-decoration: none;
    }
    
/* footer main right */
    .main-right {
        flex-grow: 1;
        position: relative;
        overflow-y: hidden;
    }

    .main-right img {
        position: absolute;
        width: 75%;
        right: 0;
        top: -65px;

    }
/* footer del footer */

    .footer-foot {
        height: 90px;
        background: #303030;
    }

    .footer-foot .container {
        display: flex;
        justify-content: space-between;
        align-items: center; 
        height: 100%;
    }

    button.signUp-btn {
        padding: 10px 10px;
        text-transform: uppercase;
        background: transparent;
        font-weight: 600;
        color: #fff;
        border: 1px solid #0282F9;
        cursor: pointer;
    }

    .footer-socials ul  {
        display: flex;
        justify-content: center;
        align-items: center;
        list-style: none;
    }

    .footer-socials ul li {
        margin-left: 15px
    }

    .footer-socials ul li img {
        height: 30px;
    }

    .follow-social {
        text-transform: uppercase;
        color: #0282F9;
        font-weight: 600;
        font-size: .8rem;
    }

</style>