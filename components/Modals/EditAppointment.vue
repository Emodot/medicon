<template>
  <div class="modal-backdrop-2">
    <div class="modal-2">
      <div class="top-modal">
        <p>Edit appointment</p>
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <rect
            x="2"
            y="2"
            width="20"
            height="20"
            rx="10"
            fill="#D9D9D9"
          />
          <path d="M15.0156 13.7703L13.2366 11.9923L15.0146 10.2143C15.3566 9.87326 15.3566 9.31826 15.0146 8.97726C14.6726 8.63326 14.1196 8.63426 13.7776 8.97626L11.9986 10.7543L10.2196 8.97426C9.8776 8.63226 9.3236 8.63426 8.9816 8.97426C8.6406 9.31626 8.6406 9.87126 8.9816 10.2123L10.7616 11.9923L8.9856 13.7673C8.6436 14.1093 8.6436 14.6643 8.9856 15.0043C9.1566 15.1763 9.3796 15.2613 9.6036 15.2613C9.8286 15.2613 10.0516 15.1763 10.2226 15.0053L11.9986 13.2293L13.7786 15.0083C13.9496 15.1793 14.1726 15.2643 14.3966 15.2643C14.6206 15.2643 14.8446 15.1783 15.0156 15.0083C15.3576 14.6663 15.3576 14.1123 15.0156 13.7703Z" fill="#200E32" />
        </svg>
      </div>
      <hr class="line">
    </div>
  </div>
</template>

<script>
export default {
  props: {
    userEmail: {
      type: String,
      default: 'emodot991@gmail.com'
    }
  },
  data () {
    return {
      // userEmail: ''
    }
  }
}
</script>

<style scoped>
* {
  font-family: 'Poppins', sans-serif;
  color: #454545;
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
  border-radius: 10px;
  overflow-y: auto;
  padding: 30px;
}

.top-modal {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.top-modal p {
  font-size: 20px;
  font-weight: 600;
}

.line {
  border: none;
  border-top: 1px solid rgba(0, 0, 0, 0.162);
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
