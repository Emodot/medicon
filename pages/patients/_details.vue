<template>
  <div class="container">
    <div class="back come-down" @click="$router.go(-1)">
      <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path opacity="0.4" d="M12.0001 22.0002C6.48509 22.0002 2.00009 17.5142 2.00009 12.0002C2.00009 6.48621 6.48509 2.00021 12.0001 2.00021C17.5141 2.00021 22.0001 6.48621 22.0001 12.0002C22.0001 17.5142 17.5141 22.0002 12.0001 22.0002Z" fill="#3F3F3F" />
        <path d="M13.4425 16.2209C13.2515 16.2209 13.0595 16.1479 12.9135 16.0019L9.42649 12.5319C9.28549 12.3909 9.20649 12.1999 9.20649 11.9999C9.20649 11.8009 9.28549 11.6099 9.42649 11.4689L12.9135 7.99692C13.2065 7.70492 13.6805 7.70492 13.9735 7.99892C14.2655 8.29292 14.2645 8.76792 13.9715 9.05992L11.0185 11.9999L13.9715 14.9399C14.2645 15.2319 14.2655 15.7059 13.9735 15.9999C13.8275 16.1479 13.6345 16.2209 13.4425 16.2209Z" fill="#3F3F3F" fill-opacity="0.5" />
      </svg>
      <p>Back</p>
    </div>
    <div class="inner">
      <div class="patient-details">
        <div class="top-block come-down">
          <p class="title">
            David Emaye’s File <span class="adm">(Patient is not on Admission)</span>
          </p>
          <div class="rh-btn">
            <button class="appoint-btn">
              New Appointment
            </button>
            <button class="admit-btn">
              Admit Now
            </button>
          </div>
        </div>
        <div class="details-top">
          <p class="details-title">
            Patient Infomation
          </p>
          <div class="edit">
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
            <p>Edit Patient’s Details</p>
          </div>
        </div>
        <hr class="grey-line">
        <div class="row-ctn">
          <div class="box">
            <p class="box-title">
              First Name
            </p>
            <p class="box-text">
              David
            </p>
          </div>
          <div class="box">
            <p class="box-title">
              Middle Name
            </p>
            <p class="box-text">
              Oluwadamilare
            </p>
          </div>
          <div class="box">
            <p class="box-title">
              Last Name
            </p>
            <p class="box-text">
              Emaye
            </p>
          </div>
          <div class="box">
            <p class="box-title">
              Email Address
            </p>
            <p class="box-text">
              emayeodavid@gmail.com
            </p>
          </div>
        </div>
        <div class="row-ctn">
          <div class="box">
            <p class="box-title">
              Phone Number
            </p>
            <p class="box-text">
              +234 810 8551 935
            </p>
          </div>
          <div class="box">
            <p class="box-title">
              Date of Birth
            </p>
            <p class="box-text">
              15th, May 2015
            </p>
          </div>
          <div class="box">
            <p class="box-title">
              Age
            </p>
            <p class="box-text">
              15
            </p>
          </div>
          <div class="box">
            <p class="box-title">
              Residential Address
            </p>
            <p class="box-text">
              15, Balogun, Ikeja
            </p>
          </div>
        </div>
        <div class="row-ctn">
          <div class="box">
            <p class="box-title">
              Date Registered
            </p>
            <p class="box-text">
              18 Dec 2020
            </p>
          </div>
          <div class="box">
            <p class="box-title">
              Gender
            </p>
            <p class="box-text">
              Male
            </p>
          </div>
          <div class="box">
            <p class="box-title">
              Card Number
            </p>
            <p class="box-text">
              5671828292
            </p>
          </div>
          <div class="box">
            <p class="box-title">
              Patient ID
            </p>
            <p class="box-text">
              178929393
            </p>
          </div>
        </div>
        <div class="row-ctn">
          <div class="box">
            <p class="box-title">
              Next of Kin
            </p>
            <p class="box-text">
              Victor Emaye
            </p>
          </div>
          <div class="box">
            <p class="box-title">
              Next of Kin Phone
            </p>
            <p class="box-text">
              +234 810 8551 935
            </p>
          </div>
          <div class="box">
            <p class="box-title">
              Next of Kin Address
            </p>
            <p class="box-text">
              15, Balogun, Ikeja
            </p>
          </div>
          <div class="box" />
        </div>
      </div>
      <div class="medical-details">
        <div class="inner-tab">
          <div
            :class="activeTab.includes('visit') ? 'active' : 'inactive'"
            class="tab"
            @click="activeTab = 'visit'"
          >
            Visit History
          </div>
          <div
            :class="activeTab.includes('appointments') ? 'active' : 'inactive'"
            class="tab"
            @click="activeTab = 'appointments'"
          >
            Appointments
          </div>
          <div
            :class="activeTab.includes('admissions') ? 'active' : 'inactive'"
            class="tab"
            @click="activeTab = 'admissions'"
          >
            Admissions
          </div>
          <div
            :class="activeTab.includes('vitals') ? 'active' : 'inactive'"
            class="tab"
            @click="activeTab = 'vitals'"
          >
            Vitals
          </div>
          <div
            :class="activeTab.includes('complaints') ? 'active' : 'inactive'"
            class="tab"
            @click="activeTab = 'complaints'"
          >
            Complaints
          </div>
          <div
            :class="activeTab.includes('note') ? 'active' : 'inactive'"
            class="tab"
            @click="activeTab = 'note'"
          >
            Doctor’s Note
          </div>
        </div>
        <div v-if="activeTab == 'visit'" class="tab-1">
          <TablesVisitHistoryTable />
        </div>
        <div v-if="activeTab == 'appointments'" class="tab-1">
          <TablesAppointmentDetailsTable @edit-user="editAppointment = true" />
        </div>
        <div v-if="activeTab == 'admissions'" class="tab-1">
          <TablesAdmissionTable />
        </div>
      </div>
    </div>
    <ModalsPatientEditAppointment v-if="editAppointment" @close-modal="editAppointment = false" />
  </div>
