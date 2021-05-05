<template>
    <footer >
        
        <div class="container div-layer">
            <div class="footer-head">

            </div>
            <div class="footer-main">
                <div class="main-left">
                    <div> 
                        <ul>
                            <li>
                                DC Comics
                            </li>
                            <li v-for="(link, index) in linksFooter" :key="index">
                                <a href="link.url">
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
                                <a href="link.url">
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
                                <a href="link.url">
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
                                <a href="link.url">
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
            <div class="container">

            </div>
        </div>
        
    </footer>
</template>

<script>
export default {
    name:'footerDC',
    data(){
        return {
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

            
        }
    }
}
</script>

<style scoped>
    footer {       
        background-image: url(../assets/img/footer-bg.jpg);
    }
    /* .bg-img {
        width: 98.8vw;        
        position: relative;
        z-index: -1;
    }

    .bg-img img {
        width: 100%;
        position: absolute;
    } */

    .div-layer {
        display: flex;
        flex-direction: column;
        position: relative;
        width: 1000px;
        height: 100%;
        margin: 0 auto;
        z-index: 1;
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
        width: 70%;
        right: 0;
        top: -33px;

    }

    .footer-foot {
        height: 90px;
        background: #303030;
    }

</style>