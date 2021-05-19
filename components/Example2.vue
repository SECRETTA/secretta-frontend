<template>
    <div class="row">
        <div class="text" data-aos-delay="200" data-aos="fade-right">
            <h1>Personalize a sua disponibilidade</h1>
            <p>Você pode estabelezer a sua disponibilidade de atendimento com base em um padrão semanal ou de forma personalizada, dia a dia.</p>
        </div>
        <div class="img-content" data-aos-delay="200" data-aos="fade-left">
            <b-img src="@/assets/img/3.png" />
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
    justify-content: left;
    text-align: right;
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
