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
        ]
      }
    },
    computed: {
      rows() {
        return this.items.length
      }
    },
    created : function () {
      this.fetchTasks();
    },
    methods: {
      fetchTasks ()
      {
        console.log('start-fetch')
        fetch('http://localhost:3001/api/task/userid/1'/*,
          {
            headers: { 'Content-Type': 'application/json'},
            method: 'get',
          }*/)
          .then(res => res.json())
          .then(obj => {
            console.log(obj);
            console.log('len', obj['tasks'].length);
            for (let i=0; i < obj['tasks'].length; i++){
              let startDate = new Date(obj['tasks'][i]['start']);
              let taskDate = String(startDate.getDate()) + '/' + String(startDate.getMonth() + 1) + '/' + String(startDate.getYear() - 100);
              console.log(taskDate);
              let newItem = {customer_name: obj['tasks'][i]['customerName'], task_date: taskDate, task_time:'9h'};
              this.items.push(newItem);
            }
          })
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

