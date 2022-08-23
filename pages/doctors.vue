<template>
  <div class="container">
    <p class="page-title">
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
  margin-top: 5rem;
}

@media only screen and (max-width: 500px) {
  .container {
    padding: 20px;
  }
}
</style>
