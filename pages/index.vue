<template>
    <div>
        <div class="hero">
            <img src="~/assets/images/index-hero.jpg" alt="hero">
            <div class="textContainer">
                <h1>Tomohiro Iida</h1>
                <h3>JavaScript Developer</h3>
            </div>
        </div>
        <div class="container">
            <div class="profile">
                <div>
                    <h2>JavaScript Nerd</h2>
                    <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
                </div>
                <img src="~/assets/images/profile.jpg" alt="profile">
            </div>
            <div class="skills">
                <h2>Skills</h2>
                <div class="skillsContainer">
                    <div><img src="~/assets/images/javascript.svg" alt="javascript"><span>JavaScript / 10 years</span></div>
                    <div><img src="~/assets/images/react.svg" alt="react"><span>React / 4 years</span></div>
                    <div><img src="~/assets/images/vue.svg" alt="vue"><span>Vue / 4 years</span></div>
                    <div><img src="~/assets/images/nuxt.svg" alt="nuxt"><span>Nuxt / 3 years</span></div>
                </div>
            </div>
            <div class="ctaButton">
                <NuxtLink to="/contact">Make It Happen!</NuxtLink>
            </div>
        </div>
    </div>
</template>

<script setup>
useHead({
    title: "Tomohiro Iida Official Site",
    meta: [
        { name: "description", content: "Tomohiro Iidaのポートフォリオサイトです"}
    ],
})
</script>