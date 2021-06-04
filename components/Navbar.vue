<template>
    <div class="navbar">
        <div class="brand">
            <img src="@/assets/img/logo.svg" class="logo"/>
            <nuxt-link to="/" style="margin-left:-0.5vw;"><p class="title">secretta</p></nuxt-link>
        </div>
        <div class="navlinks">
            <!-- <NuxtLink to="/">Início</NuxtLink>
            <NuxtLink to="/docs">Documentação</NuxtLink>
            <NuxtLink to="/planos">Planos</NuxtLink>
            <NuxtLink to="/admin/home">Admin*</NuxtLink> -->
        </div>
        <div class="button">
            <b-button pill prefetch=true to="/login" variant="outline-light">Login</b-button>
        </div>
    </div>
</template>

<script>
    export default {

    }
</script>

<style>
.navbar {
    display: flex;
    flex-direction: row;
    align-items: center;
    max-height: 15vh;
    color: var(--first-color);
    font-size: 1.5em;
    padding: 3vh 5vw;
    top: 0;
}

a {
    text-decoration: none;
    color: var(--first-color);
    margin: 0vw 3vw;
    display: inline;
}

a:hover {
    color: var(--first-color);
    text-decoration: none;
}

a:active {
    color: var(--first-color);
    text-decoration: none;
}

.logo {
    float: left;
    height: 5vh;
    width: auto;
    display: inline;
}

.title {
    font-family: 'Unica One', cursive;
    color: #ef5d60;
    font-size: 5vh;
    display: inline;
    margin: 0vh 1vw;
}


.navlinks {
    display: flex;
    justify-content: cen;
    align-items: center;
    position: relative;
    width: 50%;
}

.brand {
    display: flex;
    justify-items: center;
    align-items: center;
    justify-items: left;
    padding: 0vw 5vw;
}

.button {
    display: flex;
    position: relative;
    align-items: center;
}


</style>
