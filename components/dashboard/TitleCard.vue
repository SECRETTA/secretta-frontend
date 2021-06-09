<template>
    <div class="card-container">
        <h1>{{welcome()}},</h1>
        <h1>{{userName}}</h1>
    </div>
</template>

<script>
    export default {
        data () {
            return {
                userId : 1,
                userName: ''
            }
        },
        created : function () {
            this.fetchUserInfo();
        },
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
            },
            fetchUserInfo() {
                fetch('http://localhost:3001/api/user/userid/' + this.userId)
                .then(res => res.json())
                .then(obj => {
                  console.log(obj)
                    obj = obj[0];
                    // console.log(obj);
                    this.userName = obj['Name'];
                })
            }
        }
    }
</script>

<style scoped>
.card-container {
    width: 100%;
}

</style>
