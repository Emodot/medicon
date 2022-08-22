<template>
  <div class="main">
    <!-- <vue-internet-checker
      @status="status"
      @event="event"
    /> -->
    <div class="sidemenu">
      <SideMenu />
    </div>
    <div>
      <div class="header-content">
        <Header
          v-show="!showMobileMenu"
          @showMobileMenu="showMobileMenu = true"
          @openNotification="openNotification = true"
          @openLogout="openLogout = true"
        />
      </div>
      <div class="mobile-menu">
        <MobileMenu
          v-show="showMobileMenu"
          @closeMobileMenu="showMobileMenu = false"
        />
      </div>
      <div class="main-content">
        <Nuxt />
        <Logout
          v-if="openLogout"
          @close-logout="openLogout = false"
        />
        <Notification
          v-if="openNotification"
          @close-notification="openNotification = false"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Cookies from 'js-cookie'
// import vueInternetChecker from 'vue-internet-checker'
import Logout from '~/components/Modals/Logout.vue'
import Notification from '~/components/Modals/Notification.vue'
export default {
  name: 'MainLayout',
  components: {
    Logout,
    Notification
    // vueInternetChecker
  },
  data () {
    return {
      showMobileMenu: false,
      addNewContact: false,
      openNotification: false,
      openLogout: false,
      trigger: false,
      onLine: null
    }
  },
  watch: {
    $route () {
      this.showMobileMenu = false
      this.checkLoggedIn()
      // this.checkInternet()
    }
  },
  created () {
    // this.checkLoggedIn()
    // this.checkInternet()
  },
  methods: {
    checkLoggedIn () {
      if (Cookies.get('token') === undefined) {
        this.$router.push('/login?error=session has expired')
      } else {
        this.getUserDetails()
      }
    },
    getUserDetails () {
      this.$axios.$get('/get_user_details', {
        headers: {
          Authorization: `Bearer ${Cookies.get('token')}`
        }
      }).then((response) => {
        // console.log(response)
        if (response.error && response.errorMsg === 'Authentication Failed') {
          this.$router.push('/login?error=session has expired')
        }
      })
    }
    // status (ele) {
    //   console.log(ele)
    //   this.onLine = ele
    // },
    // event (ele) {
    //   console.log(ele)
    // }

    // checkInternet () {
    //   if (navigator.onLine) {
    //     this.connectionStatus = 'Connected to internet.'
    //   } else {
    //     this.connectionStatus = 'Unable to connect to internet.'
    //   }
    //   console.log(this.connectionStatus)
    // }
  }
}
</script>

<style>
html {
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.main {
  display: flex;
}

.header-content {
  margin-left: 18vw;
  z-index: 2;
}

.main-content {
  margin-top: 9vh;
  margin-left: 18vw;
  width: 82vw;
}

.add-new-contact {
  z-index: 3;
}

@media only screen and (max-width: 900px) {
  .main-content {
    padding: 0;
    margin-left: 0;
    width: 100vw;
  }

  .sidemenu {
    display: none;
  }

  .header-content {
    margin-left: 0;
  }
}

@media only screen and (max-width: 500px) {
.main-content {
  padding: 0;
  margin-left: 0;
  width: 100vw;
}

.sidemenu {
  display: none;
}

.header-content {
  margin-left: 0;
}

}
</style>
