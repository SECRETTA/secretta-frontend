<template>
    <div class="card-container">
        <p>card 1</p>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.card-container {
    border: 2px var(--first-color) dashed;
    box-shadow: 0 0 0.5em var(--third-color);
    border-radius: 15px;
    background-color: var(--primary-color);
    min-width: 50%;
    min-height: 40%;
}

</style>