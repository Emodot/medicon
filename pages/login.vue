<template>
  <div class="container">
    <div class="inner">
      <div class="lhs">
        <div class="logo">
          <img src="~assets/images/medicon-logo.png" alt="">
        </div>
        <p class="title">
          Sign In
        </p>
        <p class="sub-title">
          Sign in to access your Account
        </p>
      </div>
      <div class="rhs" />
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.inner {
  display: flex;
  height: 100vh;
}

.lhs {
  flex-basis: 35%;
  padding: 70px 50px;
}

.rhs {
  flex-basis: 65%;
  background-image: url('assets/images/login-bg.jpg');
  background-size: cover;
}
</style>
