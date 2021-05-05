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
                <div  :class="[{ active: link.current }, 'blue-border-hover']"></div>
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
                {text:'comics', url: '/comics', current:true},
                {text:'movies', url: '/movies', current:false},
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

<style scoped lang="scss">
@import '../Styles/headerDC';


</style>