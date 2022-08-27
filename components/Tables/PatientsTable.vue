<template>
  <div>
    <div v-if="transLoading" class="table-loader">
      <TableLoader />
    </div>
    <div v-else class="table-container come-down">
      <div class="table-top">
        <!-- <p class="table-title">
          Appointment Activity
        </p> -->
        <div class="search-box">
          <input type="text" class="search-input" placeholder="Search Patients...">
        </div>
        <!-- <p class="view-all" @click="$router.push('/subscriptions')">
          View All
        </p> -->
      </div>
      <table>
        <tr class="table-header">
          <th class="id">
            Patient ID
          </th>
          <th class="domain">
            Name
          </th>
          <th class="email">
            Email
          </th>
          <th class="date">
            Phone
          </th>
          <th class="date">
            Date Registered
          </th>
          <th class="date">
            Gender
          </th>
          <th class="date">
            Status
          </th>
        </tr>
        <tr v-for="(appointment, index) in appointments" :key="index" class="table-details" @click="$router.push('/patients/details')">
          <td class="id">
            {{ appointment.id }}
          </td>
          <td class="domain">
            {{ appointment.name }}
          </td>
          <td class="email">
            {{ appointment.email }}
          </td>
          <td class="date">
            {{ appointment.phone }}
          </td>
          <td class="date">
            {{ appointment.date }}
          </td>
          <td class="date">
            {{ appointment.gender }}
          </td>
          <!-- <td class="action-ctn">
            <div class="action">
              <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0_149_3086)">
                  <path d="M0 15.3661C0.4448 13.8397 0.888 12.3133 1.3328 10.787C1.368 10.6654 1.4048 10.5438 1.4368 10.4222C1.488 10.2382 1.584 10.0894 1.7312 9.96615C1.8688 9.85255 1.9904 9.71655 2.1168 9.59015C4.2016 7.52456 6.2864 5.45896 8.3696 3.39177C8.4176 3.34377 8.4592 3.28937 8.4928 3.24777C8.776 3.53257 9.0416 3.79977 9.3376 4.09737C9.3056 4.11977 9.2432 4.15177 9.1952 4.19977C7.0352 6.35496 4.8768 8.51016 2.7216 10.6702C2.6448 10.7486 2.5808 10.8558 2.5504 10.9614C2.2912 11.8173 2.0448 12.6781 1.7888 13.5373C1.7568 13.6445 1.7728 13.7117 1.8544 13.7853C1.9872 13.9053 2.104 14.0429 2.2384 14.1613C2.2848 14.2013 2.3728 14.2317 2.4288 14.2173C3.2896 13.9709 4.1488 13.7197 5.0064 13.4605C5.08 13.4381 5.1488 13.3757 5.2064 13.3165C7.3968 11.1326 9.584 8.94536 11.7712 6.75976C11.8128 6.71816 11.848 6.67176 11.872 6.64456C12.1824 6.95496 12.4832 7.25576 12.8128 7.58536C12.7984 7.59496 12.7408 7.61896 12.7008 7.65896C10.544 9.79495 8.384 11.9261 6.2384 14.0733C5.9392 14.3741 5.6144 14.5597 5.2128 14.6733C3.7888 15.0765 2.3712 15.5021 0.9504 15.9197C0.856 15.9469 0.76 15.9725 0.6656 15.9997H0.5376C0.4688 15.9693 0.3984 15.9421 0.3296 15.9101C0.1376 15.8205 0.072 15.6381 0 15.4605V15.3661ZM4.3024 12.7149C4.2608 12.4493 4.216 12.2061 4.1872 11.9629C4.1728 11.8477 4.1264 11.8013 4.0144 11.7805C3.7408 11.7277 3.4704 11.6589 3.2176 11.6029C5.4864 9.32936 7.7552 7.05416 10.0096 4.79337C10.3696 5.15337 10.7456 5.52776 11.1088 5.88936C8.8624 8.14216 6.5952 10.4158 4.3024 12.7149ZM10.8368 1.02538C11.0416 0.825377 11.2464 0.612577 11.4656 0.414178C12.0944 -0.152221 12.9136 -0.139421 13.5264 0.458978C14.2032 1.11818 14.8704 1.78537 15.5296 2.46217C16.1536 3.10057 16.144 3.95497 15.5216 4.59177C15.3344 4.78377 15.1408 4.97097 14.9616 5.14697C13.592 3.77897 12.224 2.41257 10.8368 1.02538ZM9.168 2.53577C9.4784 2.24457 9.7968 1.94537 10.0992 1.66057C11.5328 3.09417 12.9584 4.52137 14.3968 5.95976C14.0976 6.23976 13.776 6.54216 13.4656 6.83336L9.168 2.53577Z" fill="#A0A4A8" />
                </g>
                <defs>
                  <clipPath id="clip0_149_3086">
                    <rect width="16" height="16" fill="white" />
                  </clipPath>
                </defs>
              </svg>
              <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M4.00952 14.3248C4.02552 14.7024 4.33592 15 4.71352 15H11.2911C11.6687 15 11.9807 14.7024 11.9951 14.3248L12.4655 4.408H3.53912L4.00952 14.3248ZM9.48952 6.872C9.48952 6.7136 9.61752 6.5856 9.77592 6.5856H10.2335C10.3919 6.5856 10.5199 6.7152 10.5199 6.872V12.5376C10.5199 12.696 10.3903 12.824 10.2335 12.824H9.77592C9.61752 12.824 9.48952 12.696 9.48952 12.5376V6.872ZM7.48792 6.872C7.48792 6.7136 7.61592 6.5856 7.77432 6.5856H8.23192C8.39032 6.5856 8.51832 6.7152 8.51832 6.872V12.5376C8.51832 12.696 8.39032 12.824 8.23192 12.824H7.77432C7.61592 12.824 7.48792 12.696 7.48792 12.5376V6.872ZM5.48472 6.872C5.48472 6.7136 5.61272 6.5856 5.76952 6.5856H6.22712C6.38552 6.5856 6.51352 6.7152 6.51352 6.872V12.5376C6.51352 12.696 6.38392 12.824 6.22712 12.824H5.76952C5.61112 12.824 5.48472 12.696 5.48472 12.5376V6.872ZM12.7775 1.7216H9.74392V1.1472C9.74392 1.0656 9.67832 1 9.59672 1H6.40952C6.32792 1 6.26232 1.0656 6.26232 1.1472V1.7216H3.22712C2.98392 1.7216 2.78552 1.9184 2.78552 2.1632V3.552H13.2191V2.1632C13.2191 1.92 13.0223 1.7216 12.7775 1.7216V1.7216Z" fill="#FF6760" />
              </svg>
            </div>
          </td> -->
          <td class="type-details" :class="appointment.status === 'Admitted' ? 'success' : '' ">
            {{ appointment.status }}
          </td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>
