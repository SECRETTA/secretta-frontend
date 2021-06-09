<template>
    <div class="card-container">
        <template v-if="items.length == 0">
         <h3>Não há agendamentos hoje</h3>
        </template>
        <template v-else>
          <h5>Agendamentos hoje</h5>
          <h1 v-for="item in items" :key="item.task_time" style="font-size: 7em; align-self:center;">
            "{{item.customer_name}} - {{item.task_time}}"
          </h1>
        </template>
    </div>
</template>

<script>
    export default {
      data () {
        return {
          items: [
            // {customer_name, task_time:}
          ]
        }
      },
      methods : {
        fetchTasks () {
          fetch('http://localhost:3001/api/task/userid/1')
          .then(res => res.json())
          .then(obj => {
            console.log(obj);
            for (let i=0; i < obj['tasks'].length; i++){
                let startDate = new Date(obj['tasks'][i]['start']);
                if (this.isToday(startDate)){
                  console('today!')
                  let taskTime = this.getFormattedTime(startDate);
                  let newItem = {customer_name: obj['tasks'][i]['customerName'], task_time: taskTime};
                  this.items.push(newItem);
                }
              }
          })
        },
        isToday (date) {
          let now = Date();
          return date.getDate() == now.getDate() &&
                date.getMonth() == now.getMonth() &&
                date.getFullYear() == now.getFullYear();
        },
      }
    }
</script>

<style scoped>
.card-container {
    width: 100%;
    display: flex;
    flex-direction: column;
}
</style>
