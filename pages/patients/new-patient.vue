<template>
  <div class="container">
    <div class="back" @click="$router.go(-1)">
      <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path opacity="0.4" d="M12.0001 22.0002C6.48509 22.0002 2.00009 17.5142 2.00009 12.0002C2.00009 6.48621 6.48509 2.00021 12.0001 2.00021C17.5141 2.00021 22.0001 6.48621 22.0001 12.0002C22.0001 17.5142 17.5141 22.0002 12.0001 22.0002Z" fill="#3F3F3F" />
        <path d="M13.4425 16.2209C13.2515 16.2209 13.0595 16.1479 12.9135 16.0019L9.42649 12.5319C9.28549 12.3909 9.20649 12.1999 9.20649 11.9999C9.20649 11.8009 9.28549 11.6099 9.42649 11.4689L12.9135 7.99692C13.2065 7.70492 13.6805 7.70492 13.9735 7.99892C14.2655 8.29292 14.2645 8.76792 13.9715 9.05992L11.0185 11.9999L13.9715 14.9399C14.2645 15.2319 14.2655 15.7059 13.9735 15.9999C13.8275 16.1479 13.6345 16.2209 13.4425 16.2209Z" fill="#3F3F3F" fill-opacity="0.5" />
      </svg>
      <p>Back</p>
    </div>
    <div class="inner">
      <div class="ctn">
        <div class="row">
          <div class="input-ctn">
            <p class="label">
              First Name
            </p>
            <input v-model="first_name" type="text" class="input" placeholder="First Name">
          </div>
          <div class="input-ctn">
            <p class="label">
              Middle Name
            </p>
            <input v-model="middle_name" type="text" class="input" placeholder="Middle Name">
          </div>
          <div class="input-ctn">
            <p class="label">
              Last Name
            </p>
            <input v-model="last_name" type="text" class="input" placeholder="Last Name">
          </div>
        </div>
        <div class="row">
          <div class="input-ctn">
            <p class="label">
              Email Address
            </p>
            <input v-model="email" type="text" class="input" placeholder="Email Address">
          </div>
          <div class="input-ctn">
            <p class="label">
              Phone Number
            </p>
            <input v-model="phone" type="text" class="input" placeholder="Phone Number">
          </div>
          <div class="input-ctn">
            <p class="label">
              Date of Birth
            </p>
            <input v-model="dob" type="date" class="input" placeholder="Date of Birth">
          </div>
        </div>
        <div class="row">
          <div class="input-ctn">
            <p class="label">
              Age
            </p>
            <input v-model="age" type="text" class="input" placeholder="Age">
          </div>
          <div class="input-ctn">
            <p class="label">
              Residential Address
            </p>
            <input v-model="residence_address" type="text" class="input" placeholder="Residential Address">
          </div>
          <div class="input-ctn">
            <p class="label">
              Gender
            </p>
            <div class="form-select">
              <select v-model="gender" required>
                <option value="">
                  Please Select
                </option>
                <option value="nigerian">
                  Male
                </option>
                <option value="abuja">
                  Female
                </option>
              </select>
              <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M14.625 6.75L9 12.375L3.375 6.75" stroke="#3F3F3F60" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
              </svg>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="input-ctn">
            <p class="label">
              Next of Kin
            </p>
            <input v-model="next_of_kin" type="text" class="input" placeholder="Next of Kin">
          </div>
          <div class="input-ctn">
            <p class="label">
              Next of Kin Phone Number
            </p>
            <input v-model="next_of_kin_phone" type="text" class="input" placeholder="Next of Kin Phone Number">
          </div>
          <div class="input-ctn">
            <p class="label">
              Next of Kin Address
            </p>
            <input v-model="next_of_kin_address" type="text" class="input" placeholder="Next of Kin Address">
          </div>
        </div>
        <div class="bottom-btn">
          <button>Save &amp; Continue</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'MainLayout',
  data () {
    return {
      first_name: '',
      last_name: '',
      middle_name: '',
      email: '',
      phone: '',
      dob: '',
      gender: '',
      next_of_kin_address: '',
      next_of_kin_phone: '',
      next_of_kin: '',
      residence_address: '',
      age: ''
    }
  }
}
</script>

<style scoped>
.container {
  padding: 30px;
}

.inner {
  background-color: #fff;
  padding: 30px;
  border-radius: 20px;
  width: 90%;
}

.back {
  display: flex;
  align-items: center;
  margin-bottom: 30px;
}

.back svg {
  margin-right: 7px;
}

.back p {
  color: #3F3F3F;
}
.row {
  display: flex;
  justify-content: space-between;
  width: 100%;
  margin-bottom: 35px;
}

.input-ctn {
  flex-basis: 30%;
}

.label {
  color: #3F3F3F;
  margin-bottom: 13px;
  font-size: 14px;
}

.input {
  height: 50px;
  width: 100%;
  border: 1px solid #3F3F3F60;
  outline: none;
  border-radius: 3px;
  padding: 0 15px;
}

::placeholder {
  font-size: 14px;
  color: #3F3F3F60;
}

.form-select {
  position: relative;
}
.form-select select {
  display: block;
  border: 1px solid #3F3F3F60;
  border-radius: 3px;
  display: flex;
  justify-content: space-between;
  height: 50px;
  color: #3F3F3F;
  padding: 0 16px;
  width: 100%;
  appearance: none;
  -moz-appearance: none;
  -webkit-appearance: none;
  margin-top: 10px;
  margin-bottom: 10px;
  outline: none;
  font-size: 14px;
}
.form-select svg {
  position: absolute;
  top: 15px;
  left: 90%;
}

.bottom-btn {
  display: flex;
  justify-content: center;
  margin-top: 5rem;
}

.bottom-btn button {
  border: none;
  background-color: #1D692C;
  height: 50px;
  width: 12rem;
  font-size: 14px;
  color: #fff;
  outline: none;
  border-radius: 20px;
  cursor: pointer;
}

@media screen and (max-width: 600px) {
  .row {
    flex-direction: column;
    margin-bottom: 0;
  }

  .input-ctn {
    margin-bottom: 20px;
  }

  .bottom-btn {
    margin-top: 2rem;
  }
}
</style>
