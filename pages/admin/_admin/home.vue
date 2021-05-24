<template>
    <div class="home-container">
        <div class="home-grid">
        <div class="card1"></div>
        <div class="card2"></div>
        <div class="card3"></div>
        <div class="card4"></div>
        <div class="card5"></div>
    </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.home-container { /* trocar por grid */
    display: flex;
    border-radius: 15px;
    box-sizing:border-box;
    color: var(--first-color);
    min-height: 75vh; 
    min-width: 70vw;
    margin-right: 5vw;
}

.home-grid {
    display: grid; 
    grid-template-columns: 30vw 2vw 19vw 2vw 19vw;
    grid-template-rows: 35vh 2vw 36vh;
}
.card1 {
    grid-column: 1 / 2;
    grid-row: 1 / 2;
    border-radius: 15px;
    /* border: 1px var(--first-color) dashed; */
    background-color: var(--card-color);
    box-shadow: 0 0 1em 0.1px var(--boxshadow-color);
}

.card2 {
    grid-column: 1 / 2;
    grid-row: 3 / 4;
    border-radius: 15px;
    /* border: 1px var(--first-color) dashed; */
    background-color: var(--card-color);
    box-shadow: 0 0 1em 0.1px var(--boxshadow-color);
}

.card3 {
    grid-column: 3 / 4;
    grid-row: 1/ 2;
    border-radius: 15px;
    /* border: 1px var(--first-color) dashed; */
    background-color: var(--card-color);
    box-shadow: 0 0 1em 0.1px var(--boxshadow-color);
}

.card4 {
    grid-column: 5 / 6;
    grid-row: 1/ 2;
    border-radius: 15px;
    /* border: 1px var(--first-color) dashed; */
    background-color: var(--card-color);
    box-shadow: 0 0 1em 0.1px var(--boxshadow-color);
}

.card5 {
    grid-column: 3 / 6;
    grid-row: 3/ 4;
    border-radius: 15px;
    /* border: 1px var(--first-color) dashed; */
    background-color: var(--card-color);
    box-shadow: 0 0 1em 0.1px var(--boxshadow-color);
}
</style>