import functions from '@/utils/functions'
// import Cookies from 'js-cookie'
export default {
  data () {
    return {
      currency: functions.formatCurrency,
      transLoading: false,
      appointments: [
        {
          id: '#ND1283',
          name: 'Leslie Alexander',
          email: 'lesie.alexander@example.com',
          phone: '09099098788',
          date: '22, JAN. 2021',
          gender: 'Male',
          status: 'Admitted'
        },
        {
          id: '#ND1283',
          name: 'Ronald Richards',
          email: 'ronald.richards@example.com',
          phone: '09099098788',
          date: '22, JAN. 2021',
          gender: 'Female',
          status: 'Not Admitted'
        },
        {
          id: '#ND1283',
          name: 'Leslie Alexander',
          email: 'lesie.alexander@example.com',
          phone: '09099098788',
          date: '22, JAN. 2021',
          gender: 'Male',
          status: 'Admitted'
        },
        {
          id: '#ND1283',
          name: 'Ronald Richards',
          email: 'ronald.richards@example.com',
          phone: '09099098788',
          date: '22, JAN. 2021',
          gender: 'Female',
          status: 'Not Admitted'
        },
        {
          id: '#ND1283',
          name: 'Leslie Alexander',
          email: 'lesie.alexander@example.com',
          phone: '09099098788',
          date: '22, JAN. 2021',
          gender: 'Male',
          status: 'Admitted'
        },
        {
          id: '#ND1283',
          name: 'Ronald Richards',
          email: 'ronald.richards@example.com',
          phone: '09099098788',
          date: '22, JAN. 2021',
          gender: 'Female',
          status: 'Not Admitted'
        },
        {
          id: '#ND1283',
          name: 'Leslie Alexander',
          email: 'lesie.alexander@example.com',
          phone: '09099098788',
          date: '22, JAN. 2021',
          gender: 'Male',
          status: 'Admitted'
        },
        {
          id: '#ND1283',
          name: 'Ronald Richards',
          email: 'ronald.richards@example.com',
          phone: '09099098788',
          date: '22, JAN. 2021',
          gender: 'Female',
          status: 'Not Admitted'
        }
      ]
    }
  },
  created () {
    // this.getTransactions()
  },
  methods: {
    // getTransactions () {
    //   this.transLoading = true
    //   this.$axios.$get('/get_transaction_by_id/', {
    //     headers: {
    //       Authorization: `Bearer ${Cookies.get('token')}`
    //     }
    //   }).then((response) => {
    //     // console.log(response)
    //     this.transLoading = false
    //     this.transactions = response.data
    //   })
    // },
  }
}
</script>

