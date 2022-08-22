<template>
  <div class="modal-backdrop come-down" @click="$emit('close-logout')">
    <div @click.stop>
      <button class="logout" @click="logOut()">
        <p>LOG OUT</p>
      </button>
    </div>
  </div>
</template>

<script>
// import Cookies from 'js-cookie'
export default {
  data () {
    return {

    }
  },
  methods: {
    logOut () {
      // Cookies.remove('token')
      // Cookies.remove('first_name')
      // Cookies.remove('last_name')
      // Cookies.remove('email')
      // Cookies.remove('id')
      // Cookies.remove('emailVerified')
      this.$router.push('/login')
      this.$toast.show('Logged Out')
      // this.$router.push('/login')
    }
  }

}
</script>

<style scped>
.modal-backdrop {
  z-index: 7;
  position: fixed;
  overflow: auto;
  height: 100%;
  display: flex;
  justify-content: right;
  /* align-items: center; */
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(24, 18, 46, 0.096);
}

.logout {
  margin-right: 20px;
  margin-top: 5rem;
  background-color: #fff;
  width: 7rem;
  height: 40px;
  border: none;
  border-radius: 7px;
  cursor: pointer;
}

.logout p {
  color: #162838;
  font-weight: 600;
}
</style>
