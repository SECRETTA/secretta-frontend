<template>
    <div class="footer">
        Secretta <fa-icon :icon="['far', 'copyright']" class="icon"/> 2021
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>

.footer { 
    max-height: 20vh;
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    color: var(--first-color);
    font-size: 1em;
    position: relative;
    bottom: 5%;
    left: 0%;
}

.icon {
    margin: 0vw 1vw;
}



</style>