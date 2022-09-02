<template>
    <footer>
        <div class="insideContainer">
            <a href="https://www.google.com/"><img src="~/assets/images/github.svg" alt="logo"></a>
            <a href="https://www.google.com/"><img src="~/assets/images/linkedin.svg" alt="logo"></a>
            <a href="https://www.google.com/"><img src="~/assets/images/twitter.svg" alt="logo"></a>
            <a href="https://www.google.com/"><img src="~/assets/images/facebook.svg" alt="logo"></a>
            <hr/>
            <NuxtLink to="/jobOffer">jobOffer</NuxtLink>
            <NuxtLink to="/contact">Contact</NuxtLink>
            <NuxtLink to="/landing">Landing</NuxtLink>
            <p>©{{ new Date().getFullYear() }} Tomohiro Iida</p>
        </div>
    </footer>
</template>