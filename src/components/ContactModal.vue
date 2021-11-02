<template>
  <div id="modal" class="overlay-menu" v-show="contactOpen">
    <!-- Modal Content -->
    <div class="modal-content">
      <!-- Modal Header -->
      <div class="modal-header">
        <div class="close-btn">
          <img src="../assets/img/close_contact.png" alt="" />
        </div>
      </div>
      <!-- Modal Body -->
      <div class="modal-body">
        <div class="col-md-6 col-md-offset-3">
          <form id="contact" v-on:submit.prevent="submitForm">
            <div class="row">
              <div class="col-md-12">
                <fieldset>
                  <input
                    name="name"
                    type="text"
                    v-model="name"
                    class="form-control"
                    id="name"
                    placeholder="Nombre..."
                    required
                  />
                </fieldset>
              </div>
              <div class="col-md-12">
                <fieldset>
                  <input
                    name="_replyto"
                    type="email"
                    v-model="email"
                    class="form-control"
                    id="email"
                    placeholder="Email..."
                    required
                  />
                </fieldset>
              </div>
              <div class="col-md-12">
                <fieldset>
                  <textarea
                    name="message"
                    rows="6"
                    v-model="message"
                    class="form-control"
                    id="message"
                    placeholder="Mensaje..."
                    required
                  ></textarea>
                </fieldset>
              </div>
              <div class="col-md-12">
                <fieldset>
                  <button type="submit" id="form-submit" class="btn">
                    Enviar mensaje
                  </button>
                </fieldset>
              </div>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ContactModal",
  data() {
    return {
      name: "",
      email: "",
      message: "",
      endpoint: "https://formspree.io/madeangelis@gmail.com",
    };
  },
  props: {
    contactOpen: Boolean,
  },
  methods: {
    // async submitForm() {
    //   const data = {
    //     name: this.name,
    //     email: this.email,
    //     message: this.message,
    //   };
    //   const response = await this.$axios.post(this.endpoint, data);
    // },
  },
};
</script>

<style scoped>
.modal {
  background-color: rgba(0, 0, 0, 0.95);
  display: none;
  overflow: auto;
  position: fixed;
  z-index: 1000;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  transform: all 0.6s;
  overflow: scroll;
}

.modal::-webkit-scrollbar {
  display: none;
}

/* Modal Content */
.modal-content {
  text-align: center;
  position: relative;
  top: 0;
  width: 100%;
  margin: 0 auto;
  background-color: transparent;
}
.modal-animated-in {
  animation: totop-in 0.6s ease;
}
.modal-animated-out {
  animation: totop-out 0.6s ease forwards;
}
.modal-header {
  border-bottom: none;
}
.modal-header h3 {
  color: #fff;
  font-weight: 400;
  letter-spacing: 1px;
  font-size: 64px;
  margin-top: 5%;
  border-bottom: none;
  margin-bottom: 20px;
}

.modal-header em {
  font-style: normal;
  font-weight: 200;
}

.modal-content .close-btn {
  position: absolute;
  z-index: 99999999;
  color: #fff;
  right: 38px;
  top: 15px;
  width: 50px;
  height: 50px;
  text-align: center;
  cursor: pointer;
}

.modal-body {
  text-align: center;
  margin: 0 auto;
}

.modal-body input {
  border-radius: 5px;
  padding-left: 15px;
  font-size: 14px;
  font-weight: 200;
  color: #fff;
  background-color: rgba(250, 250, 250, 0.15);
  outline: none;
  border: none;
  box-shadow: none;
  line-height: 40px;
  height: 40px;
  width: 60%;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 25px;
}

.modal-body textarea {
  border-radius: 5px;
  padding-left: 15px;
  padding-top: 10px;
  font-size: 14px;
  font-weight: 200;
  color: #fff;
  background-color: rgba(250, 250, 250, 0.15);
  outline: none;
  border: none;
  box-shadow: none;
  height: 165px;
  max-height: 220px;
  width: 60%;
  margin-left: auto;
  margin-right: auto;
  max-width: 100%;
  margin-bottom: 25px;
}

.modal-body button {
  border-radius: 0px;
  font-size: 13px;
  text-transform: uppercase;
  font-weight: 600;
  background-color: transparent;
  color: #fff;
  letter-spacing: 2px;
  border-bottom: 3px solid #fff;
  display: inline-block;
  padding: 0px 0px 3px 0px;
  transition: all 0.5s;
  border-top: none;
  border-right: none;
  border-left: none;
}

.modal-body button:hover {
  color: rgba(250, 250, 250, 0.5);
  border-color: rgba(250, 250, 250, 0.5);
  outline: none;
}

.experience-container {
  width: fit-content;
}

@media (max-width: 530px) {
  .modal-header h3 {
    margin-top: 35%;
  }

  .modal-body input {
    width: 100%;
  }

  .modal-body textarea {
    width: 100%;
  }

  .modal-content {
    padding-bottom: 40px;
  }
}
/* Keyframes */
@keyframes totop-in {
  0% {
    top: 600px;
    opacity: 0;
  }
  100% {
    top: 0%;
    opacity: 1;
  }
}

@keyframes totop-out {
  0% {
    top: 0px;
    opacity: 1;
  }
  100% {
    top: -100%;
    opacity: 0;
  }
}
</style>
