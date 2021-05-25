<template>
    <div class="content">
        <div class="brand">
            <img src="@/assets/img/logo.svg" class="logo"/>
            <p class="title">secretta</p>
        </div>
        
        <div class="user">
            <!-- <fa-icon :icon="['fas', 'search']" class="icon" /> -->
            <!-- <fa-icon :icon="['far', 'bell']" class="icon" /> -->
            <fa-icon :icon="['fas', dark_mode ? 'moon' : 'sun']" class="icon" v-on:click="dark_mode=!dark_mode; $colorMode.preference = dark_mode ? 'dark' : 'light'"/>
            <fa-icon :icon="['fas', 'sign-out-alt']" class="icon" />
            <!-- <b-dropdown size="sm"  variant="link" toggle-class="text-decoration-none" no-caret>
                <template #button-content>
                    <fa-icon :icon="['fas', 'bars']" class="icon" />
                </template>
                <b-dropdown-item class="menu-item"><fa-icon :icon="['fas', 'sign-out-alt']" class="icon" /> Sair</b-dropdown-item>
                <b-dropdown-text>
                    <b-form-checkbox switch v-model="dark_mode">
                    </b-form-checkbox>
                    <p>{{dark_mode ? "Escuro" : "Claro"}}</p>
                </b-dropdown-text>
            </b-dropdown> -->
            <b-avatar size="5vh" style="margin-left:1vh;"></b-avatar>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                dark_mode: true
        }
    }
}
</script>

<style scoped>
.content {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    min-height: 15vh;
    max-width: 100vw;
    padding: 1vh 0vw;
}

.brand {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    min-width: 15vw;
    margin-left: 5vw;
}

.logo {
    height: 5vh;
    width: auto;
}

.title {
    font-family: 'Unica One', cursive;
    color: #ef5d60;
    font-size: 5vh;
    margin: 0vh 1vw;
}

.user {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    color: #ef5d60;
    min-width: 15vw;
    margin-right: 5vw;
}

.icon {
    margin:0 1vh;
    font-size: 4vh;
    padding: 0.5vh 0;
    color: var(--first-color);
}

.mode-switch {
    font-family: 'Poppins', sans-serif;
    font-size: 1em;
}

.menu-item {
    display:flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
}

</style>