<template>
    <div class="form-container">
        <h5>Disponibilidade de atendimento</h5>
        <b-form-group inline>
            <b-form-timepicker 
                v-model="value" 
                hour12="false" 
                pill 
                hide-header="true" 
                label-close-button="Fechar">
            </b-form-timepicker>
            <b-form-timepicker 
                v-model="value" 
                hour12="false" 
                pill 
                hide-header="true" 
                label-close-button="Fechar">
            </b-form-timepicker>
        </b-form-group>
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
    width: auto
}
</style>