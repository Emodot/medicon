<template>
  <div class="mobile-menu">
    <div class="mobile-header">
      <div class="logo">
        <img src="~assets/images/medicon-logo.png" alt="logo">
      </div>

      <div class="close" @click="closeMobileMenu">
        <span class="bar" />
        <span class="bar2" />
      </div>
    </div>
    <div class="menu-container">
      <nuxt-link to="/">
        Dashboard
      </nuxt-link>
      <nuxt-link to="/profile-data">
        Profile Data
      </nuxt-link>
      <nuxt-link to="/subscription">
        Subscription
      </nuxt-link>
      <nuxt-link to="/transactions">
        Transactions
      </nuxt-link>
      <nuxt-link to="/settings">
        Settings
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    closeMobileMenu () {
      this.$emit('closeMobileMenu')
    }
  }
}
</script>

<style scoped>
/* MOBILE HEADER  */

.mobile-menu {
  z-index: 3;
  background-color: white;
  position: fixed;
  width: 100%;
}

.mobile-header {
  height: 80px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  padding: 0 30px;
}

.logo img {
  width: 5rem;
}

.middle-section {
  display: flex;
  align-items: center;
  padding: 20px 50px;
}

.close {
  color: rgba(0, 0, 0, 0.22);
  cursor: pointer;
}

.bar,
.bar2 {
  display: block;
  width: 25px;
  height: 2px;
  margin: 5px auto;
  background-color: #101010;
}

.bar {
  transform: rotate(45deg);
  position: absolute;
}

.bar2 {
  transform: rotate(-45deg);
}

.menu-container {
  display: flex;
  flex-direction: column;
  font-size: 16px;
  width: 100%;
}

a {
  padding: 20px 20px;
  font-size: 14px;
  color: black;
  border: 1px solid rgba(0, 0, 0, 0.068);
}
</style>
