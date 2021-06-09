<template>
  <div class="table-container">
    <b-table
        :items="items"
        :fields="fields"
        :sort-by.sync="sortBy"
        :sort-desc.sync="sortDesc"
        responsive="sm"
        striped
        borderless="true"
        per-page="7"
        :current-page="currentPage"
        class="appoint-table"
        :dark="$colorMode.preference == 'dark' ? true : false"
    ></b-table>

    <div class="pagination">
        <b-pagination
            v-model="currentPage"
            per-page="7"
            pills
            :total-rows="rows"
            size="sm">
        </b-pagination>
    </div>

  </div>
</template>

<script>
  export default {
    data() {
      return {
        currentPage: 1,
        today: '27/5/2021',
        sortBy: 'date',
        sortDesc: false,
        fields: [
          { key: 'customer_name', sortable: true, label: 'Nome' },
          { key: 'task_date', sortable: true, label: 'Data' },
          { key: 'task_time', sortable: false, label: 'Horário' }
        ],
        items: [
          // {customer_name: 'João Adamastor', task_date:'27/5/2021', task_time:'9h'}
        ],
        todayTasksIndex : []
      }
    },
    computed: {
      rows() {
        return this.items.length
      },
      tasksToday (){
        let result = [];
        for (let i=0; i < this.items.length; i++){
          if (this.isToday(this.items[i]['task_date'])){
            result.push(this.items[i]);
          }
        }
      }
    },
    created : function () {
      this.fetchTasks();
    },
    methods: {
      fetchTasks ()
      {
        fetch('http://localhost:3001/api/task/userid/1')
        .then(res => res.json())
        .then(obj => {
          for (let i=0; i < obj['tasks'].length; i++){
            let startDate = new Date(obj['tasks'][i]['start']);

            let taskDate = String(startDate.getDate()) + '/' + String(startDate.getMonth() + 1) + '/' + String(startDate.getYear() - 100);
            let taskTime = this.getFormattedTime(startDate);

            let newItem = {customer_name: obj['tasks'][i]['customerName'], task_date: taskDate, task_time: taskTime};
            this.items.push(newItem);
          }
        })
      },
      getFormattedTime(date) {
        let hours = String(date.getHours());
        if (hours.length == 1){

          hours = '0' + hours;
        }
        let minutes = String(date.getMinutes());
        if (minutes.length == 1){

          minutes = '0' + minutes;
        }
        let seconds = String(date.getSeconds());
        if (seconds.length == 1){

          seconds = '0' + seconds;
        }

        return hours + ':' +
               minutes + ':' +
               seconds;
      }
    },
  }
</script>

<style scoped>
.table-container {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items:inherit;
    height: 100%;
}

.appoint-table {
  color: var(--text-color);
}
</style>

