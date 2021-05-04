<template>
    <header class="container">
        <a href="/">
            <img src="@/assets/img/dc-logo.png" alt="DC logo">
        </a>
      <!-- header nav -->
        <ul>
            <li v-for="(link, index) in links" :key="index" >
                <a :class ="{ active: link.current }" :href="link.url" >
                   {{ link.text }} 
                </a>
            </li>
        </ul>
    </header>
</template>

<script>
export default {
    name:'headerDC',
    data() {
        return {
            links:[
                {text:'characters', url: '/characters', current:false},
                {text:'comics', url: '/comics', current:false},
                {text:'movies', url: '/movies', current:true},
                {text:'tv', url: '/tv', current:false},
                {text:'games', url: '/games', current:false},
                {text:'collectibles', url: '/collectibles', current:false},
                {text:'videos', url: '/videos', current:false},
                {text:'fans', url: '/fans', current:false},
                {text:'news', url: '/news', current:false},
                {text:'shop', url: '/shop', current:false},
            ]
        }
    },
}
</script>

<style scoped>
    header {
        display:flex;
        justify-content: space-between;
        align-items: center;
        padding: 15px 0;
    }

    header a img {
        height: 70px;
    }

    ul {
        display: flex;
        list-style: none;
    }

    ul li {
        position:relative;
        margin-right: 15px;
        line-height: 4;     
    }

    ul li:last-child {
        margin-right: 0;
    }

    li > a {
        font-size: .7rem;
        color: #4A4C5F;
        font-weight: 600;
        text-decoration: none;
        text-transform: uppercase;
    }

    .blue-border-hover {
    visibility: hidden; 
    position: absolute;
    bottom: -50%;
    left: 50%;
    width: 35px;
    height: 3px;
    transform: translate(-50%, -90%);
    background: #0282F9;
    border-radius: 5px;
    }

    ul li.blue-border-hover.active,
    ul li.blue-border-hover:hover {
        visibility: visible;
    }

    li > a.active,
    li > a:hover {
        color: #0282F9;
    }
    


</style>