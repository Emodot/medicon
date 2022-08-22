<template>
  <div class="main">
    <div>
      <div class="header-content">
        <Header
          v-show="!showMobileMenu"
          @showMobileMenu="showMobileMenu = true"
          @openNotification="openNotification = true"
          @openLogout="openLogout = true"
        />
      </div>
      <div class="mobile-menu come-down">
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
        <!-- <Notification
          v-if="openNotification"
          @close-notification="openNotification = false"
        /> -->
      </div>
    </div>
  </div>
</template>

<script>
// import Cookies from 'js-cookie'
import Logout from '~/components/Modals/Logout.vue'
// import Notification from '~/components/Modals/Notification.vue'
export default {
  name: 'MainLayout',
  components: {
    Logout
    // Notification
  },
  data () {
    return {
      showMobileMenu: false,
      addNewContact: false,
      openNotification: false,
      openLogout: false
    }
  },
  watch: {
    $route () {
      this.showMobileMenu = false
      // this.checkLoggedIn()
    }
  },
  created () {
    // this.checkLoggedIn()
  },
  methods: {
    // checkLoggedIn () {
    //   if (Cookies.get('token') === undefined) {
    //     this.$router.push('/login?error=session has expired')
    //   } else {
    //     this.getUserDetails()
    //   }
    // },
    // getUserDetails () {
    //   this.$axios.$get('/get_user_details', {
    //     headers: {
    //       Authorization: `Bearer ${Cookies.get('token')}`
    //     }
    //   }).then((response) => {
    //     // console.log(response)
    //     if (response.error && response.errorMsg === 'Authentication Failed') {
    //       this.$router.push('/login?error=session has expired')
    //     }
    //   })
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
  z-index: 2;
}

.main-content {
  margin-top: 100px;
  /* margin-left: 18vw; */
  width: 100vw;
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
