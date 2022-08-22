<template>
  <div class="sidemenu-container">
    <div class="logo-box">
      <img src="~assets/images/medicon-logo.png" alt="logo">
    </div>
    <div class="menu-list">
      <div class="menu-dropdown">
        <div class="inner-menu">
          <NuxtLink to="/">
            <div class="inner">
              <div class="menu-icon">
                <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M2.25 12.375L9 16.3125L15.75 12.375" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M2.25 9L9 12.9375L15.75 9" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M2.25 5.625L9 9.5625L15.75 5.625L9 1.6875L2.25 5.625Z" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                </svg>
              </div>
              <p class="menu-header">
                Dashboard
              </p>
            </div>
          </NuxtLink>
        </div>
      </div>
      <div class="menu-dropdown">
        <div :class="verify" class="menu-header-box" @click="verify = !verify">
          <div class="inner">
            <div class="menu-icon">
              <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M4.4999 15.1875C4.42603 15.1875 4.35289 15.173 4.28464 15.1447C4.21639 15.1164 4.15438 15.075 4.10215 15.0228C4.04992 14.9705 4.00848 14.9085 3.98022 14.8403C3.95195 14.772 3.9374 14.6989 3.9374 14.625L3.93744 11.623C3.63736 11.7652 3.30621 11.8291 2.9748 11.8089C2.64338 11.7886 2.32247 11.6849 2.0419 11.5074C1.76133 11.3298 1.53023 11.0842 1.37009 10.7933C1.20995 10.5024 1.12598 10.1758 1.12598 9.84377C1.12598 9.51174 1.20995 9.1851 1.37009 8.89423C1.53023 8.60337 1.76133 8.35774 2.0419 8.18018C2.32247 8.00262 2.64338 7.8989 2.9748 7.87867C3.30621 7.85845 3.63736 7.92237 3.93744 8.06449L3.9374 5.06252C3.9374 4.98865 3.95195 4.91551 3.98022 4.84726C4.00849 4.77901 4.04992 4.717 4.10216 4.66477C4.15439 4.61253 4.2164 4.5711 4.28465 4.54283C4.35289 4.51456 4.42604 4.50002 4.49991 4.50002L7.78312 4.50005C7.641 4.19998 7.57708 3.86883 7.5973 3.53742C7.61753 3.206 7.72124 2.88509 7.8988 2.60452C8.07636 2.32395 8.322 2.09285 8.61286 1.93271C8.90372 1.77257 9.23036 1.6886 9.56239 1.6886C9.89442 1.6886 10.2211 1.77257 10.5119 1.93271C10.8028 2.09285 11.0484 2.32395 11.226 2.60452C11.4035 2.88509 11.5073 3.206 11.5275 3.53742C11.5477 3.86883 11.4838 4.19998 11.3417 4.50005L14.6249 4.50002C14.7741 4.50002 14.9171 4.55928 15.0226 4.66476C15.1281 4.77025 15.1874 4.91333 15.1874 5.06251L15.1874 8.06449C14.8873 7.92237 14.5562 7.85845 14.2248 7.87867C13.8934 7.8989 13.5724 8.00262 13.2919 8.18018C13.0113 8.35774 12.7802 8.60337 12.6201 8.89423C12.4599 9.1851 12.3759 9.51173 12.3759 9.84377C12.3759 10.1758 12.4599 10.5024 12.6201 10.7933C12.7802 11.0842 13.0113 11.3298 13.2919 11.5074C13.5724 11.6849 13.8934 11.7886 14.2248 11.8089C14.5562 11.8291 14.8873 11.7652 15.1874 11.623L15.1874 14.625C15.1874 14.7742 15.1281 14.9173 15.0226 15.0228C14.9171 15.1283 14.7741 15.1875 14.6249 15.1875L4.4999 15.1875Z" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" />
              </svg>
            </div>
            <p class="menu-header">
              Challenges
            </p>
          </div>
          <img v-if="!verify" src="~assets/icons/menu-arrow down.svg" alt="">
          <img v-else src="~assets/icons/menu-arrow up.svg" alt="">
        </div>
        <div v-if="verify" class="inner-menu">
          <NuxtLink to="/challenges/challenge-system">
            <div class="inner">
              <p class="menu-text">
                Challenge System
              </p>
            </div>
          </NuxtLink>
          <!-- <NuxtLink to="/challenges/brand-challenge">
            <div class="inner">
              <p class="menu-text">
                Brand Challenge
              </p>
            </div>
          </NuxtLink> -->
        </div>
      </div>
      <!-- <div class="menu-dropdown">
        <div class="inner-menu">
          <NuxtLink to="/weapon">
            <div class="inner">
              <div class="menu-icon">
                <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M13.5 2.8125H4.5C3.56802 2.8125 2.8125 3.56802 2.8125 4.5V13.5C2.8125 14.432 3.56802 15.1875 4.5 15.1875H13.5C14.432 15.1875 15.1875 14.432 15.1875 13.5V4.5C15.1875 3.56802 14.432 2.8125 13.5 2.8125Z" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M6.46875 6.75C6.93474 6.75 7.3125 6.37224 7.3125 5.90625C7.3125 5.44026 6.93474 5.0625 6.46875 5.0625C6.00276 5.0625 5.625 5.44026 5.625 5.90625C5.625 6.37224 6.00276 6.75 6.46875 6.75Z" fill="white" />
                  <path d="M11.5312 6.75C11.9972 6.75 12.375 6.37224 12.375 5.90625C12.375 5.44026 11.9972 5.0625 11.5312 5.0625C11.0653 5.0625 10.6875 5.44026 10.6875 5.90625C10.6875 6.37224 11.0653 6.75 11.5312 6.75Z" fill="white" />
                  <path d="M6.46875 9.84375C6.93474 9.84375 7.3125 9.46599 7.3125 9C7.3125 8.53401 6.93474 8.15625 6.46875 8.15625C6.00276 8.15625 5.625 8.53401 5.625 9C5.625 9.46599 6.00276 9.84375 6.46875 9.84375Z" fill="white" />
                  <path d="M11.5312 9.84375C11.9972 9.84375 12.375 9.46599 12.375 9C12.375 8.53401 11.9972 8.15625 11.5312 8.15625C11.0653 8.15625 10.6875 8.53401 10.6875 9C10.6875 9.46599 11.0653 9.84375 11.5312 9.84375Z" fill="white" />
                  <path d="M6.46875 12.9375C6.93474 12.9375 7.3125 12.5597 7.3125 12.0938C7.3125 11.6278 6.93474 11.25 6.46875 11.25C6.00276 11.25 5.625 11.6278 5.625 12.0938C5.625 12.5597 6.00276 12.9375 6.46875 12.9375Z" fill="white" />
                  <path d="M11.5312 12.9375C11.9972 12.9375 12.375 12.5597 12.375 12.0938C12.375 11.6278 11.9972 11.25 11.5312 11.25C11.0653 11.25 10.6875 11.6278 10.6875 12.0938C10.6875 12.5597 11.0653 12.9375 11.5312 12.9375Z" fill="white" />
                </svg>
              </div>
              <p class="menu-header">
                Weapon (Categories)
              </p>
            </div>
          </NuxtLink>
        </div>
      </div> -->
      <div class="menu-dropdown">
        <div class="inner-menu">
          <NuxtLink to="/fund-account">
            <div class="inner">
              <div class="menu-icon">
                <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M9 5.0625V6.1875" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M9 11.8125V12.9375" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M9 15.75C12.7279 15.75 15.75 12.7279 15.75 9C15.75 5.27208 12.7279 2.25 9 2.25C5.27208 2.25 2.25 5.27208 2.25 9C2.25 12.7279 5.27208 15.75 9 15.75Z" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M7.3125 11.8125H9.84375C10.2167 11.8125 10.5744 11.6643 10.8381 11.4006C11.1018 11.1369 11.25 10.7792 11.25 10.4062C11.25 10.0333 11.1018 9.6756 10.8381 9.41188C10.5744 9.14816 10.2167 9 9.84375 9H8.15625C7.78329 9 7.4256 8.85184 7.16188 8.58812C6.89816 8.3244 6.75 7.96671 6.75 7.59375C6.75 7.22079 6.89816 6.8631 7.16188 6.59938C7.4256 6.33566 7.78329 6.1875 8.15625 6.1875H10.6875" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                </svg>
              </div>
              <p class="menu-header">
                Fund Account
              </p>
            </div>
          </NuxtLink>
        </div>
      </div>
      <div class="menu-dropdown">
        <div class="inner-menu">
          <NuxtLink to="/transactions">
            <div class="inner">
              <div class="menu-icon">
                <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M15.75 3.9375H2.25C1.93934 3.9375 1.6875 4.18934 1.6875 4.5V13.5C1.6875 13.8107 1.93934 14.0625 2.25 14.0625H15.75C16.0607 14.0625 16.3125 13.8107 16.3125 13.5V4.5C16.3125 4.18934 16.0607 3.9375 15.75 3.9375Z" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M11.8125 11.8125H14.0625" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M8.4375 11.8125H9.5625" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M1.6875 6.80988H16.3125" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                </svg>
              </div>
              <p class="menu-header">
                Transactions
              </p>
            </div>
          </NuxtLink>
        </div>
      </div>
      <div class="menu-dropdown">
        <div class="inner-menu">
          <NuxtLink to="/withdraw">
            <div class="inner">
              <div class="menu-icon">
                <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M8.62474 1.81955L2.95372 2.95375L1.81952 8.62477C1.80136 8.71558 1.80589 8.80946 1.83273 8.89809C1.85956 8.98672 1.90787 9.06735 1.97335 9.13283L9.31768 16.4772C9.36992 16.5294 9.43192 16.5708 9.50017 16.5991C9.56842 16.6274 9.64156 16.6419 9.71543 16.6419C9.7893 16.6419 9.86244 16.6274 9.93069 16.5991C9.99894 16.5708 10.0609 16.5294 10.1132 16.4772L16.4771 10.1132C16.5294 10.061 16.5708 9.99897 16.5991 9.93072C16.6273 9.86247 16.6419 9.78933 16.6419 9.71546C16.6419 9.64159 16.6273 9.56845 16.5991 9.5002C16.5708 9.43196 16.5294 9.36995 16.4771 9.31771L9.1328 1.97338C9.06732 1.9079 8.98669 1.8596 8.89806 1.83276C8.80943 1.80593 8.71554 1.80139 8.62474 1.81955V1.81955Z" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M5.90625 6.75C6.37224 6.75 6.75 6.37224 6.75 5.90625C6.75 5.44026 6.37224 5.0625 5.90625 5.0625C5.44026 5.0625 5.0625 5.44026 5.0625 5.90625C5.0625 6.37224 5.44026 6.75 5.90625 6.75Z" fill="white" />
                </svg>
              </div>
              <p class="menu-header">
                Withdraw
              </p>
            </div>
          </NuxtLink>
        </div>
      </div>
      <div class="menu-dropdown">
        <div class="inner-menu">
          <NuxtLink to="/account">
            <div class="inner">
              <div class="menu-icon">
                <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M9 11.25C10.5533 11.25 11.8125 9.9908 11.8125 8.4375C11.8125 6.8842 10.5533 5.625 9 5.625C7.4467 5.625 6.1875 6.8842 6.1875 8.4375C6.1875 9.9908 7.4467 11.25 9 11.25Z" stroke="white" stroke-width="2" stroke-miterlimit="10" />
                  <path d="M4.48633 14.0185C4.91004 13.1854 5.55601 12.4859 6.35272 11.9973C7.14944 11.5086 8.06583 11.25 9.00045 11.25C9.93507 11.25 10.8515 11.5086 11.6482 11.9972C12.4449 12.4859 13.0909 13.1854 13.5146 14.0185" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M14.0625 5.0625C14.6838 5.0625 15.1875 4.55882 15.1875 3.9375C15.1875 3.31618 14.6838 2.8125 14.0625 2.8125C13.4412 2.8125 12.9375 3.31618 12.9375 3.9375C12.9375 4.55882 13.4412 5.0625 14.0625 5.0625Z" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M14.0625 2.8125V1.96875" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M13.0881 3.375L12.3574 2.95312" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M13.0881 4.5L12.3574 4.92188" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M14.0625 5.0625V5.90625" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M15.0371 4.5L15.7678 4.92188" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M15.0371 3.375L15.7678 2.95312" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                  <path d="M15.7021 8.19141C15.7341 8.45975 15.7501 8.72976 15.75 9C15.75 10.335 15.3541 11.6401 14.6124 12.7501C13.8707 13.8601 12.8165 14.7253 11.5831 15.2362C10.3497 15.7471 8.99252 15.8808 7.68314 15.6203C6.37377 15.3598 5.17104 14.717 4.22703 13.773C3.28303 12.829 2.64015 11.6262 2.3797 10.3169C2.11925 9.00749 2.25292 7.65029 2.76382 6.41689C3.27471 5.18349 4.13987 4.12928 5.2499 3.38758C6.35994 2.64588 7.66498 2.25 9 2.25C9.2112 2.25 9.41999 2.25956 9.62638 2.27868" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                </svg>
              </div>
              <p class="menu-header">
                Account
              </p>
            </div>
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      verify: false
    }
  }

}
</script>

