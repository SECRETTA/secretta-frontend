<template>
    <div class="form-container">
        <h5 style="margin-bottom:2vh;">Suas informações</h5>
        <div class="settings-form">
            <b-form>
                <b-form-group
                    inline
                    id="name-group"
                    class="form-item"
                    label="Nome"
                    label-cols-sm="2"
                    label-align-sm="right"
                    label-for="name">
                    <b-form-input 
                        id="name" 
                        v-model="name" 
                        type="text" 
                        placeholder="user.name">
                    </b-form-input>
                </b-form-group>
                <!-- <b-form-group
                    inline
                    id="uname-group"
                    class="form-item"
                    label="Nome de usuário"
                    label-cols-sm="2"
                    label-align-sm="right"
                    label-for="uname">
                    <b-form-input 
                        id="uname" 
                        v-model="uname" 
                        type="username" 
                        placeholder="user.username">
                    </b-form-input>
                </b-form-group> -->
                <b-form-group
                    inline
                    id="email-group"
                    class="form-item"
                    label="E-mail"
                    label-cols-sm="2"
                    label-align-sm="right"
                    label-for="email">
                    <b-form-input 
                        id="email" 
                        v-model="email" 
                        type="email" 
                        placeholder="user.email">
                    </b-form-input>
                </b-form-group>
                <b-form-group
                    inline
                    id="phone-group"
                    class="form-item"
                    label="Telefone"
                    label-cols-sm="3"
                    label-align-sm="left"
                    label-for="phone">
                    <b-form-input 
                        id="phone" 
                        v-model="tel" 
                        type="tel" 
                        placeholder="user.phone">
                    </b-form-input>
                </b-form-group>
                <b-form-group
                    inline
                    id="bio-group"
                    class="form-item"
                    label="Sobre você"
                    label-cols-sm="2"
                    label-align-sm="left"
                    label-for="bio">
                    <b-form-input 
                        id="bio" 
                        v-model="bio" 
                        type="text" 
                        style="height:10vh;"
                        placeholder="user.bio">
                    </b-form-input>
                </b-form-group>
                <b-form-group
                    inline
                    id="int-group"
                    class="form-item"
                    label="Intervalo das consultas"
                    label-cols-sm="4"
                    label-align-sm="left"
                    label-for="int">
                    <b-form-input
                        id="int"
                        v-model="int"
                        type="time">
                    </b-form-input>
                </b-form-group>
                <b-button 
                    block 
                    :variant="$colorMode.preference == 'dark' ? 'outline-light' : 'outline-dark'">
                Salvar informações</b-button>
            </b-form>
        </div>
    </div>
</template>

<script>
    export default {
        // data () {

        // },
        // methods: {
        //     setSchedule () {

        // },
        //     setInfo () {}  
        // }
}
</script>

<style scoped>
.form-container {
    width: auto;
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

.form-item {
    margin: 0 0;
}

</style>