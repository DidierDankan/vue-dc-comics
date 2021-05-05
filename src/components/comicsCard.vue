<template>
  <div class="box">
    <div class="box-content">
        <img :src="detail.thumb" :alt="detail.type">
    </div>
    <h5>
        {{detail.series}}
    </h5>
  </div>
</template>

<script>
export default {
    name:'comicsCard',
    props: ['detail'],

}
</script>

<style scoped lang="scss">
.box {
    
    flex-basis: calc(100% / 6);
    padding: 5px;
    .box-content {
        height: 160px;
        overflow-y: hidden;
    }
    
    img {
        width: 100%;
    }

    h5 {
        margin-top: 15px;
        text-transform: uppercase;
        color: #fff;
    }
}
</style>