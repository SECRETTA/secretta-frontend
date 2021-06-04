<template>
    <div class="form-container">
        <h5 style="margin-bottom:2vh;">Disponibilidade de atendimento</h5>

        <b-form>
        <div class="form-day">
            <p>Segunda</p>
            <b-form-group inline>
                <b-input-group inline>
                    <b-form-timepicker 
                        v-model="value" 
                        hour12="false" 
                        pill 
                        hide-header="true" 
                        placeholder="--:--"
                        label-close-button="Fechar">
                    </b-form-timepicker>
                    <b-form-timepicker 
                        v-model="value" 
                        hour12="false" 
                        pill 
                        hide-header="true" 
                        placeholder="--:--"
                        label-close-button="Fechar">
                    </b-form-timepicker>
                </b-input-group>
            </b-form-group>
        </div>

        <div class="form-day">
            <p>Terça</p>
            <b-form-group inline>
                <b-input-group inline>
                    <b-form-timepicker 
                        v-model="value" 
                        hour12="false" 
                        pill 
                        hide-header="true" 
                        placeholder="--:--"
                        label-close-button="Fechar">
                    </b-form-timepicker>
                    <b-form-timepicker 
                        v-model="value" 
                        hour12="false" 
                        pill 
                        hide-header="true" 
                        placeholder="--:--"
                        label-close-button="Fechar">
                    </b-form-timepicker>
                </b-input-group>
            </b-form-group>
        </div>

        <div class="form-day">
            <p>Quarta</p>
            <b-form-group inline>
                <b-input-group inline>
                    <b-form-timepicker 
                        v-model="value" 
                        hour12="false" 
                        pill 
                        hide-header="true" 
                        placeholder="--:--"
                        label-close-button="Fechar">
                    </b-form-timepicker>
                    <b-form-timepicker 
                        v-model="value" 
                        hour12="false" 
                        pill 
                        hide-header="true" 
                        placeholder="--:--"
                        label-close-button="Fechar">
                    </b-form-timepicker>
                </b-input-group>
            </b-form-group>
        </div>

        <div class="form-day">
            <p>Quinta</p>
            <b-form-group inline>
                <b-input-group inline>
                    <b-form-timepicker 
                        v-model="value" 
                        hour12="false" 
                        pill 
                        hide-header="true" 
                        placeholder="--:--"
                        label-close-button="Fechar">
                    </b-form-timepicker>
                    <b-form-timepicker 
                        v-model="value" 
                        hour12="false" 
                        pill 
                        hide-header="true" 
                        placeholder="--:--"
                        label-close-button="Fechar">
                    </b-form-timepicker>
                </b-input-group>
            </b-form-group>
        </div>

        <div class="form-day">
            <p>Sexta</p>
            <b-form-group inline>
                <b-input-group inline>
                    <b-form-timepicker 
                        v-model="value" 
                        hour12="false" 
                        pill 
                        hide-header="true" 
                        placeholder="--:--"
                        label-close-button="Fechar">
                    </b-form-timepicker>
                    <b-form-timepicker 
                        v-model="value" 
                        hour12="false" 
                        pill 
                        hide-header="true"
                        placeholder="--:--" 
                        label-close-button="Fechar">
                    </b-form-timepicker>
                </b-input-group>
            </b-form-group>
        </div>

        <div class="form-day">
            <p>Sábado</p>
            <b-form-group inline>
                <b-input-group inline>
                    <b-form-timepicker 
                        v-model="value" 
                        hour12="false" 
                        pill 
                        hide-header="true" 
                        placeholder="--:--"
                        label-close-button="Fechar">
                    </b-form-timepicker>
                    <b-form-timepicker 
                        v-model="value" 
                        hour12="false" 
                        pill 
                        hide-header="true" 
                        placeholder="--:--"
                        label-close-button="Fechar">
                    </b-form-timepicker>
                </b-input-group>
            </b-form-group>
        </div>

        <div class="form-day">
            <p>Domingo</p>
            <b-form-group inline>
                <b-input-group inline>
                    <b-form-timepicker 
                        v-model="value" 
                        hour12="false" 
                        pill 
                        hide-header="true" 
                        placeholder="--:--"
                        label-close-button="Fechar">
                    </b-form-timepicker>
                    <b-form-timepicker 
                        v-model="value" 
                        hour12="false" 
                        pill 
                        hide-header="true" 
                        placeholder="--:--"
                        label-close-button="Fechar">
                    </b-form-timepicker>
                </b-input-group>
            </b-form-group>
        </div>
    </b-form>

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
    width: auto;
    padding: 3vh;
}

.form-day {
    padding: 0 2vw;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 100%;
}
</style>