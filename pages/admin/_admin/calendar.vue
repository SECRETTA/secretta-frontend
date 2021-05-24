<template>
    <div class="calendar-container">
        <div class="calendar-grid">
        <div class="card1"></div>
        <div class="card2"></div>
        <div class="card3"></div>
    </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.calendar-container { /* trocar por grid */
    display: flex;
    border-radius: 15px;
    box-sizing:border-box;
    color: var(--first-color);
    min-height: 75vh; 
    min-width: 70vw;
    margin-right: 5vw;
}

.calendar-grid {
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
    grid-column: 3 / 6;
    grid-row: 1/ 4;
    border-radius: 15px;
    /* border: 1px var(--first-color) dashed; */
    background-color: var(--card-color);
    box-shadow: 0 0 1em 0.1px var(--boxshadow-color);
}

</style>