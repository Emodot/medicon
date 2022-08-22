<template>
  <div class="header-container">
    <div class="left-side">
      <div class="mobile-logo">
        <img src="~assets/images/medicon-logo.png" alt="">
      </div>
      <p v-if="pageName !== 'det'" class="head-page-title">
        {{ pageName }}
      </p>
      <p v-else class="head-page-title">
        Details
      </p>
      <div class="btn">
        <!-- <button v-if="$route.name === '/' " class="blue-btn" @click="handleNewCampaignShow">
          TOP UP
        </button> -->
        <!-- <button v-if="$route.name === 'verify-overview'" class="green-btn" @click="downloadReport()">Download Report <img src="~assets/icons/download.svg" alt=""></button> -->
        <!-- <button v-if="$route.name === 'voice-logs'" class="green-btn">Download Report <img src="~assets/icons/download.svg" alt=""></button> -->
        <!-- <button v-if="$route.name === 'sms-contact'" class="blue-btn" @click="$emit('openNewContact')">Add New  <span class="plus">+</span></button> -->
      </div>
    </div>
    <div class="right-side">
      <div class="middle-section">
        <div class="balance-box">
          <p class="title">
            CHALLENGERS ONLINE
          </p>
          <p class="price">
            {{ challengersOnline }} ONLINE
          </p>
        </div>
        <div class="balance-box">
          <p class="title">
            BALANCE
          </p>
          <p class="price">
            {{ formatNaira (balance) }}
          </p>
        </div>
        <div class="topup-btn">
          <button @click="$router.push('/fund-account')">
            TOP UP
          </button>
        </div>
      </div>
      <div class="last-section">
        <div class="notification" @click="$emit('openNotification')">
          <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M4.39046 8.12495C4.38943 7.38371 4.53511 6.64959 4.81912 5.96491C5.10313 5.28024 5.51984 4.65854 6.04524 4.13567C6.57064 3.61279 7.19433 3.19907 7.88036 2.91837C8.5664 2.63766 9.30121 2.49551 10.0424 2.50011C13.1354 2.5231 15.6094 5.09396 15.6094 8.19557V8.74995C15.6094 11.548 16.1948 13.1717 16.7104 14.0592C16.7659 14.154 16.7955 14.2618 16.7961 14.3717C16.7966 14.4816 16.7682 14.5897 16.7137 14.6851C16.6592 14.7805 16.5805 14.8599 16.4855 14.9151C16.3905 14.9704 16.2826 14.9997 16.1727 15H3.82645C3.71654 14.9997 3.60865 14.9704 3.51367 14.9151C3.41868 14.8598 3.33996 14.7805 3.28544 14.685C3.23092 14.5896 3.20253 14.4815 3.20313 14.3716C3.20374 14.2617 3.23332 14.1539 3.28889 14.059C3.80478 13.1716 4.39046 11.5479 4.39046 8.74995L4.39046 8.12495Z" stroke="white" stroke-linecap="round" stroke-linejoin="round" />
            <path d="M7.5 15V15.625C7.5 16.288 7.76339 16.9239 8.23223 17.3928C8.70107 17.8616 9.33696 18.125 10 18.125C10.663 18.125 11.2989 17.8616 11.7678 17.3928C12.2366 16.9239 12.5 16.288 12.5 15.625V15" stroke="white" stroke-linecap="round" stroke-linejoin="round" />
          </svg>
          <p v-if="!notificationsCount < 1" class="count">
            {{ notificationsCount }}
          </p>
        </div>
        <div class="user">
          <div class="user-image" @click="$router.push('/account')">
            <img src="~assets/images/user-image.png" alt="">
          </div>
          <p class="username" @click="$emit('openLogout')">
            {{ username }}
          </p>
          <img src="~assets/icons/Arrow - Down 2.svg" alt="" @click="$emit('openLogout')">
        </div>
      </div>
    </div>
    <div class="hamburger" @click="showMobileMenu">
      <span class="bar" />
      <span class="bar" />
      <span class="bar" />
    </div>
  </div>
</template>

<script>
import Cookies from 'js-cookie'
// import paystack from 'vue-paystack';
export default {
  components: {
    //   paystack
  },
  props: {
    activeTab: {
      type: String,
      default: () => ''
    }
  },
  data () {
    return {
      notificationsCount: '',
      // pageTitle: 'Dashboard'
      username: '',
      balance: '',
      challengersOnline: '0',
      newCampaignShow: false,
      campaignContactShow: false,
      paystackkey: 'pk_test_xxxxxxxxxxxxxxxxxxxxxxx', // paystack public key
      email: 'foobar@example.com', // Customer email
      amount: 1000000, // in kobo
      overviewData: []
    }
  },
  computed: {
    pageName () {
      const str = this.$route.name
      const splited = str.split('-')

      if (this.$route.name === 'index') {
        return 'Dashboard'
      }

      if (this.$route.name === `${splited[0]}-${splited[1]}`) {
        return `${splited[1]}`
      } else if (this.$route.name === `${splited[0]}-${splited[1]}-${splited[2]}`) {
        return `${splited[1]}`
      } else {
        return `${splited[0]}`
      }
    },
    reference () {
      let text = ''
      const possible = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789'

      for (let i = 0; i < 10; i++) { text += possible.charAt(Math.floor(Math.random() * possible.length)) }

      return text
    }
  },
  watch: {
    $route () {
      // this.getNotificationCount()
    }
  },
  created () {
    this.getBalance()
    this.getUserDetails()
  },
  methods: {
    getBalance () {
      this.$axios.$get('/get_balance', {
        headers: {
          Authorization: `Bearer ${Cookies.get('token')}`
        }
      }).then((response) => {
        this.loading = false
        // console.log(response)
        if (response.error && response.errorMsg === 'Authentication Failed') {
          this.$router.push('/login?error=session has expired')
        }
        this.balance = response.balance.balance
        this.$store.commit('setBalance', this.balance)
      })
    },
    getUserDetails () {
      this.$axios.$get('/get_user_details', {
        headers: {
          Authorization: `Bearer ${Cookies.get('token')}`
        }
      }).then((response) => {
        // console.log(response)
        this.userDetails = response.data
        this.username = this.capitalizeFirstLetter(this.userDetails.username)
        this.$store.commit('setUserDetails', this.userDetails)
      })
    },
    capitalizeFirstLetter (string) {
      return string.charAt(0).toUpperCase() + string.slice(1)
    },
    callback (response) {
      // console.log(response)
    },
    close () {
      // console.log("Payment closed")
    },
    showMobileMenu () {
      this.$emit('showMobileMenu')
    },
    handleNewCampaignShow () {
      this.newCampaignShow = true
    },
    handleNewCampaignClose () {
      this.newCampaignShow = false
    },
    handleContactsShow () {
      this.campaignContactShow = true
    },
    handleContactClose () {
      this.campaignContactShow = false
    },
    handleCampaignSubmit () {
      this.handleNewCampaignClose()
      this.handleContactsShow()
    },
    formatNaira (num) {
      return '₦' + num.toString().replace(/(\d)(?=(\d{3})+(?!\d))/g, '$1,')
    }
  }
}
</script>

