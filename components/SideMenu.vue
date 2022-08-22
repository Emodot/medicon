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
                <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M7.2192 2.20659C3.7856 2.20659 1 4.99059 1 8.42579C1 11.861 3.784 14.6466 7.2192 14.6466C10.6544 14.6466 13.4384 11.8626 13.4384 8.42579H7.2192V2.20659V2.20659ZM15 7.71379C15 5.99699 14.304 4.44179 13.1792 3.31699L8.7808 7.71379H15ZM8.0064 1.35059V7.56819L12.4032 3.17139C11.1888 1.95699 9.5968 1.35059 8.0064 1.35059V1.35059Z" fill="#90BB6E" />
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
        <div class="inner-menu">
          <NuxtLink to="/appointments">
            <div class="inner">
              <div class="menu-icon">
                <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <g clip-path="url(#clip0_150_5890)">
                    <path d="M15.6463 6.79995C15.0799 6.35355 14.0223 6.73435 13.1983 7.64955C12.4287 7.43515 11.7455 7.48795 11.1631 7.81595C10.0479 8.44475 9.62553 9.89115 9.46873 10.9903C9.44473 11.1599 9.42234 11.3327 9.39834 11.5055C9.14874 13.4079 8.91193 15.2063 6.65593 15.2063C6.61913 15.2063 6.58233 15.2063 6.54393 15.2047C5.90393 15.1887 5.44313 14.9903 5.13593 14.5967C4.56953 13.8703 4.66713 12.6831 4.73913 12.1903C4.96313 12.0895 5.12153 11.8687 5.12953 11.6079L5.16313 10.6335L6.35833 10.2783C6.50713 10.2335 6.62233 10.1391 6.70553 10.0223C6.91993 10.0703 7.18713 10.0591 7.37593 9.94075C7.70713 9.73435 8.19033 9.33755 8.79193 8.58715C9.44953 7.76635 9.61114 7.10555 9.62714 6.67675C9.63514 6.37115 9.42234 6.06075 9.26394 5.97435C9.10554 5.88795 9.07674 6.04955 9.10714 6.35355C9.15194 6.81115 9.07993 7.50715 8.48953 8.26395C8.47833 8.27675 8.46874 8.28635 8.45914 8.29915L8.46393 8.26555C8.60473 8.04795 8.72634 7.81915 8.81914 7.57435C9.77914 5.03195 7.70393 2.06555 7.61433 1.94075C7.59513 1.91355 7.56953 1.89595 7.54393 1.87515C7.60313 1.73915 7.58873 1.61595 7.48953 1.55195C7.33433 1.45115 7.09113 1.14875 6.95033 0.876747L6.70073 0.399947C6.56153 0.129547 6.26713 0.0815474 6.04633 0.292747L5.42713 0.894348C5.20473 1.10555 5.24793 1.39195 5.51833 1.53435L5.95513 1.75835C6.22553 1.90075 6.52153 2.15675 6.61753 2.33115C6.68953 2.46075 6.85593 2.47995 7.02713 2.39195C7.20313 2.64795 8.91193 5.24155 8.12793 7.31675C8.09593 7.40155 8.04633 7.47995 8.00473 7.56155L7.99993 7.56315C7.95193 7.55195 7.90553 7.53435 7.85593 7.53435C7.73273 7.53435 7.61753 7.57115 7.52153 7.63195L7.66713 7.77115C7.57913 7.87835 7.51993 8.00955 7.51993 8.15835C7.51993 8.19515 7.52793 8.23035 7.53433 8.26555C7.25913 8.56635 6.91513 8.83515 6.49913 9.06395C6.34553 8.97755 6.15993 8.95035 5.97913 9.00475L4.52313 9.43675L2.96473 8.94395C2.78713 8.88795 2.60153 8.91195 2.44953 8.99515C1.70713 8.55515 1.20153 7.99355 0.943934 7.31675C0.123134 5.14235 2.04153 2.39675 2.06073 2.36955C2.06233 2.36475 2.06233 2.35995 2.06713 2.35515C2.06713 2.35515 2.11193 2.39835 2.16793 2.44795C2.22393 2.50075 2.34553 2.40155 2.44153 2.22715C2.53593 2.05115 2.83513 1.79515 3.10553 1.65435L3.54073 1.42875C3.81273 1.28795 3.85433 1.00155 3.63353 0.788747L3.01273 0.188747C2.79193 -0.0240526 2.50073 0.0239474 2.35833 0.295947L2.11033 0.772747C1.96793 1.04475 1.72633 1.34555 1.57113 1.44795C1.41273 1.54715 1.34393 1.68315 1.41273 1.74715L1.53913 1.86555C1.50873 1.88635 1.48153 1.90875 1.45753 1.94075C1.36793 2.06555 -0.707266 5.03195 0.252734 7.57435C0.575934 8.42555 1.19673 9.11835 2.10553 9.64635C2.12953 9.90075 2.30393 10.1279 2.56313 10.2111L3.83513 10.6127L3.80153 11.5615C3.79673 11.7583 3.87833 11.9375 4.00953 12.0655C3.92153 12.6527 3.80473 14.0895 4.55193 15.0479C4.99833 15.6207 5.66233 15.9215 6.52633 15.9423C6.57273 15.9455 6.61753 15.9455 6.66233 15.9455C9.55993 15.9455 9.87674 13.5407 10.1311 11.6031C10.1535 11.4335 10.1759 11.2639 10.1999 11.0959C10.3887 9.77275 10.8591 8.83675 11.5263 8.46075C11.8607 8.27035 12.2623 8.21755 12.7199 8.29755C12.1455 9.24635 12.0735 10.2367 12.5967 10.6527C13.2031 11.1327 14.3775 10.6591 15.2191 9.59515C16.0607 8.53115 16.2511 7.27995 15.6463 6.79995ZM8.35353 8.42555C8.30393 8.48475 8.25434 8.54875 8.20634 8.60315C8.25434 8.54235 8.30234 8.48155 8.34714 8.41915L8.35353 8.42555ZM14.1375 8.71515C13.8223 9.11515 13.3823 9.29275 13.1551 9.11195C12.9887 8.98075 12.9839 8.69435 13.1151 8.39355C13.2351 8.43195 13.3567 8.47355 13.4815 8.52635C13.6719 8.60635 13.8863 8.51995 13.9663 8.33115C14.0463 8.14395 13.9583 7.92635 13.7695 7.84635C13.7135 7.82235 13.6607 7.80475 13.6047 7.78555C13.8623 7.59675 14.1327 7.53915 14.2943 7.66875C14.5231 7.84955 14.4511 8.31835 14.1375 8.71515Z" fill="#82888D" />
                  </g>
                  <defs>
                    <clipPath id="clip0_150_5890">
                      <rect width="16" height="16" fill="white" />
                    </clipPath>
                  </defs>
                </svg>
              </div>
              <p class="menu-header">
                Appointments
              </p>
            </div>
          </NuxtLink>
        </div>
      </div>
      <!-- <div class="menu-dropdown">
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
          <NuxtLink to="/challenges/brand-challenge">
            <div class="inner">
              <p class="menu-text">
                Brand Challenge
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
  width: 17vw;
  height: 100vh;
  background-color: #fff;
  position: fixed;
}

.logo-box {
  /* background-color: white; */
  height: 11vh;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  padding-left: 40px;
}

.logo-box img {
  width: 50%;
  /* margin: 6px 40px; */
}

.menu-list {
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
  font-weight: 700;
  color: #82888D;
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
  fill: #90BB6E;
  /* stroke: #90BB6E; */
  color: #90BB6E;
}

a.nuxt-link-exact-active .menu-icon svg path,
a.nuxt-link-exact-active .menu-header,
a.nuxt-link-exact-active .menu-text {
  fill: #90BB6E;
  /* stroke: #90BB6E; */
  color: #90BB6E;
}

.menu-text {
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
