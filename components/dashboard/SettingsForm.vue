<template>
    <div class="form-container">
        <h5 style="margin-bottom:2vh;">Configurações de usuário</h5>
        <div class="settings-form">
            <b-form>
                <label for="name">Seu nome</label>
                <b-form-input id="name" v-model="name" type="text" placeholder="user.name"></b-form-input>
                <b-form-input v-model="email" type="email" placeholder="user.email"></b-form-input>
            </b-form>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.form-container {
    width: 100%;
    display: flex;
    flex-direction: column;
    color: var(--text-color);
    padding: 3vh;
}

.settings-form {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

</style>