<style scoped>
.header-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: fixed;
  height: 9vh;
  width: 82vw;
  background-color: #151C31;
  border-bottom: 1px solid rgba(226, 226, 234, 0.161);
  padding: 0 25px;
  z-index: 5;
}

.left-side {
  display: flex;
  align-items: center;
  flex-basis: 40%;
}

.mobile-logo {
  display: none;
}

.head-page-title {
  font-weight: 600;
  text-transform: capitalize;
}

.btn .green-btn {
  color: white;
  background-color: #3DD598;
  border: none;
  border-radius: 5px;
  font-size: 14px;
  width: 10rem;
  height: 50px;
  margin-left: 50px;
  padding: 0 10px;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
}

.btn .blue-btn {
  color: #0082FA;
  background-color: #CEE3FF;
  border: none;
  border-radius: 5px;
  font-size: 16px;
  font-weight: 600;
  width: 210px;
  height: 50px;
  margin-left: 50px;
  padding: 0 20px;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
}

.btn .green-btn img {
  margin-left: 10px;
}

.btn .blue-btn .plus {
  margin-left: 30px;
}

.right-side {
  flex-basis: 60%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.middle-section {
  display: flex;
  align-items: center;
}

.balance-box {
  /* border-right: 1px solid #E1EDFE; */
  width: 13rem;
  padding: 20px 30px;
}

.title {
  color: #1DA1F2;
  font-size: 13px;
  margin-bottom: 8px;
}

.price {
  font-weight: 500;
  font-size: 16px;
  color: #fff;
  overflow: hidden;
}

.topup-btn button {
  border: none;
  border-radius: 6px;
  color: #fff;
  width: 7rem;
  height: 40px;
  /* padding: 0.8rem 0; */
  background-color: #1DA1F2;
  margin: 0 40px;
  cursor: pointer;
  font-weight: 500;
}

.last-section {
  display: flex;
  align-items: center;
}

.notification {
  position: relative;
  margin-right: 20px;
  cursor: pointer;
  display: flex;
}

.count {
  position: absolute;
  font-size: 10px;
  font-weight: 600;
  top: -3px;
  left: 40%;
  border-radius: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 15px;
  height: 15px;
  color: #fff;
  background-color: #3DD598;
}

.username {
  font-size: 15px;
  margin-right: 10px;
  white-space: nowrap;
}

.user {
  width: fit-content;
  display: flex;
  align-items: center;
  cursor: pointer;
}

.user-image {
  margin-right: 10px;
}

.user-image img {
  width: 35px;
  height: 35px;
  border-radius: 50%;
}

.hamburger {
  display: none;
}

/* RESPONSIVENESS */

.bar {
  display: block;
  width: 25px;
  height: 2px;
  margin: 5px auto;
  background-color: #fff;
}

@media only screen and (max-width: 900px) {
.header-container {
  width: 100vw;
  padding: 15px 50px;
}

.mobile-logo {
  display: block;
}

.page-title {
  font-size: 18px;
  margin-left: 20px;
}

.mobile-logo img {
  width: 80px;
}

.hamburger {
    display: block;
    cursor: pointer;
    margin-left: 20px;
  }

.balance-box,
.username,
.topup-btn,
.user {
  display: none;
}

/* .header-container {
  width: 100%;
} */

}

@media only screen and (max-width: 500px) {
.header-container {
  height: 11vh;
  width: 100vw;
  padding: 15px;
}

.mobile-logo {
  display: block;
}

.btn .green-btn {
  font-size: 14px;
  width: 10rem;
  height: 40px;
  margin-left: 20px;
}

.btn .blue-btn {
  font-size: 14px;
  width: 8rem;
  height: 40px;
  margin-left: 20px;
}

.btn .blue-btn .plus {
  margin-left: 10px;
}

.mobile-logo img {
  width: 80px;
  margin-right: 10px;
}

.hamburger {
    display: block;
    cursor: pointer;
    margin-left: 10px;
  }

.balance-box,
.page-title,
.username,
.topup-btn,
.user {
  display: none;
}

/* .header-container {
  width: 100%;
} */

}
</style>
