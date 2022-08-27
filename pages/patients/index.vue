<template>
  <div class="container">
    <div class="page-top come-down">
      <p class="page-title">
        Patients
      </p>
      <button class="admit-btn" @click="$router.push('/patients/new-patient')">
        New Patient
      </button>
    </div>
    <div class="dashboard-table">
      <TablesPatientsTable />
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

.page-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.admit-btn {
  border: none;
  background-color: #1D692C;
  height: 40px;
  color: #fff;
  font-weight: 600;
  font-size: 14px;
  border-radius: 5px;
  width: 8rem;
  cursor: pointer;
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
