<template>
    <div class="row">
        <div class="img-content" data-aos="fade-right">
            <b-img src="@/assets/img/4.png" data-aos="fade-right" />
        </div>
        <div class="text">
            <h1>Disponível o tempo todo</h1>
            <p>Sem mais preocupações quanto a marcar atendimentos fora do horário comercial.</p>
        </div>
    </div>
</template>

<script>
    export default {
        methods: {
            getImageUrl: function(imageId) {
                return `@/assets/img/${imageId}`
            }
        }
    }
</script>

<style scoped>
.row {
    display: flex;
    flex-direction: row;
    justify-self: center;
    padding: 2vh;
    flex-wrap: nowrap;
    align-items: center;
    max-width: 100vw;
    max-height: 70vh;
    margin-bottom: 10vh;
}
.img-content {
    display: flex;
    flex-direction: column;
    position: relative;
    max-width: 45%;
    padding: 5vw;
    margin: 1vw;
}

.text {
    display: flex;
    flex-direction: column;
    justify-content: right;
    text-align: left;
    color: white;
    position: relative;
    max-width: 45%;
    padding: 5vw;
    margin: 1vw;
}

p {
    font-size: 1.5em;
    font-weight: 300;
}
</style>