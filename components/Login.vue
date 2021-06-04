<template>
    <div class="login">
        <div class="login-form">
            <h3>Acesse seu painel de controle.</h3>
            <b-form-input 
                class="login-input"
                v-model="form.email"
                type="email"
                placeholder="E-mail"
                required />
            <b-form-input 
                class="login-input"
                v-model="form.password"
                type="password"
                placeholder="Senha"
                required />
            <b-form-checkbox
                class="login-input"
                id="checkbox-1"
                v-model="form.remember"
                name="checkbox-1">
                Mantenha-me conectado
            </b-form-checkbox>
            <b-button type="submit" variant="light">Entrar</b-button>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                form: {
                email: '',
                password: '',
                remember: ''
                }
            }
        },
        
    }
</script>

<style scoped>
.login {
    display: flex;
    flex-direction: column;
    justify-items: center;
    align-items: center;
}

.login-form {
    display: flex;
    flex-direction: column;
    justify-self: center;
}

.login-input {
    display: block;
    margin: 2vh 0vw;
    justify-self: center;
    background-color: transparent;
}

</style>