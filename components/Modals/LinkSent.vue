<template>
  <div class="modal-backdrop-2">
    <div class="modal-2">
      <div class="modal-icon">
        <img src="~assets/icons/plane.svg" alt="">
      </div>
      <h1 class="title">
        Link Sent
      </h1>
      <p class="sub-title">
        We have sent a link to <span class="user-email">{{ userEmail }}</span> for your account recovery
      </p>
      <div class="form">
        <div class="btn">
          <button @click="$emit('set-password')">
            Set New Password
          </button>
        </div>
        <!-- <p class="text">
          Cancel
        </p> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    userEmail: {
      type: String,
      default: ''
    }
  },
  data () {
    return {
      // userEmail: ''
    }
  }
}
</script>

<style scoped>
* {
  /* font-family: 'Poppins', sans-serif; */
  color: #474680;
}
.modal-backdrop-2 {
  z-index: 7;
  position: fixed;
  overflow: auto;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(24, 18, 46, 0.8);
}

.modal-2 {
  /* margin-top: 5%; */
  background-color: white;
  width: 32%;
  height: fit-content;
  align-items: center;
  border-radius: 20px;
  overflow-y: auto;
  padding-bottom: 50px;
}

.modal-icon {
  text-align: center;
  margin-top: 40px;
  margin-bottom: 20px;
}

.modal-icon img {
  width: 60px;
}

::placeholder {
  font-size: 14px;
  color: #47468060;
}

.title {
  font-size: 24px;
  font-weight: 600;
  text-align: center;
}

.user-email {
  font-weight: 600;
}

.sub-title {
  font-size: 14px;
  text-align: center;
  width: 60%;
  margin: auto;
  margin-top: 10px;
}

.form {
  width: 75%;
  margin: auto;
  margin-top: 30px;
}

.input-container {
  margin-bottom: 20px;
}

.label {
  color: #474680;
  font-size: 14px;
  margin-bottom: 8px;
}

input {
  height: 50px;
  width: 100%;
  border-radius: 5px;
  border: 1px solid #47468060;
  padding: 0 20px;
  outline: none;
}

.btn button {
  width: 100%;
  height: 50px;
  background-color: #1D692C;
  color: #fff;
  border: none;
  outline: none;
  cursor: pointer;
  border-radius: 5px;
  margin-top: 20px;
}

.text {
  margin-top: 20px;
  text-align: center;
  font-size: 14px;
  cursor: pointer;
}

@media only screen and (max-width: 900px) {
  .modal-2 {
    width: 70%;
  }
}

@media only screen and (max-width: 500px) {

  .modal-2 {
    width: 90%;
    padding: 30px;
    /* padding-top: 50px; */
    margin-top: 1rem;
  }

  .modal-icon {
    margin-top: 0;
  }

  .title {
    font-size: 20px;
  }

  .sub-title {
    font-size: 14px;
    width: 100%;
  }

  .form {
    width: 100%;
  }

  .label {
    font-size: 12px;
  }

  ::placeholder {
    font-size: 12px;
  }

  .text {
    font-size: 12px;
  }

  .btn button {
    font-size: 14px;
  }

}

</style>
