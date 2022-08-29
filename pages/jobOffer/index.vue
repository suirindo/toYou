<template>
    <div class="wrapper">
        <div class="container">
        <h1>jobOffer</h1>
        <p>エンジニアの日常生活をお届けします</p>
        <div v-for="singleData in data" :key="singleData.id" class="jobOfferCard">                            
            <div class="textsContainer">
                <h3>{{ singleData.title }}</h3>
                <p>{{ singleData.excerpt }}</p>
                <p>{{ singleData.date }}</p>
                <NuxtLink :to="singleData._path" class="linkButton">Read More</NuxtLink> 
            </div>
            <div class="jobOfferImg">
                <img :src="singleData.image" alt="jobOffer-image">
            </div>  
        </div>
        </div>
        <Pagination :numberPages="numberPages" />
    </div>
</template>

<script setup>
//import Pagination from '../../components/pagination.vue';
const jobOffersPerPage = 5
const { data } = await useAsyncData("jobOfferQuery", () => 
    queryContent("/jobOffer")
    .sort({ id: -1 })
    .limit(jobOffersPerPage)
    .find()
)
const alljobOffers = await queryContent("/jobOffer").find()

const numberPages = Math.ceil(alljobOffers.length / jobOffersPerPage)

useHead({
    title: "ブログ",
    meta: [
        { name: "description", content: "ブログページです"}
    ],
})

</script>