<template>
  <div class="modal-backdrop-2 come-down">
    <div class="modal-2">
      <div class="modal-icon">
        <img src="~assets/icons/settings.svg" alt="">
      </div>
      <h1 class="title">
        Reset Password
      </h1>
      <p class="sub-title">
        Enter the email associated with your account to reset your password
      </p>
      <div class="form">
        <div class="input-container">
          <p class="label">
            Email Address
          </p>
          <input v-model="email" type="email" name="email" placeholder="Enter Email Address">
        </div>
        <div class="btn">
          <button v-if="loading">
            <Loader />
          </button>
          <button v-else @click="forgotPassword()">
            Send Instructions
          </button>
        </div>
        <p class="text" @click="$emit('close-modal')">
          Cancel
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import Cookies from 'js-cookie'
export default {
  props: {
    actionData: {
      type: String,
      default: ''
    }
  },
  data () {
    return {
      email: '',
      loading: false
    }
  },
  methods: {
    forgotPassword () {
      this.loading = true
      this.$emit('sentInst', this.email)
      this.$axios.$post('/forgot_password', {
        email: this.email
      }, {
        headers: {
          Authorization: `Bearer ${Cookies.get('token')}`
        }
      }).then((response) => {
        console.log(response)
        if (!response.error) {
          this.$toast.success(response.statusText)
          this.$emit('sentInst', this.email)
        } else {
          this.$toast.error(response.errorMsg)
        }
      })
    }
  }
}
</script>

<style scoped>
* {
  color: #3F3F3F;
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
  color: #3F3F3F60;
}

.title {
  font-size: 24px;
  font-weight: 600;
  text-align: center;
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
  color: #3F3F3F;
  font-size: 14px;
  margin-bottom: 8px;
}

input {
  height: 50px;
  width: 100%;
  border-radius: 5px;
  border: 1px solid #3F3F3F60;
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
