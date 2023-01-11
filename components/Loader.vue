<template>
  <div class="loader-ctn">
    <div class="loader reveals" />
  </div>
</template>

<style scoped>
.loader-ctn {
  /* width: 100%; */
}
.loader {
  border: 2.5px solid #f2f3f3;
  border-radius: 50%;
  border-top: 2.5px solid #1D692C;
  width: 18px;
  height: 18px;
  -webkit-animation: spin 0.6s linear infinite;
  animation: spin 0.6s linear infinite;
  margin: 0 auto;
}

@-webkit-keyframes spin {
  0% {
    -webkit-transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(360deg);
  }
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>