<style scoped>

.table-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 30px 30px;
}

.table-title {
  font-size: 22px;
  font-weight: 700;
  color: #474680;
}

.search-box {
  border: 1px solid #064a7b2c;
  height: 50px;
  background-color: #fafafa;
  display: flex;
  width: 25rem;
  padding: 0 15px;
  border-radius: 100px;
}

::placeholder {
  font-size: 14px;
}

.search-input {
  width: 100%;
  border: none;
  background-color: transparent;
  outline: none;
}

.view-all {
  font-size: 15px;
  cursor: pointer;
}
.table-loader {
  margin-top: 100px;
}
.table-container {
  background-color: #ffffff;
  border-radius: 10px;
  width: 100%;
  /* border: 1px solid #1A240; */
}
table, th, td {
  width: 100%;
  /* border: 1px solid #fff; */
  border-collapse: collapse;
  font-size: 15px;
}
.table-header {
  height: 60px;
  background-color: #F0F2F4;
  padding: 0 20px;
}

.table-header th {
  font-weight: 500;
  color: #474680;
}
.table-details {
  height: 60px;
  padding: 0 20px;
  cursor: pointer;
}
.table-details:nth-child(odd) {
  height: 60px;
  background-color: #F9FAFB;
  padding: 0 20px;
}
th {
  text-align: left;
}

.id {
  width: 13rem;
  padding-left: 25px;
}

.domain {
  width: 14rem;
}

.date {
  width: 18rem;
}

.email {
  width: 18rem;
}

.description {
  width: 20rem;
}

.type {
  width: 10rem;
}

.action-ctn {
  width: 7rem;
}

.action {
  /* width: 5rem; */
  display: flex;
  align-items: center;
}

.action svg {
  margin: 0 3px;
  cursor: pointer;
}

.type-details {
  width: 10rem;
  color: #EE3E3E;
}

.success {
  color: #4ABF21;
}

.amount {
  width: 13rem;
}

@media only screen and (max-width: 500px) {
  .table-container {
    width: 100%;
    overflow: auto;
  }

  .table-top {
    padding: 20px 15px;
  }

  .search-box {
    width: 60%;
  }

  table {
    width: 47rem;
  }

  .email {
    width: 25rem;
  }
}
</style>
