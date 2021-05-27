<template>
    <div class="sidebar-content">
        <div class="links">
            <NuxtLink to="/admin/home" class="sidebar-link"><fa-icon :icon="['fas','chart-pie']" class="icon" />Visão Geral</NuxtLink>
            <!-- <NuxtLink to="/admin/calendar" class="sidebar-link"><fa-icon :icon="['fas','calendar']" class="icon" />Calendário</NuxtLink> -->
            <!-- <NuxtLink to="/admin/config" class="sidebar-link"><fa-icon :icon="['fas','user-friends']" class="icon" />Clientes</NuxtLink> -->
            <NuxtLink to="/admin/config" class="sidebar-link"><fa-icon :icon="['fas','cog']" class="icon" />Configurações</NuxtLink>
        </div>
        <div class="footer">
            <p>Secretta <fa-icon :icon="['far', 'copyright']" class="icon"/> 2021</p>
        </div>
    </div>
</template>

<script>
    export default {
    }
</script>

<style scoped>

.sidebar-content{
    background-color: var(--first-color);
    display: flex;
    flex-direction: column;
    position: relative;
    float: left;
    min-width: 15vw;
    min-height: 75%;
    border-radius: 15px;
    box-shadow: 0 0 0.5em var(--boxshadow-color);
    justify-content: top;
    align-items: center;
    padding: 1vh;
    margin-left: 5vw;
    margin-right: 2vw;
}

.links {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 2vh 0vw;
    color: white;
    width: 15vw;
}

.sidebar-link {
    text-decoration: none;
    color: var(--primary-color);
    border: 1px var(--first-color) solid;
    padding: 0 3vh;
    margin: 1.5vh 0;
    margin-right: 1vh;
}

.sidebar-link:hover {
    border: 1px var(--primary-color) solid;
    border-radius: 15px;
}

.sidebar-link:active{
    color: var(--first-color);
    border: 1px var(--primary-color) solid;
    background-color: var(--primary-color);
    
}

.active {
    color: var(--first-color);
    border: 1px var(--primary-color) solid;
    background-color: var(--primary-color);
    border-radius: 15px;
}

.icon {
    margin:0 1vh;
}

.footer {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    position: absolute;
    bottom: 0;
    margin-bottom: 1vh;
}

/*
@media screen and (max-width:992px) { /* tablet
    
}

@media screen and (max-width:600px) { /* mobile 
    
}
*/ 
</style>