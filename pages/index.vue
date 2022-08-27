<template>
  <div class="container">
    <div class="cards">
      <div class="card come-down">
        <div class="card-img">
          <img src="~assets/images/first aid.png" alt="">
        </div>
        <div class="card-details">
          <p class="card-name">
            Appointments
          </p>
          <p class="card-num">
            213
          </p>
        </div>
      </div>
      <div class="card come-down">
        <div class="card-img">
          <img src="~assets/images/crutch.png" alt="">
        </div>
        <div class="card-details">
          <p class="card-name">
            New Patients
          </p>
          <p class="card-num">
            104
          </p>
        </div>
      </div>
      <div class="card come-down">
        <div class="card-img">
          <img src="~assets/images/operation theater.png" alt="">
        </div>
        <div class="card-details">
          <p class="card-name">
            On Admission
          </p>
          <p class="card-num">
            24
          </p>
        </div>
      </div>
      <div class="card come-down">
        <div class="card-img">
          <img src="~assets/images/UserCirclePlus.png" alt="">
        </div>
        <div class="card-details">
          <p class="card-name">
            Doctors
          </p>
          <p class="card-num">
            7
          </p>
        </div>
      </div>
    </div>
    <div class="dashboard-table">
      <TablesDashboardTable />
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

.cards {
  display: flex;
  justify-content: space-between;
}

.card {
  flex-basis: 24%;
  padding: 24px;
  display: flex;
  background-color: #fff;
  border-radius: 8px;
}

.card-img {
  margin-right: 15px;
}

.card-name {
  color: #474680;
  font-weight: 600;
}

.card-num {
  color: #474680;
  font-size: 24px;
  margin-top: 10px;
}

.dashboard-table {
  margin-top: 5rem;
}

@media only screen and (max-width: 900px) {
  .cards {
    flex-wrap: wrap;
  }

  .card {
    flex-basis: 48%;
    margin-bottom: 20px;
  }
}

@media only screen and (max-width: 500px) {
  .container {
    padding: 20px;
  }
  .cards {
    flex-direction: column;
  }

  .card {
    margin-bottom: 10px;
  }
}
</style>
