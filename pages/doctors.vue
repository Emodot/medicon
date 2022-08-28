<template>
  <div class="container">
    <p class="page-title come-down">
      Doctors
    </p>
    <div class="dashboard-table">
      <TablesDoctorsTable />
    </div>
  </div>
</template>

<script>
export default {
  layout: 'MainLayout'
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
