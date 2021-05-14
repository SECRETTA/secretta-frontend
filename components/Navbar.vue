<template>
    <div class="navbar">
        <div class="brand">
            <img src="@/assets/img/logo.svg" class="logo"/>
        </div>
        <div class="navlinks">
            <a href="/">Início</a>
            <a>Documentação</a>
            <a>Planos</a>
        </div>
        <div class="button"></div>
        <b-button pill type="link" href="/login" variant="outline-light">Login</b-button>
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
    min-height: 15vh;
    color: white;
    font-size: 1.5em;
    padding: 1vh 5vw;
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
    height: 10vh;
    width: auto;
    display: inline;
    justify-self: center;
    border: 1px white solid;
}

.navlinks {
    display: inherit;
    justify-items: center;
    padding: 0vw 5vw;
    position: absolute;
    right: 50%;
    transform: translate(50%);
}

.brand {
    display: inherit;
    justify-items: left;
    padding: 0vw 5vw;
}

.button {
    display: inherit;
    justify-items: right;
    padding: 0vw 5vw;
}


</style>