<template>
  <div class="container">
    <p class="page-title come-down">
      Appointments
    </p>
    <div class="dashboard-table">
      <TablesAppointmentTable @edit-user="editAppointment = true" />
    </div>
    <ModalsEditAppointment v-if="editAppointment" @close-modal="editAppointment = false" />
  </div>
</template>

<script>
export default {
  layout: 'MainLayout',
  data () {
    return {
      editAppointment: false
    }
  }
}
</script>

<style scoped>
.container {
  padding: 50px;
}

.dashboard-table {
  margin-top: 3rem;
}

@media only screen and (max-width: 500px) {
  .container {
    padding: 20px;
  }
  .dashboard-table {
    margin-top: 3rem;
  }
}
</style>
