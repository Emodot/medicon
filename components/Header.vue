<template>
  <div class="header-container">
    <div class="left-side">
      <div class="mobile-logo">
        <img src="~assets/images/medicon-logo.png" alt="">
      </div>
      <div class="search-ctn">
        <svg width="14" height="14" viewBox="0 0 14 14" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M11.2028 9.85162C11.1006 9.74942 11.0866 9.57302 11.165 9.45122C11.781 8.50342 12.1422 7.37502 12.1422 6.16262C12.1422 2.81382 9.4178 0.0908203 6.0718 0.0908203C2.723 0.0908203 0 2.81382 0 6.16262C0 9.51002 2.723 12.233 6.0718 12.233C7.3752 12.233 8.582 11.8144 9.5732 11.1116C9.6894 11.0276 9.8644 11.0388 9.9666 11.1396L12.1366 13.3096C12.1506 13.3236 12.166 13.3376 12.1814 13.3488C12.2066 13.3698 12.3116 13.4678 12.4124 13.57L12.67 13.8262C12.7722 13.927 12.9374 13.927 13.0382 13.8262L13.923 12.9414C14.0252 12.8392 14.0252 12.674 13.9244 12.5718L11.2028 9.85162ZM9.744 8.99062C9.5438 9.25102 9.3184 9.48902 9.0692 9.70042C8.26 10.3878 7.2142 10.805 6.0718 10.805C3.5112 10.805 1.428 8.72182 1.428 6.16262C1.428 3.60342 3.5112 1.51882 6.0718 1.51882C8.631 1.51882 10.7142 3.60202 10.7142 6.16262C10.7142 7.22662 10.3488 8.20662 9.744 8.99062Z" fill="#CACCCF" />
        </svg>
        <input type="search" name="" placeholder="Search">
      </div>
    </div>
    <div class="last-section">
      <div class="notification" @click="$emit('openNotification')">
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M20.2223 18.3815C20.1479 18.2135 20.1311 17.9687 20.1935 17.7959C20.6759 16.4279 21.1703 15.0671 21.6839 13.7087C22.2311 12.2663 22.6559 10.8143 22.4423 9.2375C22.1999 7.4471 21.4655 5.8967 20.1431 4.6727C19.4975 4.0775 18.7415 3.6095 17.9927 3.0527C18.0503 2.8943 18.1439 2.6471 18.2351 2.3999C18.3839 1.9919 18.2687 1.6727 17.9255 1.5455C17.5727 1.4159 17.2775 1.5623 17.1119 1.9583C17.0039 2.2127 16.9079 2.4695 16.8023 2.7335C15.8039 2.4887 14.8175 2.3903 13.8167 2.5343C10.8335 2.9615 8.6807 4.5263 7.5167 7.3175C6.8039 9.0335 6.2159 10.8023 5.5823 12.5495C5.5055 12.7655 5.3831 12.8927 5.1743 12.9863C4.1135 13.4615 3.0599 13.9511 1.9991 14.4335C1.7159 14.5607 1.5047 14.7407 1.5119 15.0767C1.5191 15.4247 1.7639 15.5639 2.0519 15.6671C4.0319 16.3775 6.0071 17.0951 7.9919 17.7911C8.2895 17.8967 8.3927 18.0143 8.3759 18.3431C8.2751 20.5463 10.3415 22.1879 12.4799 21.6287C13.3463 21.4031 14.0063 20.8967 14.5031 20.1431C14.6063 20.1791 14.6999 20.2127 14.7935 20.2439C16.8047 20.9639 18.8159 21.6839 20.8271 22.4087C21.1295 22.5167 21.4079 22.5623 21.6575 22.3055C21.9167 22.0367 21.8087 21.7607 21.6743 21.4775C21.1799 20.4527 20.6879 19.4231 20.2223 18.3815ZM11.1191 20.4599C10.1615 20.1839 9.5279 19.3247 9.5951 18.3455C10.8479 18.7919 12.0743 19.2311 13.3055 19.6703C12.9551 20.3423 11.9495 20.6999 11.1191 20.4599Z" fill="#CACCCF" />
        </svg>
        <p v-if="!notificationsCount < 1" class="count">
          {{ notificationsCount }}
        </p>
      </div>
      <div class="user">
        <div class="user-image" @click="$router.push('/settings')">
          <img src="~assets/images/user-image.png" alt="">
        </div>
        <p class="username" @click="$emit('openLogout')">
          {{ username }}
        </p>
        <svg width="8" height="6" viewBox="0 0 8 6" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M3.34025 5.70145C3.30642 5.66849 3.16175 5.54404 3.04275 5.42811C2.29433 4.74846 1.06933 2.97544 0.695417 2.04745C0.635333 1.90652 0.508167 1.55021 0.5 1.35984C0.5 1.17742 0.542 1.00353 0.627167 0.837596C0.746167 0.630744 0.933417 0.464808 1.1545 0.373884C1.30792 0.315352 1.767 0.224428 1.77517 0.224428C2.27742 0.133504 3.0935 0.0834961 3.99533 0.0834961C4.85458 0.0834961 5.63742 0.133504 6.14725 0.207948C6.15542 0.216472 6.72592 0.307396 6.92133 0.406844C7.27833 0.58926 7.5 0.945568 7.5 1.32688V1.35984C7.49125 1.60818 7.26958 2.13042 7.26142 2.13042C6.88692 3.0084 5.722 4.7405 4.94792 5.43664C4.94792 5.43664 4.749 5.63269 4.62475 5.71793C4.44625 5.85091 4.22517 5.91683 4.00408 5.91683C3.75733 5.91683 3.5275 5.84239 3.34025 5.70145Z" fill="#90BB6E" />
        </svg>
      </div>
      <div class="hamburger" @click="showMobileMenu">
        <span class="bar" />
        <span class="bar" />
        <span class="bar" />
      </div>
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
    }
  },
  watch: {
    $route () {
      // this.getNotificationCount()
    }
  },
  created () {
    this.getUserDetails()
  },
  methods: {
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
  height: 11vh;
  width: 83vw;
  background-color: #f2f5fb;
  border-bottom: 1px solid rgba(226, 226, 234, 0.161);
  padding: 0 25px;
  z-index: 5;
}

.left-side {
  display: flex;
  align-items: center;
  flex-basis: 40%;
}

.search-ctn {
  display: flex;
  align-items: center;
  padding: 0 15px;
  background-color: #fff;
  width: 23rem;
  height: 40px;
  border-radius: 100px;
}

.search-ctn input {
  margin-left: 12px;
  border: none;
  background-color: transparent;
  width: 100%;
  outline: none;
}

::placeholder {
  font-size: 13px;
  color: #A0A4A8;
}

.mobile-logo {
  display: none;
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
  background-color: rgb(33, 33, 33);
}

@media only screen and (max-width: 900px) {
.search-ctn {
  margin-left: 30px;
}
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
  width: 100px;
}

.notification {
  margin-right: 0;
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
