<template>
    <div class="card-container">
        <h1>{{welcome()}},</h1>
        <h1>"{user.first_name}'"</h1>
    </div>
</template>

<script>
    export default {
        methods: {
            welcome() {
                var myDate = new Date();
                var hrs = myDate.getHours();

                if (hrs < 12){
                    return 'Bom dia';
                } else if (hrs >= 12 && hrs <= 17) {
                    return 'Boa tarde';
                }
                else if (hrs >= 17 && hrs <= 24){
                    return 'Boa noite';
                }
            }
        }
    }
</script>

<style scoped>
.card-container {
    width: 100%;
}

</style>