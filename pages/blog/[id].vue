<template>
    <div>
        <div class="hero">
            <img :src="data.image" alt="blog-image">
        </div>
        <div class="wrapper">  
            <div class="container">               
                <h1>{{ data.title }}</h1>
                <p>{{ data.date }}</p> 
                <ContentDoc />
            </div> 
            <PrevNext :prev="prev" :next="next" />
        </div>
    </div> 
</template>

<script setup>
//import PrevNext from '../../components/prevNext.vue';
const { data } = await useAsyncData(useRoute().path, () => 
    queryContent(useRoute().path).findOne()
)

const [prev, next] = await queryContent("/blog")
    .sort({ id: 1 })
    .findSurround(useRoute().path)

</script>
