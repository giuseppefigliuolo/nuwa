<template>
    <section>
        <div class="title">
            <h3>{{ title }}</h3>
        </div>
        <div class="illustration">
            <img :src="require('../assets/capsule-illustration.png')" :alt="title" />
        </div>
    </section>
</template>

<script>
export default {
    props: ['title']
}
</script>

<style leng="scss" scoped>
    section{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    .title{
        margin: 2em;
    }
    h3{
        font-size: 2em;
    }
    img{
        width: 100%;
    }
   
</style>