<template>
  <div class="container">
    <div class="inner">
      <div class="lhs">
        <div class="logo">
          <img src="~assets/images/medicon-logo.png" alt="">
        </div>
        <p class="title">
          Sign Up
        </p>
        <p class="sub-title">
          Create an Account
        </p>
        <div class="form">
          <div class="input-box">
            <p class="label">
              Name
            </p>
            <input v-model="text" class="text-input" placeholder="Name" type="email">
          </div>
          <div class="input-box">
            <p class="label">
              Email Address
            </p>
            <input v-model="email" class="text-input" placeholder="Email Address" type="email">
          </div>
          <div class="input-box">
            <p class="label">
              Password
            </p>
            <input v-model="passowrd" class="text-input" placeholder="Password" type="email">
          </div>
          <label class="check-container">I agree to the Terms and Privacy
            <input class="check-input" type="checkbox" :checked="checked" @click="toogleCheck">
            <span class="checkmark" />
          </label>
          <button class="sign-in" @click="$emit('start-quiz')">
            <svg width="22" height="22" viewBox="0 0 22 22" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M9.45416 14.6094L13.0626 11L9.45416 7.39062" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
              <path d="M3.4375 11H13.06" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
              <path d="M13.0625 3.4375H17.875C18.0573 3.4375 18.2322 3.50993 18.3611 3.63886C18.4901 3.76779 18.5625 3.94266 18.5625 4.125V17.875C18.5625 18.0573 18.4901 18.2322 18.3611 18.3611C18.2322 18.4901 18.0573 18.5625 17.875 18.5625H13.0625" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
            </svg>
            <span class="btn-text">Sign Up</span>
          </button>
          <div class="bottom-text">
            <!-- <p class="forgot">
              Forgot Password?
            </p> -->
            <p class="no-account">
              Have an Account? <span class="sign-up" @click="$router.push('/login')">Sign In!</span>
            </p>
          </div>
        </div>
      </div>
      <div class="rhs" />
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      checked: false
    }
  },
  methods: {
    toogleCheck () {
      this.checked = !this.checked
    }
  }
}
</script>

<style scoped>
.inner {
  display: flex;
  height: 100vh;
}

.lhs {
  flex-basis: 35%;
  padding: 70px 70px;
}

.logo img {
  width: 35%;
}

.rhs {
  flex-basis: 65%;
  background-image: url('assets/images/login-bg.jpg');
  background-size: cover;
  background-position-y: bottom;
  height: 100vh;
}

.title {
  font-size: 38px;
  font-weight: 600;
  margin-top: 6rem;
}

.sub-title {
  margin-top: 20px;
}

.form {
  margin-top: 4rem;
}

.input-box {
  margin-bottom: 15px;
}

.label {
  font-size: 15px;
  font-weight: 500;
  color: #3F3F3F;
}

.text-input {
  border: 1px solid #3F3F3F60;
  background-color: transparent;
  outline: none;
  padding: 0 15px;
  width: 100%;
  height: 50px;
  margin-top: 7px;
  border-radius: 10px;
}

::placeholder {
  color: #3F3F3F60;
}

.check-ctn {
  display: flex;
}

.check-ctn p {
  margin-left: 10px;
}
/* The container */
.check-container {
  display: block;
  position: relative;
  padding-left: 25px;
  margin-bottom: 12px;
  margin-top: 10px;
  cursor: pointer;
  font-size: 16px;
  font-weight: 400;
  /* color: #758396; */
  line-height: 25px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

/* Hide the browser's default checkbox */
.check-container .check-input {
  position: absolute;
  opacity: 0;
  cursor: pointer;
  height: 0;
  width: 0;
}

/* Create a custom checkbox */
.checkmark {
  position: absolute;
  margin-top: 5px;
  top: 0;
  left: 0;
  height: 15px;
  width: 15px;
  background-color: #ccc;
  border-radius: 3px;
}

/* On mouse-over, add a grey background color */
.check-container:hover .check-input ~ .checkmark {
  background-color: #ccc;
}

/* When the checkbox is checked, add a background */
.check-container .check-input:checked ~ .checkmark {
  background-color: #1D692C;
}

/* Create the checkmark/indicator (hidden when not checked) */
.checkmark:after {
  content: "";
  position: absolute;
  display: none;
}

/* Show the checkmark when checked */
.check-container .check-input:checked ~ .checkmark:after {
  display: block;
}

/* Style the checkmark/indicator */
.check-container .checkmark:after {
  left: 5px;
  top: 2px;
  width: 5px;
  height: 10px;
  border: 1px solid white;
  border-width: 0 3px 3px 0;
  -webkit-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  transform: rotate(45deg);
}

.sign-in {
  border: none;
  background-color: #1D692C;
  height: 45px;
  width: 7rem;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 5px;
  margin-top: 2rem;
  cursor: pointer;
}

.btn-text {
  color: #fff;
  margin-left: 10px;
}

.bottom-text {
  margin-top: 7rem;
}

.forgot {
  color: #1D692C;
  cursor: pointer;
}

.no-account {
  margin-top: 10px;
}

.sign-up {
  color: #1D692C;
  cursor: pointer;
}

@media only screen and (max-width: 500px) {

  .logo img {
  width: 45%;
}
  .rhs {
    display: none;
  }

  .lhs {
    flex-basis: 100%;
    padding: 20px 30px;
  }

  .title {
    margin-top: 3rem;
  }

  .form {
    margin-top: 2rem;
  }

  .bottom-text {
    margin-top: 3rem;
  }

  .no-account {
    padding-bottom: 3rem;
  }
}

</style>