</template>

<script>
export default {
  layout: 'MainLayout',
  data () {
    return {
      activeTab: 'visit',
      editAppointment: false
    }
  }
}
</script>

<style scoped>
.container {
  padding: 30px;
}

.inner {
  background-color: #fff;
  padding: 30px;
  border-radius: 20px;
  width: 90%;
}

.back {
  display: flex;
  align-items: center;
  margin-bottom: 30px;
}

.back svg {
  margin-right: 7px;
}

.back p {
  color: #3F3F3F;
}

.top-block {
  margin-bottom: 40px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.title {
  font-weight: 700;
  font-size: 20px;
}

.adm {
  color: #068F35;
  font-size: 14px;
  font-style: italic;
}

.rh-btn {
  display: flex;
}

.appoint-btn {
  border: 1px solid #1D692C;
  background-color: transparent;
  height: 40px;
  color: #1D692C;
  font-weight: 600;
  font-size: 14px;
  border-radius: 5px;
  width: 9rem;
  cursor: pointer;
  margin-right: 10px;
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

.details-top {
  display: flex;
  justify-content: space-between;
}

.details-title {
  color: #A2ABAA;
  font-size: 15px;
}

.edit {
  display: flex;
  align-items: center;
  cursor: pointer;
}

.edit p {
  color: #A2ABAA;
  font-size: 15px;
  margin-left: 5px;
}

.grey-line {
  border: none;
  border-top: 1px solid #dbd7d7;
  margin-top: 15px;
  margin-bottom: 25px;
}

.row-ctn {
  display: flex;
  margin-bottom: 30px;
}

.more-data {
  margin-bottom: 0;
}

.box {
  flex-basis: 25%;
  padding-right: 20px;
}

.box-ot {
  flex-basis: 50%;
  padding-right: 20px;
}

.box-su {
  flex-basis: 100%;
  padding-right: 20px;
}

.box-ex {
  margin-top: 20px;
  margin-bottom: 30px;
}

.box-title {
  font-size: 13px;
  color: #75759E;
}

.box-text {
  margin-top: 7px;
  line-height: 20px;
  color: #3F3F3F;
}

/* MEDICAL DETAILS */
.medical-details .active {
  color: #1D692C !important;
  border-bottom: 3px solid #1D692C;
}

.inner-tab {
  display: flex;
  margin-top: 50px;
  border-bottom: 1px solid #a8a8ad6e;
}

.medical-details .tab{
  padding: 15px;
  cursor: pointer;
  margin-right: 70px;
  color: #777777;
}

.tab-1 {
  padding-top: 3rem;
}

@media only screen and (max-width: 500px) {
  .container {
    padding: 20px;
  }
  .inner {
    width: 100%;
    padding: 15px;
  }

  .row-ctn {
    margin-bottom: 0;
    flex-wrap: wrap;
  }

  .box {
    flex-basis: 50%;
    margin-bottom: 20px;
  }

  .box-text {
    font-size: 15px;
    word-break: break-word;
  }

  .box-ot {
    margin-bottom: 20px;
  }
}
</style>
