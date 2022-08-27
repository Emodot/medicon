<template>
  <div class="modal-backdrop-2 reveal">
    <div class="modal-2">
      <div class="modal-icon">
        <img src="~assets/icons/check.svg" alt="">
      </div>
      <h1 v-if="page === 'account'" class="title">
        Email Verified!
      </h1>
      <h1 v-else class="title">
        Account Created!
      </h1>
      <p v-if="page === 'account'" class="sub-title">
        Your Email Address has been successfully Verified. Your can start taking Challenges
      </p>
      <p v-else class="sub-title">
        Please navigate to the Account page to complete your profile
      </p>
      <div class="form">
        <div class="btn">
          <button v-if="page === 'account'" @click="$router.push('/challenges/challenge-system')">
            Challenge System
          </button>
          <button v-else @click="$router.push('/account')">
            Account Page
          </button>
        </div>
        <!-- <p class="text" @click="$router.push('/')">
          Go Home
        </p> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    actionData: {
      type: String,
      default: ''
    },
    page: {
      type: String,
      default: ''
    }
  },
  data () {
    return {
      userEmail: 'acumen@mail.com'
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
  width: 80px;
}

::placeholder {
  font-size: 14px;
}

.title {
  font-size: 24px;
  font-weight: 600;
  text-align: center;
  margin-top: 30px;
}

.sub-title {
  font-size: 14px;
  text-align: center;
  width: 60%;
  margin: auto;
  margin-top: 20px;
}

.span-account {
  font-size: 14px;
  color: #1D692C;
  cursor: pointer;
  /* text-align: center;
  width: 60%;
  margin: auto;
  margin-top: 10px; */
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

.btn {
  display: flex;
  justify-content: center;
}

.btn button {
  width: 70%;
  height: 50px;
  background-color: #1da0f239;
  border: 2px solid #1D692C;
  color: #1D692C;
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
