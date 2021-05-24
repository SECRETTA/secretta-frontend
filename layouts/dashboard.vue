<template>
    <div class="content">
        <DashboardNavbar />
        
        <div class="page-content">
            <DashboardSidebar />
            <Nuxt nuxt-child-key="dashboard_views" />
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.content {
    background-color: var(--background-color);
    min-width: 100vw;
    min-height: 100vh;
}
.page-content {
    display: flex;
    flex-direction: row;
    margin: 0;
    padding: 0;
    width: auto;
    max-height: 75vh;
}

</style>