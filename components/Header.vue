<template>
    <div>
        <div class="phrase">
            Sua secretária virtual.
            <div class="signup">
                <b-form-input class="mail" v-model="text" placeholder="Seu e-mail"></b-form-input><b-button block variant="light">Entre na lista de espera</b-button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>

.phrase {
    display: flex;
    flex-direction: column;
    justify-items: center;
    align-items: center;
    color: white;
    font-size: 5em;
    min-height: 60vh;
    padding: 15vh;
}

.signup {
    display: flex;
    flex-direction: row;
    justify-items: center;
    align-items: center;
    color: white;
    font-size: 1.5em;
    padding: 10vh;
}

.mail {
    background-color: transparent;
}

</style>