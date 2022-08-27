<template>
  <div class="modal-backdrop-2">
    <div class="modal-2">
      <div class="modal-icon">
        <svg width="34" height="34" viewBox="0 0 34 34" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M4.95835 12.75H7.08335V9.91664C7.08335 4.44855 11.5318 0 17 0C22.4682 0 26.9166 4.44855 26.9166 9.91664V12.75H29.0416C29.4332 12.75 29.75 13.0668 29.75 13.4584V31.1667C29.75 32.7293 28.4793 34 26.9166 34H7.08329C5.52068 34 4.25 32.7293 4.25 31.1666V13.4584C4.25 13.0668 4.56682 12.75 4.95835 12.75ZM14.8791 27.5468C14.857 27.7467 14.9213 27.9473 15.0555 28.0975C15.1897 28.2476 15.382 28.3334 15.5833 28.3334H18.4166C18.6179 28.3334 18.8102 28.2476 18.9444 28.0975C19.0786 27.9474 19.143 27.7468 19.1208 27.5468L18.674 23.5286C19.3996 23.0008 19.8333 22.1659 19.8333 21.25C19.8333 19.6874 18.5626 18.4166 16.9999 18.4166C15.4373 18.4166 14.1666 19.6873 14.1666 21.25C14.1666 22.1659 14.6003 23.0008 15.3259 23.5286L14.8791 27.5468ZM11.3334 12.75H22.6666V9.91664C22.6666 6.7921 20.1245 4.25 17 4.25C13.8755 4.25 11.3334 6.7921 11.3334 9.91664V12.75V12.75Z" fill="#474680" />
        </svg>
      </div>
      <h1 class="title">
        Create new Password
      </h1>
      <p class="sub-title">
        Your new password must be different from previous used passwords.
      </p>
      <div class="form">
        <div class="input-container">
          <p class="label">
            Enter OTP
          </p>
          <div class="password-input">
            <input v-model="code" class="pass-input" type="number" placeholder="Enter OTP">
            <!-- <p class="show-hide" @click="showHide()">
              {{ show_hide }}
            </p> -->
          </div>
        </div>
        <div class="input-container">
          <p class="label">
            Password
          </p>
          <div class="password-input">
            <input v-model="password" class="pass-input" :type="type" placeholder="Enter Password">
            <p class="show-hide" @click="showHide()">
              {{ show_hide }}
            </p>
          </div>
        </div>
        <div class="btn">
          <button v-if="loading">
            <Loader />
          </button>
          <button v-else @click="resetPassword()">
            Reset password
          </button>
        </div>
        <!-- <p class="text" @click="$emit('close-modal')">
          Cancel
        </p> -->
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
      code: '',
      loading: false,
      type: 'password',
      show_hide: 'show',
      password: ''
    }
  },
  methods: {
    showHide () {
      if (this.type === 'password') {
        this.type = 'text'
        this.show_hide = 'hide'
      } else if (this.type === 'text') {
        this.type = 'password'
        this.show_hide = 'show'
      }
    },
    resetPassword () {
      this.loading = true
      this.$router.push('/')
      this.$axios.$post('/reset_password', {
        resetCode: this.code,
        newpassword: this.password
      }, {
        headers: {
          Authorization: `Bearer ${Cookies.get('token')}`
        }
      }).then((response) => {
        // console.log(response)
        if (!response.error) {
          this.$toast.success(response.statusText)
          this.window.location.reload()
        } else {
          this.$toast.error(response.errorMsg)
        }
        // this.$emit('sentInst')
      })
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

.password-input input {
  border: none;
  /* position: relative; */
  /* bottom: 10px; */
  padding: 0;
  width: 100%;
  height: 20px;
  font-size: 15px;
  outline: none;
  /* padding: 0 20px; */
}

.password-input {
  display: flex;
  align-items: center;
  border: 1px solid #47468060;
  border-radius: 5px;
  width: 100%;
  height: 50px;
  outline: none;
  padding: 0 20px;
  margin-top: 10px;
}

.show-hide {
  opacity: 0.5;
  cursor: pointer;
  font-size: 14px;
}

.btn button {
  width: 100%;
  height: 50px;
  background-color: #90BB6E;
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
