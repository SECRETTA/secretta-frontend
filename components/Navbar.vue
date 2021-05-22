<template>
    <div class="navbar">
        <div class="brand">
            <img src="@/assets/img/logo.svg" class="logo"/>
            <p class="title">kairós</p>
        </div>
        <div class="navlinks">
            <a href="/">Início</a>
            <a>Documentação</a>
            <a>Planos</a>
        </div>
        <div class="button">
          <b-button pill type="link" href="/login" variant="outline-light">Login</b-button>
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
    max-height: 15vh;
    color: white;
    font-size: 1.5em;
    padding: 3vh 5vw;
    top: 0;
}

a {
    text-decoration: none;
    color: white;
    margin: 0vw 3vw;
    display: inline;
}

a:hover {
    color: white;
    font-weight: 500;
}

a:active {
    color: white;
    font-weight: 500;
}

.logo {
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
    display: inherit;
    justify-items: center;
    align-items: center;
    padding-right: 15vw;
    position: relative;
    width: 50%;
}

.brand {
    display: inherit;
    justify-items: center;
    align-items: center;
    justify-items: left;
    padding: 0vw 5vw;
}

.button {
    display: inherit;
    position: relative;
}


</style>
