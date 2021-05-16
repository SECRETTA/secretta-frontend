<template>
    <div class="img-content" :data-aos="position">
        <b-img :src="getImageURL(name)" />
    </div>
</template>

<script>
    export default {
        name: Image,
        props:{
            position: String,
            name: String
        },
        methods: {
            getImageUrl(imageId) {
                return `@/assets/img/${imageId}`
            }
        }
    }
</script>

<style scoped>
.img-content {
    display: flex;
    flex-direction: column;
}
</style>