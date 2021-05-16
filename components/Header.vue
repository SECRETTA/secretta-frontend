<template>
    <div>
        <div class="phrase">
            <nobr>Sua <span id="title">secretária</span> virtual.</nobr>
            <div class="signup">
                <b-input-group class="mt-3">
                    <b-form-input class="mail" v-model="email" placeholder="Seu e-mail"></b-form-input>
                    <b-input-group-append>
                        <b-button block variant="light" @click="registerEmail">Entre na lista de espera</b-button>
                        </b-input-group-append>
                </b-input-group>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
      data: {
        email : "",
        timestamp : ""
      },
      methods:{
        registerEmail() {
          this.timestamp = new Date(Date.now()).toISOString().slice(0, 19).replace('T', ' ');
          fetch('localhost:3001/api/email',
          {
            headers: { 'Content-Type': 'application/json'},
            method: 'post',
            body: JSON.stringify({
              'Email': this.email,
              'Timestamp': this.timestamp
            })
          })
          .then(res => {
            console.log(res);
          })
        }
      }
    }
</script>

<style scoped>

.phrase {
    display: flex;
    flex-direction: column;
    justify-items: center;
    align-items: center;
    color: white;
    font-size: 5em;
    min-height: 60vh;
    padding: 15vh;
    white-space:nowrap;
}

.signup {
    display: flex;
    flex-direction: row;
    justify-items: center;
    align-items: center;
    color: white;
    font-size: 1.5em;
    padding: 10vh;
}

.mail {
    background-color: transparent;
}

span {
    white-space:normal;
    display: inline;
    background: -webkit-linear-gradient(bottom,#cd32fc, #42f5e9);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}



</style>
