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
          {customer_name: 'João Adamastor', task_date:'27/5/2021', task_time:'9h'}
        ]
      }
    },
    computed: {
      rows() {
        return this.items.length
      }
    },
    methods: {
    }
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

