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
      <nuxt-link to="/appointments">
        Appointments
      </nuxt-link>
      <nuxt-link to="/doctors">
        Doctors
      </nuxt-link>
      <nuxt-link to="/patients">
        Patients
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
  padding-top: 25px;
}

.mobile-header {
  height: 80px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  padding: 0 50px;
}

.logo img {
  width: 100px;
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