<style scoped>
.sidemenu-container {
  width: 18vw;
  height: 100vh;
  background-color: #01081E;
  position: fixed;
}

.logo-box {
  /* background-color: white; */
  height: 11%;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 120px;
}

.logo-box img {
  width: 50%;
  /* margin: 6px 40px; */
}

.menu-list {
  margin-top: 7rem;
  padding: 54px 40px;
  height: 70%;
  overflow: auto;
  -ms-overflow-style: none;  /* IE and Edge */
  scrollbar-width: none;
  /* min-height: fit-content; */
  /* height: fit-content; */
}

.menu-list::-webkit-scrollbar {
  display: none;
}

.menu-dropdown {
  padding: 15px 0;
}

.menu-header-box {
  display: flex;
  align-items: center;
  margin-bottom: 15px;
  cursor: pointer;
  justify-content: space-between;
}

.menu-header {
  font-family: 'Rubik', sans-serif;
  color: #fff;
}

.inner {
  display: flex;
  padding: 16px 0;
  align-items: center;
  cursor: pointer;
}

.menu-icon {
  margin-right: 12px;
}

.inner:hover .menu-icon svg path,
.inner:hover .menu-header,
.inner:hover .menu-text {
  /* fill: #1da0f2; */
  stroke: #1DA1F2;
  color: #1DA1F2;
}

a.nuxt-link-exact-active .menu-icon svg path,
a.nuxt-link-exact-active .menu-header,
a.nuxt-link-exact-active .menu-text {
  /* fill: #1da0f2; */
  stroke: #1DA1F2;
  color: #1DA1F2;
}

.menu-text {
  font-family: 'Rubik', sans-serif;
  color: rgba(255, 255, 255, 0.666);
  /* opacity: 70%; */
  margin-left: 30px;
}

.collapse {
  border-top: 1px solid #d3d7ea7e;
  margin-top: 15px;
  padding-top: 20px;
}

@media only screen and (max-width: 500px) {
  .menu-text {
    display: none;
  }

  .menu-header {
    font-size: 14px;
    /* text-align: center; */
    margin: auto;
  }

  .menu-list {
    padding: 54px 15px;
  }
  .menu-icon {
    margin: auto;
  }

  .logo-box {
    background-color: white;
    height: 10%;
    display: flex;
    align-items: center;
  }

  .logo-box img {
    width: 60px;
    margin: auto;
  }
}
</style>
