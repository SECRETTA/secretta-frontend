<template>
    <div class="img-content" :class="position">
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

.left {
    justify-content: left;
}

.right {
    justify-content: right;
}
</style>