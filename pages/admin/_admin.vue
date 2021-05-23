<template>
    <div>
        <Transition appear name="fade">
            <div v-if="$route.path.endsWith('/home')">
                <NuxtChild />
            </div>
            <div v-if="$route.path.endsWith('/calendar')">
                <NuxtChild />
            </div>
            <div v-if="$route.path.endsWith('/config')">
                <NuxtChild />
            </div>
        </Transition>
    </div>
</template>

<script>
    export default {
        layout: 'dashboard'
    }
</script>

<style scoped>
.fade-enter-active, .fade-leave-active {
    transition: opacity .5s;
}
.fade-enter, .fade-leave-to {
    opacity: 0;
}

</style>