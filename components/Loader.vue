<template>
  <div class="loader-ctn">
    <div class="loader reveals" />
  </div>
</template>

<style scoped>
.loader-ctn {
  width: 100%;
  /* margin-top: 5%; */
}
.loader {
  border: 3px solid #f3f3f3;
  border-radius: 50%;
  border-top: 3px solid #000;
  width: 20px;
  height: 20px;
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
