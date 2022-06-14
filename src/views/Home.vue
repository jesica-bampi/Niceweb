<template>
  <div class="home container">
    <div class="content-form">
      <div class="content-form-title">
        <h1>For sale</h1>
      </div>
      <form class="row content-form-elements" @submit.prevent="send()">
        <div class="col form-group content-form-elements-form">
          <input type="text" class="form-control" v-model="form.name" placeholder="nome" required>
        </div>
        <div class=" col form-group content-form-elements-form">
          <input type="email" class="form-control" v-model="form.email" placeholder="email" required>
        </div>
        <div class=" col form-group content-form-elements-form">
          <label for="proposal">U$D</label>
          <input id="proposal" type="text" class="form-control" v-model="form.proposal" placeholder="proposal" required>
          
        </div>
        <div class="content-form-elements-btn">
          <button type="submit" class="btn btn-primary">Enviar</button>
        </div>
      </form>
    </div>
    <div class="content logo">
      <img src="@/assets/img/logo-niceweb.png" alt="logo" class="img-fluid">
    </div>
    <template id="modalThankYou" class="" v-if="showModal == true">
      <div class="content-success">
        <div class="content-success-card">
          <h1>Thank you!</h1>
          <h5>Your proposal has been sent successfully.<br> Soon we will contact you.</h5>
          <button @click="closeModal()">
            <p>ok</p>
          </button>
        </div>
      </div>
  </template>
  </div>
</template>
<script>

export default {
  data() {
    return {
      form: {
        name: '',
        email: '',
        proposal: ''
      },
      showModal: false
    }
  },
  methods: {
    send() {
      console.log(this.form);
      this.showModal = true;
      this.form = {}
    },
    closeModal() {
      this.showModal = false;
    }
  }
}
</script>
<style src="./style.scss" lang="scss" scoped />

