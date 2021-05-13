<template>
    <div class="navbar">
        <div class="brand">
            <img src="@/assets/img/logo.svg" class="logo"/>
        </div>
        <div class="navlinks">
            <a>Início</a>
            <a>Documentação</a>
        </div>
        <div class="button"></div>
        <b-button variant="outline-light">Login</b-button>
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
    margin: 0vw 3vw;
    display: inline;
}

a:hover {
    font-weight: 500;
}

a:active {
    font-weight: 500;
}

.logo {
    height: 13vh;
    width: auto;
    display: inline;
    justify-self: center;
}

.navlinks {
    display: inherit;
    justify-items: center;
    padding: 0vw 5vw;
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